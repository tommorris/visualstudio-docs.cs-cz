---
title: Obecné, ladění, dialogové okno Možnosti | Dokumentace Microsoftu
ms.custom: ''
ms.date: 05/23/2017
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.options.General
- VS.ToolsOptionsPages.Debugger.General
- VS.ToolsOptionsPages.Debugger.ENC
- vs.debug.options.ENC
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- Options dialog box, debugging
ms.assetid: b33aee0b-43c3-4c26-8ed4-bc673f491503
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e46301c84b1a9b27eed8cb6667b312ff73af2960
ms.sourcegitcommit: 1ab675a872848c81a44d6b4bd3a49958fe673c56
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2018
ms.locfileid: "44280634"
---
# <a name="general-debugging-options-dialog-box"></a>Obecné, ladění, dialogové okno Možnosti
**Nástroje > Možnosti > ladění > Obecné** stránce umožňuje nastavit možnosti uvedené v tomto článku.

Pokud potřebujete obnovit výchozí nastavení, můžete to, že při použití **nástroje** > **nastavení importu a exportu** > **obnovit všechna nastavení**. Pokud chcete obnovit podmnožinu nastavení, nastavení v uložte **Průvodce importem a exportem nastavení** před prováděním změn, které chcete testovat, pak naimportujte uložená nastavení později.
  
**Zeptat se před smazáním všech zarážek** vyžaduje potvrzení před dokončením **smazat všechny zarážky** příkazu.  
  
**Přerušit všechny procesy při přerušení jednoho procesu** současně ukončí všechny procesy, ke kterým je připojen ladicí program, když dojde k přerušení.  
  
**Přerušit, pokud výjimky kříží třídu AppDomain nebo spravované/nativní hranice** ve spravovaném nebo kombinovaném režimu ladění, modul common language runtime může zachytit výjimky, které překračují hranice aplikační domény nebo spravované/nativní hranice při následující podmínky jsou splněny:  
  
1\) když nativní kód volá spravovaný kód pomocí zprostředkovatele komunikace s objekty COM a spravovaný kód vyvolá výjimku. Zobrazit [představení zprostředkovatele komunikace s objekty COM](/dotnet/articles/visual-basic/programming-guide/com-interop/introduction-to-com-interop).  
  
2\) když spravovaný kód spuštěný v aplikační doméně 1 volá spravovaný kód v aplikační doméně 2, a vyvolá výjimku, kód v aplikační doméně 2. Zobrazit [programování pomocí domén aplikace](/dotnet/articles/framework/app-domains/index).  

3\) když kód volá funkci pomocí reflexe a funkce vyvolá výjimku. Zobrazit [reflexe](/dotnet/framework/reflection-and-codedom/reflection).  
  
V podmínce 2 a 3, výjimka někdy zachycena spravovaným kódem v `mscorlib` místo modul common language runtime. Tato možnost nemá vliv na zastavení při výjimkách zachycených podle `mscorlib`.  
  
**Povolit ladění na úrovni adres** umožňuje používat pokročilé funkce pro ladění na úrovni adresy ( **zpětný překlad** okně **zaregistruje** okna a zarážky adresy).  
  
- **Zobrazit zpětný překlad, pokud není k dispozici zdroj** automaticky zobrazí **zpětný překlad** okno při pokusu o ladění kódu pro zdroj, který je k dispozici.  
  
**Povolit filtry zarážek** vám umožní nastavit filtry zarážky tak, že se ovlivní pouze specifické procesy, vlákna nebo počítače.  
 
**Pomocí nového pomocníka výjimka** umožňuje pomocníka výjimky (Visual Studio 2017), který nahrazuje Pomocníka pro výjimky.
  
> [!NOTE]
> Pro spravovaný kód, tato možnost nazývala dříve **Povolit Pomocníka pro výjimky** . 
  
**Povolit volbu pouze vlastní kód** ladicí program zobrazí a vstoupí do jenom uživatelský kód ("můj kód"), ignoruje systémový kód a jiný kód, který je optimalizován nebo který nemá žádné symboly ladění.

- **Varovat při žádném uživatelském kódu při spuštění (pouze spravované)** při spuštění ladění s povoleným kódem Just My, tato možnost vás upozorní, pokud neexistuje žádný uživatelský kód ("můj kód"). 

**.NET Framework, povolit krokování zdrojových kódů** umožňuje ladicímu programu vstup do zdroje rozhraní.NET Framework. Povolením této možnosti automaticky zakážete pouze můj kód rozhraní .NET Framework symboly budou staženy do umístění mezipaměti. Můžete změnit umístění mezipaměti v **možnosti** dialogovém okně **ladění** kategorie, **symboly** stránky.  
  
**Krokovat přes vlastnosti a operátory (pouze spravované)** ladicí program zabraňuje krokování s vnořením do vlastností a operátorů ve spravovaném kódu.  
  
**Povolit vyhodnocování vlastností a jiných implicitních volání funkcí** Zapne automatické hodnocení vlastností a implicitní funkce se volá v oknech proměnných a **QuickWatch** dialogové okno.  
  
- **Volání funkce pro převod řetězce na objektech v oknech proměnné (C# a JavaScript pouze)** provede volání rozhraní řetězec implicitní převod při vyhodnocování objektů v oknech proměnných. Zobrazí se výsledek jako řetězec namísto názvu typu. Platí pouze při ladění v kódu jazyka C#. Toto nastavení lze přepsat pomocí atributu DebuggerDisplay (viz [pomocí atributu DebuggerDisplay](../debugger/using-the-debuggerdisplay-attribute.md)).  
  
**Povolit podporu zdrojového serveru** sdělí ladicímu programu sady Visual Studio, aby získal zdrojové soubory ze zdrojových serverů, které implementují SrcSrv (`srcsrv.dll`) protokolu. Team Foundation Server a ladění nástroje pro Windows jsou dva servery zdroje, které implementují protokol. Další informace o nastavení SrcSrv naleznete v tématu [zdrojový server](/windows-hardware/drivers/debugger/srcsrv) dokumentaci. Kromě toho najdete v článku [zadejte symbolu (.pdb) a zdrojových souborů](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).  
  
> [!IMPORTANT]
> Protože čtení *PDB* souborů může spustit libovolný kód v souborech, ujistěte se, že serveru důvěřujete.  
  
- **Vytisknout diagnostickou zprávu zdrojového serveru do okna výstup** když je povolena podpora zdrojového serveru, toto nastavení zapne diagnostické zobrazení.  
  
- **Povolit zdrojový server pro sestavení částečné důvěryhodnosti (pouze spravované)** když je povolena podpora zdrojového serveru, toto nastavení potlačí výchozí chování nenačítání zdrojů pro sestavení částečné důvěryhodnosti.  

**Povolit podporu zdrojového odkazu** sdělí ladicímu programu sady Visual Studio ke stažení zdrojových souborů pro soubory PDB, které obsahují informace o odkazu na zdroj. Další informace o odkazu na zdroj, najdete v článku [specifikace propojení zdroje](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/source_link.md).

    > [!IMPORTANT]
    >  Because Source Link will download files using http or https, make sure you trust the .pdb file.  
  
**Zvýraznění celého řádku pro zarážky a aktuální příkaz (pouze C++)** Když ladicí program zvýrazní zarážku nebo aktuální příkaz, jde zvýraznit celý řádek.  
  
**Vyžadovat, aby zdrojové soubory shodovaly původní verze** dává pokyn ladicímu programu k ověření, že zdrojový soubor odpovídá verzi zdrojového kódu k sestavení spustitelného souboru, který ladíte. Pokud verze neodpovídá, budete vyzváni k vyhledání odpovídajícího zdroje. Pokud není nalezen odpovídající zdroj, zdrojový kód se nezobrazí během ladění. 
  
**Přesměrovat text z okna výstup do příkazového podokna** odešle všechny zprávy, které by se obvykle zobrazily v ladicího programu **výstup** okna **okamžité** okno místo.  
  
**Zobrazit nezpracovanou strukturu objektů v oknech proměnných** vypne všechny úpravy zobrazení struktury objektu. Další informace o přizpůsobení zobrazení naleznete v tématu [vytváření vlastních zobrazení objektů .managed](../debugger/create-custom-views-of-dot-managed-objects.md).  
  
**Potlačení optimalizace JIT při načtení modulu (pouze spravované)** zakáže optimalizaci JIT spravovaného kódu, když je modul je načten a JIT je zkompilován, zatímco je připojen ladicí program. Zakázání optimalizace může usnadnit práci ladění některých problémů, i když za cenu výkonu. Pokud používáte pouze můj kód, potlačení JIT optimalizace může způsobit kódu nepocházejícího od uživatele jako uživatelského kódu ("můj kód"). Další informace najdete v tématu [optimalizaci JIT a ladění](../debugger/jit-optimization-and-debugging.md).

**Povolit ladění jazyka JavaScript pro ASP.NET (Chrome a IE)** umožňuje ladicímu prostředku skriptů pro aplikace ASP.NET. Při prvním použití v prohlížeči Chrome budete muset přihlásit do prohlížeče při prvním použití povolení rozšíření Chrome, které jste nainstalovali. Zakažte tuto možnost, chcete-li vrátit ke starší verzi chování.    

**Načtení exportů dll** načte tabulky exportu knihovny dll. Informace o symbolech z tabulky exportu knihovny dll může být užitečné při práci s Windows zprávy, postupů Windows (WindowProcs), objekty COM nebo zařazování nebo libovolnou knihovnou dll pro kterou nemáte symboly. Informace o exportu knihovny dll pro čtení zahrnují nadměrné. Proto tato možnost je ve výchozím nastavení vypnuta.  
  
Chcete-li zjistit, jaké symboly jsou k dispozici v exportní tabulce knihovny DLL, použijte `dumpbin /exports`. Symboly jsou k dispozici pro všechny 32bitové verzi systému dll. V článku `dumpbin /exports` výstupu uvidíte přesný název funkce, včetně jiných než alfanumerických znaků. To je užitečné pro nastavení zarážky na funkci. Názvy funkcí z tabulky exportu knihovny dll může zobrazit ořezané jinde v ladicím programu. Volání jsou uvedena v pořadí volání s aktuální funkcí (nejhlouběji vnořených) nahoře. Další informace najdete v tématu [dumpbin/EXPORTS](/cpp/build/reference/dash-exports).  
  
**Zobrazit paralelních zásobníků Odspodu nahoru diagram** Určuje směr, ve kterém jsou zobrazeny balíčky v **paralelní zásobníky** okna.
  
**Ignorovat výjimky přístupu k paměti GPU, pokud zapsaná data nezměnila hodnotu** ignoruje konflikty časování, které byly zjištěny během ladění, pokud se data nezměnila. Další informace najdete v tématu [ladění kódu GPU](../debugger/debugging-gpu-code.md).  
  
**Použít spravovaný režim kompatibility** nahradí výchozí modul ladění pomocí starší verze, chcete-li povolit tyto scénáře:  
  
- Používáte jiný jazyk rozhraní .NET Framework než C#, VB nebo F #, který obsahuje vlastní vyhodnocení výrazu (to zahrnuje C + +/ CLI).  
  
- Chcete povolit funkce upravit a pokračovat pro projekty v jazyce C++ při ladění ve smíšeném režimu.  
  
> [!NOTE]
> Režim Výběr spravované kompatibility zakáže některé funkce, které jsou implementovány pouze ve výchozím ladicím modulu. 

**Použít starší verze vyhodnocovače výrazů C# a VB** ladicí program použije vyhodnocovače výrazů Visual Studio 2013 C# /VB místo vyhodnocovače výrazů Visual Studio 2015 roslynu.    
  
**Upozornit při opakovaném použití vlastních vizualizérů ladění s potenciálně nebezpečnými procesy (pouze spravované)** sady Visual Studio vás upozorní, když používáte vlastní vizualizér, na kterém běží kód v procesu laděného procesu, protože to může spuštěn nebezpečný kód.  
  
**Povolit přidělování haldy při ladění Windows (pouze nativní)** umožňuje haldy ladění systému windows k vylepšení diagnostiky haldy. Povolením této možnosti bude mít vliv na výkon ladění.  
  
**Povolit nástroje pro ladění uživatelského rozhraní pro XAML** The Live Visual Tree a Live prozkoumejte vlastnost windows se zobrazí při spuštění ladění (F5) typ projektu podporovaná. Další informace najdete v tématu [vlastnosti kontrolovat XAML při ladění](../debugger/inspect-xaml-properties-while-debugging.md).  
  
- **Zobrazit náhled vybraných elementů v dynamickém vizuálním stromu** The XAML prvek, jehož kontext je vybraná také vybraný v **Live Visual Tree** okna.  
  
- **Zobrazit nástroje runtime v aplikaci** ukazuje, **Live Visual Tree** příkazy na panelu nástrojů v hlavním okně aplikace XAML, která je právě laděna. Tato možnost byla zavedena v aplikaci Visual Studio 2015 Update 2. 

- **Povolit XAML Edit and Continue** umožňuje použití operace upravit a pokračovat funkcí pro kód XAML. 
  
**Při ladění povolit diagnostické nástroje** **diagnostické nástroje** při ladění, zobrazí se okno.
  
**Zobrazit časem, který uplynul při ladění** okna kódu zobrazí uplynulý čas dané metody volání při ladění.  
  
**Povolení funkce upravit a pokračovat** můžete použít upravit a pokračovat funkce při ladění.  
  
- **Povolit nativní upravit a pokračovat** můžete použít upravit a pokračovat funkce při ladění nativního kódu C++. Další informace najdete v tématu [upravit a pokračovat (Visual C++)](../debugger/edit-and-continue-visual-cpp.md).  
  
- **Použít změny při pokračování (jenom nativní)** sady Visual Studio automaticky zkompiluje a použije všechny zbývající kód změny provedené při pokračování procesu ze stavu pozastavení. Pokud není vybrána, můžete použít změny pomocí položky "Použít změny kódu" v nabídce ladění.  
  
- **Upozornit na starý kód (pouze nativní)** získat upozornění na starý kód.    

**Zobrazit spuštění klikněte na tlačítko v editoru během ladění** Pokud je vybraná tato možnost, [běžet do kliknutí](debugger-feature-tour.md#run-to-a-point-in-your-code-quickly-using-the-mouse) tlačítko se zobrazí při ladění.

## <a name="options-supported-in-older-versions-of-visual-studio"></a>Možnosti podporované ve starších verzích sady Visual Studio

Pokud používáte starší verzi sady Visual Studio, může být k dispozici některé další možnosti.

**Povolit Pomocníka pro výjimky** pro spravovaný kód, povolené Pomocníka pro výjimky. V sadě Visual Studio 2017 nahrazuje pomocníka výjimky Pomocníka pro výjimky.

**Vrátit zásobník volání v případě neošetřených výjimek** způsobí, že **zásobník volání** okno vrátit zásobník volání do bodu předtím, než došlo k neošetřené výjimce. 

**Varovat, pokud při spuštění (pouze nativní) nejsou žádné symboly** zobrazí dialogové okno upozornění při pokusu o ladění programu, pro které ladicí program neobsahuje žádné informace o symbolu. 

**Varovat, pokud je při spuštění zakázáno ladění skriptu** zobrazí dialogové okno upozornění, když ladicí program se spustí s ladění skriptů zakázáno.

**Použít nativní režim kompatibility** Pokud je vybraná tato možnost, ladicí program používá nativní ladicí program sady Visual Studio 2010 místo nové nativní ladicí program.  
  
Tuto možnost by měla používat při ladění kódu .NET, C++, protože nového modulu pro ladění nepodporuje vyhodnocování výrazů .NET C++. Povolení nativní režim kompatibility zakáže však řadu funkcí, které závisí na aktuální implementace ladicí program k provozu. Například starý modul nemá mnoho vizualizéry pro předdefinované typy, jako jsou `std::string` v projektech Visual Studio 2015.   Použijte projekty Visual Studio 2013 pro ladění optimálnímu v těchto případech.
  
## <a name="see-also"></a>Viz také:  
 [Ladění v sadě Visual Studio](../debugger/index.md)  
 [Prohlídka funkcí ladicího programu](../debugger/debugger-feature-tour.md)
