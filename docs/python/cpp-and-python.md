---
title: "Práce s C++ a Python v sadě Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 09/28/2017
ms.reviewer: 
ms.suite: 
ms.technology: devlang-python
ms.devlang: python
ms.tgt_pltfrm: 
ms.topic: get-started-article
ms.assetid: f7dbda92-21bf-4af0-bb34-29b8bf231f32
description: "Kroky amd zpracování napsat modul nebo rozšíření C++ pro Python v sadě Visual Studio"
caps.latest.revision: "1"
author: kraigb
ms.author: kraigb
manager: ghogen
ms.openlocfilehash: 0438a2d0f2524ea2163cb3454fdcf50f2ae7f499
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="creating-a-c-extension-for-python"></a>Vytváření rozšíření pro C++ pro jazyk Python

Moduly, které jsou napsané v C++ (nebo C) se běžně používají k rozšíření možností překladač Pythonu tak, aby přístup k funkcím nízké úrovně operačního systému. Existují tři primární typy modulů:

- Moduly akcelerátoru: Python je interpretovaný jazyk, a proto může být zapsán určité části kódu v jazyce C++ pro vyšší výkon. 
- Obálka moduly: obálky vystavit existující rozhraní C/C++ pro kód Python nebo odhalí další rozhraní API "Pythonic", které se snadno používá z Pythonu.
- Nízké úrovně systému přístup moduly: vytvořili pro přístup k funkcím nižší úrovně CPython runtime, operační systém nebo základní hardware. 

Toto téma vás provede sestavování rozšíření modulu C++ pro CPython, která vypočítá hyperbolický tangens a volá z kódu jazyka Python. Rutiny se implementuje nejprve v Pythonu k předvedení výkonnější implementace stejné rutiny v jazyce C++.

Přístup prováděné v tomto poli je, že pro standardní CPython rozšíření, jak je popsáno v [Python dokumentaci](https://docs.python.org/3/c-api/). Porovnání mezi touto a jinými prostředky je popsaný v části [Alternativní přístupy](#alternative-approaches) na konci tohoto tématu.

## <a name="prerequisites"></a>Požadavky

- Visual Studio 2017 s oběma **vývoj plochy s jazykem C++** a **vývoj Python** úlohy, které jsou nainstalované s výchozími možnostmi. 
- V **vývoj Python** zatížení, taky zaškrtnout políčko na pravé straně pro **Python tools nativní vývoj**, která nastaví většina možností popsaných v tomto tématu. (Tato možnost také zahrnuje úlohy C++ automaticky.) 

![Vybráním možnosti nástroje jazyka Python nativní vývoj](media/cpp-install-native.png)

- Instalace **vědecké zpracování dat a analytických aplikací** zatížení také zahrnuje Python a **Python tools nativní vývoj** možnost ve výchozím nastavení.

Další informace najdete v tématu [instalaci podpory jazyka Python pro Visual Studio](installation.md), včetně použití jiné verze sady Visual Studio. Pokud instalujete Python samostatně, je nutné vybrat **stáhnout symboly ladění** a **ladicí binární soubory ke stažení** pod **pokročilé možnosti** v instalačním programu. Tato možnost zajistí, abyste měli k dispozici nezbytné ladění knihoven, pokud se rozhodnete sestavení ladicí verze.

## <a name="create-the-python-application"></a>Vytvoření aplikace Python

1. Vytvořte nový projekt Python v sadě Visual Studio výběrem **soubor > Nový > projekt**. Vyhledejte "Python", vyberte **aplikace Python** šablony, poskytněte vhodný název a umístění a vyberte **OK**.

1. V projektu `.py` souboru, vložte následující kód, který benchmarks výpočet hyperbolický tangens (implementována bez použití knihovny math pro snazší porovnání). Můžete zadat kód ručně, aby některé z prostředí [Python úpravy funkce](code-editing.md).

    ```python
    from itertools import islice
    from random import random
    from time import perf_counter

    COUNT = 500000  # Change this value depending on the speed of your computer
    DATA = list(islice(iter(lambda: (random() - 0.5) * 3.0, None), COUNT))

    e = 2.7182818284590452353602874713527

    def sinh(x):
        return (1 - (e ** (-2 * x))) / (2 * (e ** -x))

    def cosh(x):
        return (1 + (e ** (-2 * x))) / (2 * (e ** -x))

    def tanh(x):
        tanh_x = sinh(x) / cosh(x)
        return tanh_x

    def sequence_tanh(data):
        '''Applies the hyperbolic tangent function to map all values in
        the sequence to a value between -1.0 and 1.0.
        '''
        result = []
        for x in data:
            result.append(tanh(x))
        return result

    def test(fn, name):
        start = perf_counter()
        result = fn(DATA)
        duration = perf_counter() - start
        print('{} took {:.3f} seconds\n\n'.format(name, duration))

        for d in result:
            assert -1 <= d <=1, " incorrect values"

    if __name__ == "__main__":
        print('Running benchmarks with COUNT = {}'.format(COUNT))
        test(sequence_tanh, 'sequence_tanh')

        test(lambda d: [tanh(x) for x in d], '[tanh(x) for x in d]')
    ```

1. Spustit pomocí programu **ladění > Spustit bez ladění** (Ctrl + F5) a zobrazte si výsledky. Můžete upravit `COUNT` proměnné změnit, jak dlouho trvat srovnávací testy ke spuštění. Pro účely tohoto návodu nastavte počet tak, aby každý srovnávací test trvá přibližně dvou sekund.

## <a name="create-the-core-c-project"></a>Vytvoření projektu C++ jádra

1. V Průzkumníku řešení klikněte pravým tlačítkem a vyberte **Přidat > Nový projekt...** . Řešení sady Visual Studio může obsahovat Python a C++ projekty společně.

1. Vyhledávání v "C++", vyberte **prázdný projekt**, zadejte název (například TanhBenchmark) a vyberte **OK**. Poznámka: Pokud jste nainstalovali **nativní vývoj nástrojů Python** s Visual Studio 2017, můžete spustit v **modul Python rozšíření** šablony, která má velmi co je zde popsáno již na místě . V tomto návodu ale spuštění s prázdným projektem ukazuje vytvoření rozšíření modulu krok za krokem.

1. Vytvořte soubor C++ v novém projektu kliknutím pravým tlačítkem myši **zdrojové soubory** uzlu, pak vyberte **Přidat > novou položku... "**, vyberte **soubor C++**, zadejte jeho název (jako `module.cpp`) a vyberte **OK**. Tento krok je nutné zapnout na stránkách vlastností C++ v dalších krocích.

1. Klikněte pravým tlačítkem na nový projekt a vyberte **vlastnosti**, pak v horní části **stránky vlastností** nastavte dialogové okno, který se zobrazí **konfigurace** k **všechny Konfigurace**.

1. Nastavte konkrétní vlastnosti, jak je popsáno níže a potom vyberte **OK**.

    | Tabulátor | Vlastnost | Hodnota | 
    | --- | --- | --- |
    | Obecné | Obecné > název cíle | Nastavte pole přesně odpovídal názvu modulu jako Python uvidí ho. |
    | | Obecné > cíle rozšíření | .pyd |
    | | Výchozí nastavení projektu > typ konfigurace | Dynamická knihovna (DLL) |
    | C/C++-> Obecné | Další zahrnuté adresáře | Přidat Python `include` složky podle potřeby pro instalaci, například`c:\Python36\include` |     
    | C/C++ > preprocesor | Definice preprocesoru | Přidat `Py_LIMITED_API;` na začátek řetězce, který omezuje některé funkce můžete volat z Python a umožňuje kód víc přenosného mezi různými verzemi jazyka Python. |
    | C/C++ > generování kódu | Běhové knihovny | Vícevláknové knihovny DLL (/ MD) (viz následující upozornění) |
    | Linkeru > Obecné | Další knihovny adresáře | Přidat Python `libs` složku obsahující `.lib` soubory potřebné pro instalaci, například `c:\Python36\libs`. (Ujistěte se, tak, aby odkazoval `libs` složku, která obsahuje `.lib` soubory, a *není* `Lib` složku, která obsahuje `.py` soubory.) | 

    > [!Tip]
    > Pokud se nezobrazí na kartě C/C++, je to, protože projektu neobsahuje všechny soubory, které označuje jako C/C++ zdrojové soubory. K tomuto stavu může dojít, pokud vytvoření zdrojového souboru bez `.c` nebo `.cpp` rozšíření. Například, pokud jste omylem zadali `module.coo` místo `module.cpp` nové položky dříve v dialogovém okně, pak Visual Studio vytvoří soubor, ale typ souboru není nastavena na "C / C + kód," což je co aktivuje na kartě Vlastnosti C/C++. Tato misidentification zůstane tak i v případě, že přejmenujte soubor s `.cpp`. Typ souboru nastavit správně, klikněte pravým tlačítkem na soubor v Průzkumníku řešení, vyberte **vlastnosti**, nastavte **typ souboru** k **kódu C/C++**.

    > [!Warning]
    > Není nastavený **C/C++ > generování kódu > Runtime Library** na možnost "vícevláknové ladění knihoven DLL (/ MDd)" i pro konfiguraci ladění. Vyberte "vícevláknové knihovny DLL (/ MD)" runtime protože se jedná, co jsou vytvořené binární soubory bez ladění Python s. Pokud jste se nastavit možnost /MDd, se zobrazí chyba *C1189: Py_LIMITED_API není kompatibilní s Py_DEBUG, Py_TRACE_REFS a Py_REF_DEBUG* při sestavování konfiguraci ladění vaší knihovny DLL. Kromě toho pokud odeberete `Py_LIMITED_API` nechcete chyby sestavení, Python, dojde k chybě při pokusu o import modulu. (V rámci volání knihovny DLL se stane havárii `PyModule_Create` jak je popsáno dále, s výstup zprávu *Python závažná chyba: PyThreadState_Get: žádný aktuální vlákno*.)
    >
    > Možnost /MDd je, co se používá k sestavení ladicí binární soubory Python (například python_d.exe), ale stále výběr rozšiřující knihovny DLL způsobuje chybu sestavení s `Py_LIMITED_API`.
   
1. Klikněte pravým tlačítkem na projekt C++ a vyberte **sestavení** k testování vaše konfigurace (ladění a vydání). `.pyd` Soubory jsou umístěny v *řešení* ve složce **ladění** a **verze**, není C++ projektu samotné složce.

1. Přidejte následující kód do projektů C++ je hlavní `.cpp` souboru:

    ```cpp
    #include <Windows.h>
    #include <cmath>    

    const double e = 2.7182818284590452353602874713527;

    double sinh_impl(double x) {
        return (1 - pow(e, (-2 * x))) / (2 * pow(e, -x));
    }

    double cosh_impl(double x) {
        return (1 + pow(e, (-2 * x))) / (2 * pow(e, -x));
    }

    double tanh_impl(double x) {
        return sinh_impl(x) / cosh_impl(x);
    }
    ```

1. Sestavení projektu C++ znovu pro potvrzení, že jste kód napsali správně.


## <a name="convert-the-c-project-to-an-extension-for-python"></a>Převedení projektu C++ na rozšíření pro jazyk Python

Chcete-li C++ DLL do rozšíření pro jazyk Python, budete muset upravit exportovaných metod pro interakci s typy Python. Pak musíte přidat funkce, který exportuje modulu, společně s definice metod modulu. Pozadí na co se zde zobrazí, najdete v části [Python nebo C API referenční příručce](https://docs.python.org/3/c-api/index.html) a hlavně [objekty modulu](https://docs.python.org/3/c-api/module.html) na python.org. (Nezapomeňte z ovládacího prvku rozevíracího seznamu v pravém horním rohu vyberte verzi jazyka Python.)

1. V souboru C++ zahrnují `Python.h` v horní části:

    ```cpp
    #include <Python.h>
    ```

1. Změnit `tanh_impl` metoda přijmout a návratové typy Python:

    ```cpp
    PyObject* tanh_impl(PyObject *, PyObject* o) {
        double x = PyFloat_AsDouble(o);
        double tanh_x = sinh_impl(x) / cosh_impl(x);
        return PyFloat_FromDouble(tanh_x);
    }
    ```

1. Přidat strukturu, která definuje jak C++ `tanh` pro Python zobrazí funkce:

    ```cpp
    static PyMethodDef superfastcode_methods[] = {
        // The first property is the name exposed to python, the second is the C++ function name        
        { "fast_tanh", (PyCFunction)tanh_impl, METH_O, nullptr },

        // Terminate the array with an object containing nulls.
        { nullptr, nullptr, 0, nullptr }
    };
    ```

1. Přidejte do struktury definující modul Python uvidí ho:

    ```cpp
    static PyModuleDef superfastcode_module = {
        PyModuleDef_HEAD_INIT,
        "superfastcode",                        // Module name
        "Provides some functions, but faster",  // Module description
        0,
        superfastcode_methods                   // Structure that defines the methods
    };
    ```

1. Přidejte metodu, která volá Python, pokud ho načte modul, který musí mít název `PyInit_<module-name>`, kde  *&lt;module_name&gt;*  přesně odpovídá projektu C++ **Obecné > název cílové** vlastnost (to znamená, odpovídá název souboru `.pyd` sestavený projektem).

    ```cpp
    PyMODINIT_FUNC PyInit_superfastcode() {    
        return PyModule_Create(&superfastcode_module);
    }
    ```

1. Sestavení projektu C++ znovu k ověření vašeho kódu.

## <a name="test-the-code-and-compare-the-results"></a>Testování kódu a porovnejte výsledky

Teď, když máte knihovnu DLL strukturovaná jako rozšíření Python, můžete na ni odkazuje z projektu Python, naimportujte modul a použít její metody.

### <a name="make-the-dll-available-to-python"></a>Zpřístupnit knihovnu DLL jazyka Python

Existují dva způsoby, jak zpřístupnit knihovnu DLL jazyka Python.

Nejprve přidáte odkaz z projektu Python do projektu C++ za předpokladu, že jsou ve stejném řešení sady Visual Studio:

1. V Průzkumníku řešení klikněte pravým tlačítkem myši **odkazy** uzlu v projektu jazyka Python a vyberte **přidat odkaz na**. V dialogovém okně se zobrazí, vyberte **projekty** vyberte **superfastcode** projektu (nebo ať název je používáte) a potom **OK**.

Druhý instalací modulu v globální prostředí Python zpřístupnění do jiných Python projektů. Proto obvykle to vyžaduje, můžete obnovit databázi doplňování IntelliSense pro prostředí. Aktualizace je také nezbytné při odebírání modulu z prostředí.

1. Pokud používáte Visual Studio 2017, spusťte instalační program sady Visual Studio, vyberte **upravit**, vyberte **jednotlivých součástí > kompilátory, sestavení nástroje a moduly runtime > Sada nástrojů Visual C++ 2015.3 v140**. Tento krok je nezbytný, protože Python (pro Windows) je sám vytvořené s nástroji Visual Studio 2015 (verze 14.0) a očekává, že tyto nástroje jsou k dispozici při sestavování rozšíření pomocí metody popsané v tomto poli.

1. Vytvořte soubor s názvem `setup.py` v projektu jazyka C++ kliknutím pravým tlačítkem na projekt a výběrem **Přidat > novou položku...** . Potom vyberte "Soubor C++ ()", zadejte název souboru `setup.py`a výběr **OK** (pojmenovávání souborů a `.py` rozšíření umožňuje rozpoznat ho jako Python bez ohledu C++ pomocí souborů šablony sady Visual Studio). Když soubor se zobrazí v editoru, vložte do ní následující kód:

    ```python
    from distutils.core import setup, Extension, DEBUG

    sfc_module = Extension('superfastcode', sources = ['module.cpp'])

    setup(name = 'superfastcode', version = '1.0',
        description = 'Python Package with superfastcode C++ Extension',
        ext_modules = [sfc_module]
        )
    ```

    V tématu [sestavení C a C++ rozšíření](https://docs.python.org/3/extending/building.html) (python.org) pro dokumentaci na tento skript.

1. `setup.py` Kód dá pokyn Python k sestavení rozšíření pomocí nástrojů Visual Studio 2015 C++ při použití z příkazového řádku. Otevřete příkazový řádek se zvýšenými oprávněními, přejděte do složky obsahující projekt C++ (a `setup.py`) a zadejte následující příkaz:

    ```
    pip install .
    ```

### <a name="call-the-dll-from-python"></a>Volání knihovny DLL z Pythonu

Po dokončení některou z výše uvedených metod, teď můžete volat `fast_tanh` funkce a porovnání jeho výkon a Python implementace:

1. Přidejte následující řádky do vaší `.py` souboru k volání `fast_tanh` Metoda Export z knihovny DLL a zobrazí jeho výstup. Pokud zadáte `from s` příkaz ručně, uvidíte `superfastcode` spolu v seznamu dokončení a po zadání `import` `fast_tanh` metodu.

    ```python
    from superfastcode import fast_tanh    
    test(lambda d: [fast_tanh(x) for x in d], '[fast_tanh(x) for x in d]')
    ```

1. Spusťte Python program a najdete v části rutiny C++ rychleji než implementace Python spouští 5 až 20 vyšší. Znovu, zkuste zvýšit `COUNT` proměnné tak, aby rozdíly jsou mnohem výraznější. Všimněte si, že sestavení pro vydání modulu C++ spustí rychleji než sestavení ladicí verze, protože sestavení ladicí verze je menší také Optimalizovaná a obsahuje různé chyby kontroly. Nebojte se, že přepínat mezi tyto konfigurace pro porovnání.

## <a name="debug-the-c-code"></a>Ladění kódu C++

Visual Studio podporuje ladění kódu jazyka Python a C++ společně.

1. Klikněte pravým tlačítkem na projekt Python v Průzkumníku řešení, vyberte **vlastnosti**, vyberte **ladění** a pak vyberte **ladění > Povolit ladění nativního kódu** možnost.

    > [!Tip]
    > Když povolíte ladění nativního kódu, ve výstupním okně Python může zmizet okamžitě, když program dokončí bez budete obvykle pozastavení "Stisknutím libovolné klávesy... Pokračujte". K vynucení pozastavení, přidejte `-i` možnost k **spustit > překladač argumenty** na **ladění** kartě při povolení ladění nativního kódu. Tento argument překladač Pythonu umístí do interaktivním režimu po dokončení kód v tomto okamžiku se čeká na stiskněte klávesy Ctrl + Z, zadejte ukončíte. (Případně, pokud vám nevadí, úprava kódu jazyka Python, můžete přidat `import os` a `os.system("pause")` příkazy na konci vašeho programu. Tento kód duplicity řádku původní pozastavení).

1. Vyberte **soubor > Uložit** uložit změny vlastností.

1. Nastavte konfiguraci sestavení pro ladění na panelu nástrojů Visual Studio. 

    ![Nastavení konfigurace sestavení pro ladění](media/cpp-set-debug.png)

1. Protože kód obvykle trvá déle ke spuštění v ladicím programu, můžete změnit `COUNT` proměnné v vaše `.py` souboru na hodnotu, která je menší přibližně 5 výskyty (můžete například změnit z `500000` k `100000`).

1. Ve vašem kódu C++ nastavit zarážky první řádek `tanh_impl` metoda pak spuštění ladicího programu (F5 nebo **ladění > Spustit ladění**). Ladicí program zastaví, když je volána tento kód. Pokud není průchodu zarážkou, zkontrolujte, že konfigurace je nastavená na ladění a že jste uložili projektu (který neprobíhá automaticky při spuštění ladicího programu).

    ![Zastavení u zarážky v kódu C++](media/cpp-debugging.png)

1. V tomto okamžiku můžete krok prostřednictvím kódu C++, zkontrolujte proměnné a tak dále. Tyto funkce jsou podrobně popsané na [ladění C++ a Python společně](debugging-mixed-mode.md).

## <a name="alternative-approaches"></a>Alternativní přístupy 

Existuje mnoho různých prostředků k vytvoření rozšíření Python, jak je popsáno v následující tabulce. První položka pro CPython je, co bylo popsané v tomto tématu již.

| Přístup | Ročníku | Zástupce jiní uživatelé | Pro(s) | CON(s) |
| --- | --- | --- | --- | --- |
| C/C++ rozšíření modulů pro CPython | 1991 | Standardní knihovna | [Kurzy a rozsáhlou dokumentaci](https://docs.python.org/3/c-api/). Celkový počet ovládacího prvku. | Kompilace, přenositelnost, odkaz na správu. Vysoká C znalostní báze. |
| SWIG | 1996 | [crfsuite](http://www.chokkan.org/software/crfsuite/) | Generovat vazby u mnoha jazycích najednou. | Nadměrnému zatížení, pokud Python je jediný cíl. |
| ctypes | 2003 | [oscrypto](https://github.com/wbond/oscrypto) | Žádné kompilace široké dostupnosti. | Přístup k informacím a mutace C struktury náročná a chyba náchylné k chybám. |
| Cython | 2007 | [gevent](http://www.gevent.org/), [kivy](https://kivy.org/) | Jako Python. Vysoce vyspělá. Vysoký výkon. | Kompilace a nástrojů a nové syntaxe. |
| cffi | 2013 | [kryptografie](https://cryptography.io/en/latest/), [pypy](http://pypy.org/) | Snadná integrace, PyPy kompatibility. | Nové, méně vyspělá. |