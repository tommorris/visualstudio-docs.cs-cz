---
title: 'Postupy: instrumentace dynamicky kompilované ASP.NET – webové aplikaci a shromažďování dat paměti pomocí příkazového řádku profileru | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 2cdd9903-39db-47e8-93dd-5e6a21bc3435
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- aspnet
ms.openlocfilehash: 6ef538ac7316375b14dcbd951d5cf89702cdde0e
ms.sourcegitcommit: 1b9c1e333c2f096d35cfc77e846116f8e5054557
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/06/2018
ms.locfileid: "34815584"
---
# <a name="how-to-instrument-a-dynamically-compiled-aspnet-web-application-and-collect-memory-data-by-using-the-profiler-command-line"></a>Postupy: instrumentace dynamicky kompilované webové aplikace ASP.NET a shromažďování dat paměti pomocí příkazového řádku profileru
Toto téma popisuje postup použití [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profilace nástroje příkazového řádku nástroje ke shromažďování podrobné data paměti .NET přidělení a objekt doba platnosti pro dynamicky kompilované [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] webovou aplikaci pomocí metoda profilování instrumentace.  
  
> [!NOTE]
>  Nástroje příkazového řádku nástroje profilace jsou umístěné v *\Team Tools\Performance nástroje* podadresáři [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] instalační adresář. Na 64bitových počítačích 64bitové a 32bitové verze nástroje jsou k dispozici. Chcete-li použít nástroje příkazového řádku profileru, musí přidat cestu nástroje do proměnné prostředí PATH okna příkazového řádku nebo ho přidat do samotný příkaz. Další informace najdete v tématu [zadejte cestu k nástroje příkazového řádku](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
  
 Ke shromažďování dat výkonu z [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] webové aplikace, můžete změnit *web.config* souboru cílová aplikace povolit [VSInstr.exe](../profiling/vsinstr.md) nástroj, který instrumentace dynamicky kompilované soubory aplikace. Pak použijete [VSPerfCLREnv.cmd](../profiling/vsperfclrenv.md) nástroj pro konfiguraci serveru, který je hostitelem [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] webovou aplikaci a povolit .NET profilace paměti nastavením příslušné proměnné prostředí a pak restartujte počítač.  
  
 Ke shromažďování dat, spusťte profileru a pak spusťte cílová aplikace. Při profileru je připojen k aplikaci, můžete pozastavit a obnovit data kolekce. Když máte shromažďována příslušná data, zavře se aplikace, zavřete pracovního procesu Internetové informační služby (IIS) a poté vypněte profileru.  
  
 Po dokončení profilování práci obnovit *web.config* souborový a webový server do původního stavu.  
  
## <a name="configure-the-aspnet-web-application-and-the-web-server"></a>Konfigurace webové aplikace ASP.NET a webový server  
  
#### <a name="to-configure-the-aspnet-web-application-and-the-web-server"></a>Konfigurace webové aplikace ASP.NET a webový server  

1.  Změnit *web.config* souboru cílová aplikace. V tématu [postupy: Úprava souborů web.config a instrumentace dynamicky kompilované webové aplikace ASP.NET profilu](../profiling/how-to-modify-web-config-files-to-instrument-dynamically-compiled-aspnet-apps.md).  
  
2.  Otevřete okno příkazového řádku na počítači, který je hostitelem webové aplikace.  
  
3.  Inicializujte profilování proměnné prostředí. Typ:  
  
     **Vsperfclrenv – /globaltracegc**  
  
     -nebo-  
  
     **Vsperfclrenv – /globaltracegclife**  
  
    -   **/globaltracegc** umožňuje shromažďování dat o přidělení paměti.  
  
    -   **/globaltracegclife** umožňuje shromažďování dat přidělování paměti a životnosti objektů.  
  
4.  Restartujte počítač.  
  
## <a name="run-the-profiling-session"></a>Spuštění relace profilování  
  
#### <a name="to-profile-the-aspnet-web-application"></a>Do profilu webové aplikace ASP.NET  
  
1.  Spusťte profileru. Typ:  
  
     **VSPerfCmd** [/start](../profiling/start.md) **: trasování** [/výstup](../profiling/output.md) **:** `OutputFile` [`Options`]  
  
    -   **/Start:trace** možnost inicializuje profileru.  
  
    -   **/Výstup:** `OutputFile` možnost je povinná s **/start**. `OutputFile` Určuje název a umístění data profilování (. *Vsp*) souboru.  
  
     Můžete použít některou z následujících možností s **/start:trace** možnost.  
  
    > [!NOTE]
    >  **User** a **/crosssession** možnosti jsou obvykle vyžaduje pro aplikace ASP.NET.  
  
    |Možnost|Popis|  
    |------------|-----------------|  
    |[Parametr/User](../profiling/user-vsperfcmd.md) **:**[`Domain`**\\**]`UserName`|Určuje nepovinné doména a uživatelské jméno účtu, který vlastní [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] pracovní proces. Tato možnost je povinná, pokud je proces spuštěný jako uživatel, než je přihlášený uživatel. Název je uveden v **uživatelské jméno** sloupec **procesy** karty Správce úloh systému Windows.|  
    |[/crosssession](../profiling/crosssession.md)|Umožňuje profilace procesů v jiných relacích. Tato možnost je povinná, pokud je aplikace spuštěna v jiné relaci. ID je uvedena v relaci **ID relace** sloupce v **procesy** karty Správce úloh systému Windows. **/CS** lze zadat jako zkratkou pro **/crosssession**.|  
    |[/globaloff](../profiling/globalon-and-globaloff.md)|Spuštění, které profileru se shromažďováním dat. pozastavena. Použití [/globalon](../profiling/globalon-and-globaloff.md) obnovit profilace.|  
    |[/ Čítač](../profiling/counter.md) **:** `Config`|Shromažďuje informace z výkon procesoru čítač zadaný v `Config`. Informace o čítači se přidá na data shromažďovaná v každé profilování události.|  
    |[/wincounter](../profiling/wincounter.md) **:** `WinCounterPath`|Určuje čítačů výkonu systému Windows, které se mají shromažďovat při vytváření profilu.|  
    |[/automark](../profiling/automark.md) **:** `Interval`|Použití s **/wincounter** pouze. Určuje počet milisekund, po mezi události kolekce čítače výkonu systému Windows. Výchozí hodnota je 500 ms.|  
    |[/Events](../profiling/events-vsperfcmd.md) **:** `Config`|Určuje událost trasování událostí pro Windows (ETW), které se mají shromažďovat při vytváření profilu. Události trasování událostí se shromažďují v samostatné (. *ETL*) souboru.|  
  
2.  Spuštění [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] webové aplikace v obvyklým způsobem.  
  
## <a name="control-data-collection"></a>Řízení shromažďování dat  
 Když cílová aplikace běží, lze řídit shromažďování dat spuštění a zastavení zápisu dat do datového souboru profileru pomocí *VSPerfCmd.exe* možnosti. Řízení shromažďování dat umožňuje shromažďování dat pro konkrétní součást spuštění programu, jako je například spouštění nebo ukončením aplikace.  
  
#### <a name="to-start-and-stop-data-collection"></a>Spuštění a zastavení shromažďování dat  
  
-   Následující páry možnosti spuštění a zastavení shromažďování dat. Zadejte jednotlivé možnosti na samostatném řádku příkaz. Shromažďování dat můžete zapnout a vypnout vícekrát.  
  
    |Možnost|Popis|  
    |------------|-----------------|  
    |[/globalon /globaloff](../profiling/globalon-and-globaloff.md)|Spustí (**/globalon**) nebo zastaví (**/globaloff**) shromažďování dat pro všechny procesy.|  
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Spustí (**/processon**) nebo zastaví (**/processoff**) shromažďování dat pro proces zadaný pomocí ID procesu (`PID`).|  
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|Spustí (**/threadon**) nebo zastaví (**/threadoff**) shromažďování dat pro vlákno určeného ID vlákna (`TID`).|  
  
-   Můžete také **VSPerfCmd.exe**[/označit](../profiling/mark.md) možnost vložit do datového souboru profilování značky. **/Označit** příkaz přidá identifikátor časovým razítkem a volitelné uživatelem definované textový řetězec. Značky lze použít k filtrování dat v zobrazení dat a sestav profileru.  
  
## <a name="end-the-profiling-session"></a>Ukončení relace profilování  
 K ukončení relace profilování, zavřete cíl [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] webovou aplikaci, zastavte Internetové informační služby (IIS) při ukončení procesu PROFILOVANÉHO a poté vypněte profileru. Potom restartujte službu IIS.  
  
#### <a name="to-end-a-profiling-session"></a>K ukončení relace profilování  
  
1.  Zavřít [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] webové aplikace.  
  
2.  Zavřít [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] pracovní proces resetováním Internetové informační služby (IIS). Typ:  
  
     **Příkaz IISReset/stop**  
  
3.  Vypněte profileru. Typ:  
  
     **VSPerfCmd**  [ /Shutdown](../profiling/shutdown.md)  
  
4.  Restartujte službu IIS. Typ:  
  
     **Příkaz IISReset/Start**  
  
## <a name="restore-the-application-and-computer-configuration"></a>Obnovit konfiguraci aplikace a počítače  
 Po dokončení všech profilace nahradit *web.config* souboru, zrušte profilování proměnné prostředí a restartujte počítač k obnovení serveru a [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] aplikace do původního stavu.  
  
#### <a name="to-restore-the-application-and-computer-configuration"></a>Chcete-li obnovit konfiguraci aplikace a počítače  
  
1.  Nahraďte *web.config* soubor s kopií původního souboru.  
  
2.  (Volitelné). Zrušte profilování proměnné prostředí. Typ:  
  
     **Vsperfcmd – /globaloff**  
  
3.  Restartujte počítač.  
  
## <a name="see-also"></a>Viz také:  
 [Webové aplikace ASP.NET profilu](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Zobrazení dat paměti .NET](../profiling/dotnet-memory-data-views.md)
