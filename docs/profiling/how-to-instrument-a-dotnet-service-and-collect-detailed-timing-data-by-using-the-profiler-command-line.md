---
title: 'Postupy: instrumentace služby rozhraní .NET a shromažďování podrobných dat časování pomocí příkazového řádku profileru | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: c7a5cbb2f411a6d1e2c01275e07da1ea7321488b
ms.sourcegitcommit: 1b9c1e333c2f096d35cfc77e846116f8e5054557
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/06/2018
ms.locfileid: "34815961"
---
# <a name="how-to-instrument-a-net-service-and-collect-detailed-timing-data-by-using-the-profiler-command-line"></a>Postupy: instrumentace služby rozhraní .NET a shromažďování podrobných dat časování pomocí příkazového řádku profileru

Tento článek popisuje, jak pomocí nástroje příkazového řádku Visual Studio Tools profilace účelem instrumentace [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] služby a shromažďování podrobných dat časování.

> [!NOTE]
> Pomocí metody instrumentace nelze profilu služby, pokud nelze restartovat službu po spuštění počítače, tato služba, která spustí jenom v případě, že operační systém při spuštění.
>
> Nástroje příkazového řádku nástroje profilace jsou umístěné v *\Team Tools\Performance nástroje* podadresáři [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] instalační adresář. Na 64bitových počítačích 64bitové a 32bitové verze nástroje jsou k dispozici. Chcete-li použít nástroje příkazového řádku profileru, musí přidat cestu nástroje do proměnné prostředí PATH okna příkazového řádku nebo ho přidat do samotný příkaz. Další informace najdete v tématu [zadejte cestu k nástroje příkazového řádku](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).
>
> Přidání dat interakce vrstev spuštění profilování vyžaduje konkrétní postupy profilování nástroje příkazového řádku. V tématu [shromažďování dat interakce vrstev](../profiling/adding-tier-interaction-data-from-the-command-line.md).

Shromažďování podrobných dat časování z [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] službu pomocí metody instrumentace můžete použít [VSInstr.exe](../profiling/vsinstr.md) nástroj pro generování instrumentovaného verzi komponentu. Je pak nahradit verzi služby-instrumentovány instrumentovaného verze, a ujistěte se, že služba je nakonfigurována pro spustit ručně. Můžete použít [VSPerfCLREnv.cmd](../profiling/vsperfclrenv.md) nástroj k inicializaci globální profilování proměnné prostředí a pak restartujte počítač hostitele. Potom je nutné spustit profileru.

Když je služba spuštěna, časování data jsou shromažďována automaticky do datového souboru. Můžete pozastavit a obnovit shromažďování dat během relace profilování.

K ukončení relace profilování, vypněte službu a poté explicitně vypněte profileru. Ve většině případů doporučujeme vymazání na konci relace profilování proměnné prostředí.

## <a name="start-the-application-with-the-profiler"></a>Spuštění aplikace s profilerem

1. Otevřete okno příkazového řádku.

2. Použití **vsinstr –** nástroj pro generování instrumentovaného verzi binární.

3. Nahradíte původní binární instrumentovaného verzí. V systému Windows správce řízení služeb, ujistěte se, že služba typ spuštění nastavený na ruční.

4. Inicializace [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] profilace proměnné prostředí. Typ:

     **Vsperfclrenv – /globaltraceon**

5. Restartujte počítač.

6. Otevřete okno příkazového řádku.

7. Spusťte profileru. Typ:

     **VSPerfCmd /start:trace output:** `OutputFile` [`Options`]

    - [/Start](../profiling/start.md)**: trasování** možnost inicializuje profileru.

    - [/Výstup](../profiling/output.md)**:** `OutputFile` možnost je povinná s **/start**. `OutputFile` Určuje název a umístění data profilování (. *Vsp*) souboru.

     Můžete použít některou z následujících možností s **/start:trace** možnost.

    > [!NOTE]
    > **User** a **/crosssession** možnosti jsou obvykle vyžaduje profilování služeb.

    |Možnost|Popis|
    |------------|-----------------|
    |[Parametr/User](../profiling/user-vsperfcmd.md) **:**[`Domain`**\\**]`UserName`|Určuje, doména a uživatelské jméno účtu, který vlastní PROFILOVANÉHO proces. Tato možnost je vyžaduje jenom v případě, že je proces spuštěný jako uživatel, než je přihlášený uživatel. Vlastník procesu, je uvedena ve **uživatelské jméno** sloupec **procesy** karty Správce úloh systému Windows.|
    |[/crosssession](../profiling/crosssession.md)|Umožňuje profilace procesů v jiných relacích. Tato možnost je povinná, pokud je aplikace spuštěna v jiné relaci. ID je uvedena v relaci **ID relace** sloupce v **procesy** karty Správce úloh systému Windows. **/CS** lze zadat jako zkratkou pro **/crosssession**.|
    |[/waitstart](../profiling/waitstart.md)[**:**`Interval`]|Určuje počet sekund pro čekání profileru k chybě při inicializaci předtím, než vrátí chybu. Pokud `Interval` není zadán, profileru čeká neomezenou dobu zaseknout. Ve výchozím nastavení **/start** vrátí okamžitě.|
    |[/globaloff](../profiling/globalon-and-globaloff.md)|Spuštění profileru se shromažďování dat pozastavena, přidejte **/globaloff** možnost k **/start** příkazového řádku. Použití **/globalon** obnovit profilace.|
    |[/ Čítač](../profiling/counter.md) **:** `Config`|Shromažďuje informace z čítače zadaný v konfiguračním výkon procesoru. Informace o čítači se přidá na data shromažďovaná v každé profilování události.|
    |[/wincounter](../profiling/wincounter.md) **:** `WinCounterPath`|Určuje čítačů výkonu systému Windows, které se mají shromažďovat při vytváření profilu.|
    |[/automark](../profiling/automark.md) **:** `Interval`|Použití s **/wincounter** pouze. Určuje počet milisekund, po mezi události kolekce čítače výkonu systému Windows. Výchozí hodnota je 500 ms.|
    |[/Events](../profiling/events-vsperfcmd.md) **:** `Config`|Určuje událost trasování událostí pro Windows (ETW), které se mají shromažďovat při vytváření profilu. Události trasování událostí se shromažďují v samostatné (. *ETL*) souboru.|

8. Spusťte službu z modulu snap-in Správce řízení služeb systému Windows.

## <a name="control-data-collection"></a>Řízení shromažďování dat

Pokud je služba spuštěná, můžete použít *VSPerfCmd.exe* možnosti spuštění a zastavení zápisu dat do datového souboru profileru. Řízení shromažďování dat umožňuje shromažďování dat pro konkrétní součást spuštění programu, například spuštění nebo vypnutí služby.

- Následující dvojice **VSPerfCmd** možnosti spuštění a zastavení shromažďování dat. Zadejte jednotlivé možnosti na samostatném řádku příkaz. Shromažďování dat můžete zapnout a vypnout vícekrát.

    |Možnost|Popis|
    |------------|-----------------|
    |[/globalon /globaloff](../profiling/globalon-and-globaloff.md)|Spustí (**/globalon**) nebo zastaví (**/globaloff**) shromažďování dat pro všechny procesy.|
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Spustí (**/processon**) nebo zastaví (**/processoff**) shromažďování dat pro proces zadaný pomocí ID procesu (`PID`).|
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|Spustí (**/threadon**) nebo zastaví (**/threadoff**) shromažďování dat pro vlákno určeného ID vlákna (`TID`).|

## <a name="end-the-profiling-session"></a>Ukončení relace profilování

K ukončení relace profilování, zastavte službu, která běží komponentu instrumentované a pak zavolají **VSPerfCmd** [/Shutdown](../profiling/shutdown.md) možnost vypnout profileru a zavřete profilování datového souboru. **Vsperfclrenv – /globaloff** příkaz vymaže profilování proměnné prostředí.

Musíte restartovat počítač pro použití nového nastavení prostředí.

1. Zastavte službu ze Správce řízení služeb.

2. Vypněte profileru. Typ:

     **Vsperfcmd – Shutdown**

3. Po dokončení všech profilace zrušte profilování proměnné prostředí. Typ:

     **Vsperfclrenv – /globaloff**

4. Modul instrumentovaného nahraďte původní. V případě potřeby znovu nakonfigurujte typ spouštění služby.

5. Restartujte počítač.

## <a name="see-also"></a>Viz také:

[Profil služby](../profiling/command-line-profiling-of-services.md)  
[Zobrazení dat metody instrumentace](../profiling/instrumentation-method-data-views.md)
