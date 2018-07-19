---
title: Možnosti příkazového řádku MSTest
ms.date: 07/12/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: reference
helpviewer_keywords:
- vstest.console.exe
- command-line tests
ms.author: gewarren
author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e2821e785d0caf504cd64eb90a6538b1a69e9a26
ms.sourcegitcommit: e5a382de633156b85b292f35e3d740f817715d47
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2018
ms.locfileid: "38978506"
---
# <a name="vstestconsoleexe-command-line-options"></a>VSTest.Console.exe – možnosti příkazového řádku

*VSTest.Console.exe* je nástroj příkazového řádku pro spuštění testů. Několik možností, jak můžete zadat v libovolném pořadí, v příkazovém řádku. Tyto možnosti jsou uvedeny v [Obecné možnosti příkazového řádku](#general-command-line-options).

> [!NOTE]
> Adaptér MSTest v sadě Visual Studio také funguje ve starším režimu (ekvivalent procesu spuštění testů s *mstest.exe*) z důvodu kompatibility. Ve starším režimu nemůže využívat funkci TestCaseFilter. Adaptér můžete přepnout na starší režim při *testsettings* soubor zadán, **forcelegacymode** je nastavena na **true** v *runsettings* soubor, nebo pomocí atributů, jako **HostType**.
>
> Ke spuštění automatizovaných testů na počítači založené na architektuře ARM, je nutné použít *VSTest.Console.exe*.

## <a name="general-command-line-options"></a>Obecné možnosti příkazového řádku

V následující tabulce jsou uvedeny všechny možnosti pro *VSTest.Console.exe* a krátký popis. Podobný Přehled zobrazíte zadáním příkazu `VSTest.Console/?` příkazového řádku.

| Možnost | Popis |
|---|---|
|**[*názvy souborů testů*]**|Spusťte testy ze zadaných souborů. Názvy souborů testů oddělte mezerou.<br />Příklady: `mytestproject.dll`, `mytestproject.dll myothertestproject.exe`|
|**/ Nastavení: [*název_souboru*]**|Spusťte testy s dalším nastavením, například sběrače dat.<br />Příklad: `/Settings:Local.RunSettings`|
|**/ Tests: [*název testu*]**|Spusťte testy s názvy, které obsahují zadané hodnoty. Chcete-li zadat více hodnot, oddělte je čárkami.<br />Příklad: `/Tests:TestMethod1,testMethod2`<br />**/Testy** nemohou být součástí možnost příkazového řádku **/testcasefilter** možnost příkazového řádku.|
|**/ Parallel**|Určuje, že se testy spouští paralelně. Ve výchozím nastavení až všechna dostupná jádra v počítači může být použit. Počet jader, která se pomocí můžete konfigurovat pomocí souboru nastavení.|
|**/ Enablecodecoverage**|Umožňuje spustit diagnostický adaptér CodeCoverage v testovací data.<br />Výchozí nastavení jsou použita, pokud nejsou zadány pomocí souboru nastavení.|
|**/ InIsolation**|Spustí testy v izolovaném procesu.<br />Díky této izolaci *vstest.console.exe* méně pravděpodobné, že proces zastavení v případě chyby v testech, ale testy mohou probíhat pomaleji.|
|**/ UseVsixExtensions**|Tato volba způsobí, *vstest.console.exe* použití procesu nebo přeskočí rozšíření VSIX nainstalovaná do testovacího běhu (pokud existuje).<br />Tato možnost je zastaralý. Počínaje příští hlavní verze sady Visual Studio tato možnost může být odebrán. Přesunout na použití rozšíření k dispozici jako balíček NuGet.<br />Příklad: `/UseVsixExtensions:true`|
|**/ TestAdapterPath: [*cesta*]**|Vynutí *vstest.console.exe* procesu použít vlastní adaptéry testu ze zadané cesty (pokud existuje) v testovacím běhu.<br />Příklad: `/TestAdapterPath:&lt;pathToCustomAdapters&gt;`|
|**/ Platform: [*typ platformy*]**|Cílová architektura platformy, které má být použit pro provádění testů.<br />Platné hodnoty jsou x86 x64 a ARM.|
|**/ Framework: [*verzi rozhraní framework*]**|Cílová verze rozhraní .NET Framework má být použit pro provádění testů.<br />Platné hodnoty jsou Framework35, Framework40, Framework45 a FrameworkUap10.<br />Pokud cílová architektura, která je zadána jako **Framework35**, testy spustit v modulu CLR 4.0 "compatibly režim".<br />Příklad: `/Framework:framework40`|
|**/ TestCaseFilter: [*výraz*]**|Spusťte testy, které odpovídají danému výrazu.<br />< výraz\> je ve formátu < vlastnost\>= < hodnota\>[&#124;< výraz\>].<br />Příklad: `/TestCaseFilter:"Priority=1"`<br />Příklad: `/TestCaseFilter:"TestCategory=Nightly&#124;FullyQualifiedName=Namespace.ClassName.MethodName"`<br />**/Testcasefilter** nemohou být součástí možnost příkazového řádku **/testy** možnost příkazového řádku. <br />Informace o vytváření a používání výrazů naleznete v tématu [testovací případ filtr](https://github.com/Microsoft/vstest-docs/blob/master/docs/filter.md).|
|**/?**|Zobrazí informace o použití.|
|**/ Logger: [*uri/friendlyname*]**|Zadejte protokolovací nástroj pro výsledky testů.<br />Příklad: Pro protokolování výsledků do Visual Studio Test výsledky souboru (TRX), použijte **/Logger:trx**.<br />Příklad: Chcete-li publikovat výsledky testů do sady Team Foundation Server, použijte TfsPublisher:<br />**/Logger:TfsPublisher;**<br />**Kolekce = < adresa url projektu týmové\>;**<br />**BuildName = < název sestavení\>;**<br />**TeamProject = < název týmového projektu\>;**<br />**[; Platform = < výchozí hodnota je "Jakékoli CPU" >]**<br />**[; Flavor = < výchozí hodnota je "Debug" >]**<br />**[; RunTitle = < název\>]**|
|**/ ListTests: [*název_souboru*]**|Zobrazí seznam testů v daném kontejneru testů zjištěných.|
|**/ Listdiscoverers zobrazí**|Zobrazí seznam nainstalovaných nástrojů zjišťování testu.|
|**/ ListExecutors**|Zobrazí seznam nainstalovaných modulů provádění testu.|
|**/ ListLoggers**|Zobrazí seznam nainstalovaných nástrojů protokolování testu.|
|**/ Listsettingsproviders zobrazí**|Zobrazí seznam nainstalovaných poskytovatelů nastavení testu.|
|**/ Příčiny**|Sleduje testy jako při spuštění a, pokud proces hostitele testu dojde k chybě, až vysílá názvy testů v jejich pořadí spuštění a včetně konkrétní test, který byl spuštěn v době selhání. Tímto výstupem je snazší izolovat problematický testu a dále je diagnostikovat. [Další informace o](https://github.com/Microsoft/vstest-docs/blob/master/docs/extensions/blame-datacollector.md).|
|**/ Diag: [*název_souboru*]**|Protokoly diagnostické trasování zapíše do zadaného souboru.|

> [!TIP]
> Možnosti a hodnoty nejsou malá a velká písmena.

## <a name="examples"></a>Příklady

Syntaxe pro spuštění *VSTest.Console.exe* je:

`Vstest.console.exe [TestFileNames] [Options]`

Následující příkaz spustí *VSTest.Console.exe* pro knihovnu testu **myTestProject.dll**:

```cmd
vstest.console.exe myTestProject.dll
```

Následující příkaz spustí *VSTest.Console.exe* s více testovacích souborů. Názvy souborů testů oddělte mezerami:

```cmd
Vstest.console.exe myTestFile.dll myOtherTestFile.dll
```

Následující příkaz spustí *VSTest.Console.exe* s několika možnostmi. Spustí testy v *myTestFile.dll* souboru v izolovaném procesu a používá nastavení uvedená v *Local.RunSettings* souboru. Kromě toho pouze spuštění testů, které jsou označeny "Priority = 1" a zaznamená výsledky do *.trx* souboru.

```cmd
vstest.console.exe  myTestFile.dll /Settings:Local.RunSettings /InIsolation /TestCaseFilter:"Priority=1" /Logger:trx
```