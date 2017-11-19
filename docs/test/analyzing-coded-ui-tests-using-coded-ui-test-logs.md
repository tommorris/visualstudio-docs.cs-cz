---
title: "Analýza programových testů uživatelského rozhraní pomocí protokolů z těchto testů | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-test
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 7e795873-1d4b-4a13-a52a-a411d87fb759
caps.latest.revision: "13"
ms.author: douge
manager: douge
ms.openlocfilehash: 39ed1ba397fd1c0a9ff1f30acea1cff4a38529a2
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="analyzing-coded-ui-tests-using-coded-ui-test-logs"></a>Analýza programových testů uživatelského rozhraní pomocí protokolů z těchto testů
Programových filtru protokoly testu uživatelského rozhraní a záznam, který spouští důležité informace o vaší programového testu uživatelského rozhraní.  
  
 **Požadavky**  
  
-   Visual Studio Enterprise  
  
## <a name="why-should-i-do-this"></a>Proč to mám udělat?  
 Protokoly jsou uvedené ve formátu, který umožňuje rychle ladění problémů.  
  
## <a name="how-do-i-do-this"></a>Jak to dělat?  
  
### <a name="step-1-enable-logging"></a>Krok 1: Povolení protokolování  
 V závislosti na scénáři Povolte protokol pomocí jedné z následujících metod.  
  
-   Cílové verze rozhraní .NET Framework 4 se nacházejí v projektu testovací soubor App.config  
  
    -   Otevřete **QTAgent32_40.exe.config** souboru.  
  
         Ve výchozím nastavení je tento soubor umístěný ve  **\<drvie >: \Program soubory (x86) \Microsoft Visual Studio 12.0\Common7\IDE**.  
  
         Změňte hodnotu pro EqtTraceLevel na požadovanou úroveň protokolu.  
  
         Uložte soubor.  
  
-   Cílové verze rozhraní .NET Framework 4.5 se nacházejí v projektu testovací soubor App.config  
  
    -   Otevřete **QTAgent32.exe.config** souboru.  
  
         Ve výchozím nastavení je tento soubor umístěný ve  **\<drvie >: \Program soubory (x86) \Microsoft Visual Studio 12.0\Common7\IDE**.  
  
         Změníte hodnotu EqtTraceLevel na požadovanou úroveň protokolu.  
  
         Uložte soubor.  
  
-   Soubor App.config nacházejí v projektu testu  
  
    -   Otevřete soubor App.config v projektu.  
  
         Přidejte následující kód v uzlu Konfigurace:  
  
         `<system.diagnostics>     <switches>       <add name="EqtTraceLevel" value="4" />     </switches>  </system.diagnostics>`  
  
-   Povolit protokolování z samotný kód testu  
  
    -   <xref:Microsoft.VisualStudio.TestTools.UITesting.PlaybackSettings.LoggerOverrideState%2A>= HtmlLoggerState.AllActionSnapshot;  
  
### <a name="step-2-run-your-coded-ui-test-and-view-the-log"></a>Krok 2: Spuštění vaší programového testu uživatelského rozhraní a zobrazit protokol  
 Při spuštění programového testu uživatelského rozhraní se změny **QTAgent32.exe.config** soubor v místě, se zobrazí ve výsledcích testování Explorer je odkaz na výstup. Soubory protokolu se produkují, ne jenom v případě, test nezdaří, ale i pro úspěšné testů, pokud je úroveň trasování nastavena na "verbose."  
  
1.  Na **TEST** nabídce zvolte **Windows** a pak vyberte **Průzkumníka testů**.  
  
2.  Na **sestavení** nabídce zvolte **sestavit řešení**.  
  
3.  V Průzkumníku testování vyberte programového testu UI chcete spouštět, otevřete jeho místní nabídce a potom zvolte **spuštění testů vyberte**.  
  
     Automatizované testy budou spuštěny a pokud předaná nebo se nezdařilo.  
  
    > [!TIP]
    >  K zobrazení Průzkumníka testů z **testovací nabídky**, přejděte na příkaz **Windows** a potom zvolte **Průzkumníka testů**.  
  
4.  Vyberte **výstup** odkaz ve výsledcích Průzkumníka testů.  
  
     ![Výstup odkaz v Průzkumníka testů](../test/media/cuit_htmlactionlog1.png "CUIT_HTMLActionLog1")  
  
     Zobrazí se výstup pro test, který bude obsahovat odkaz na protokol akcí.  
  
     ![Výsledky a odkazy na výstup z programového testu uživatelského rozhraní](../test/media/cuit_htmlactionlog2.png "CUIT_HTMLActionLog2")  
  
5.  Vyberte odkaz UITestActionLog.html.  
  
     Protokol se zobrazí ve webovém prohlížeči.  
  
     ![Programové uživatelského rozhraní testovací soubor protokolu](../test/media/cuit_htmlactionlog3.png "CUIT_HTMLActionLog3")  
  
## <a name="q--a"></a>Dotazy a odpovědi  
  
### <a name="q-what-happened-to-the-enablehtmllogger-key"></a>Otázka: co se stalo s EnableHtmlLogger klíč?  
 V předchozích verzích sady Visual Studio nebyly dva další nastavení konfigurace pro povolení protokoly ve formátu Html v programového testu uživatelského rozhraní:  
  
```  
  
<add key="EnableHtmlLogger" value="true"/>  
  
<add key="EnableSnapshotInfo" value="true"/>  
  
```  
  
 Obě tato nastavení jsou zastaralé od verze sady Visual Studio 2012. EqtTraceLevel je jenom nastavení, které je potřeba upravit tak, aby povolit HtmlLogger.  
  
## <a name="see-also"></a>Viz také  
 [Použití automatizace uživatelského rozhraní k testování kódu](../test/use-ui-automation-to-test-your-code.md)   
 [Postupy: spouštění testů ze sady Microsoft Visual Studio](http://msdn.microsoft.com/Library/1a1207a9-2a33-4a1e-a1e3-ddf0181b1046)