---
title: "Port, migrace a Upgrade projektů sady Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 01/04/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- Win8ExpressDesktopBlock
- w8trefactor
- VS.ReviewProjectAndSolutionChangesDialog.UpgradeRetarget
- ProjectCompatibilityDlgHelpTopic
- VS.ReviewProjectAndSolutionChangesDialog.Upgrade
helpviewer_keywords:
- conversion, projects
- asset compatibility
- projects, conversion
author: kraigb
ms.author: kraigb
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: b47bcd95e19245ee09d4aeca16146ab415f7d896
ms.sourcegitcommit: 5f436413bbb1e8aa18231eb5af210e7595401aa6
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/08/2018
---
# <a name="port-migrate-and-upgrade-visual-studio-projects"></a>Port, migrace a Upgrade projektů sady Visual Studio

Každá nová verze sady Visual Studio obecně podporuje většinu typů předchozí projekty, soubory a dalších prostředků. Můžete pracovat s nimi [jako budete mít vždy](../ide/solutions-and-projects-in-visual-studio.md), a za předpokladu, že nemáte závisí na novější funkce, Visual Studio zachovává zpětné kompatibility s předchozími verzemi jako Visual Studio 2015, Visual Studio 2013 a Visual Studio 2012. (Viz [poznámky k verzi](https://www.visualstudio.com/vs/release-notes/) pro funkce, které jsou specifické pro jaké verze.)

Podpora pro některé typy změny projektu v čase, ale. Novější verze sady Visual Studio může už nepodporuje některé typy nebo vyžadovat, aby se migrovat a aktualizovat tak, že už jsou zpětně kompatibilní. Aktuální stav na problémy s migrací, najdete v části [webu Visual Studio Community vývojáře](https://developercommunity.visualstudio.com).

> [!Important]
> Tento článek existuje poskytuje podrobnosti pouze pro typy projektů ve Visual Studio 2017, které zahrnují migraci. Nezahrnuje typy podporované projektů, které mají žádné problémy migrace; Tento seznam se nachází na [cílení a kompatibilita platformy](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs). Všimněte si také, že některé typy projektů již nejsou podporovány v aplikaci Visual Studio 2017 vůbec a proto se nedají migrovat.

> [!Important]
> Přidání příslušné úlohy v sadě Visual Studio je nutné pro otevření určité typy projektů Instalační služby. Pokud nemáte zatížení nainstalovaná, Visual Studio nahlásí typ projektu neznámý nebo není kompatibilní. V takovém případě zkontrolujte možnosti instalace a zkuste to znovu. Znovu, najdete v článku [cílení a kompatibilita platformy](https://www.visualstudio.com/productinfo/vs2017-compatibility-vs) článku informace o podporovaných projektu ve Visual Studio 2017.

## <a name="projects"></a>Projekty

Následující seznam popisuje podporu v Visual Studio 2017 pro projekty, které byly vytvořeny v dřívějších verzích.

Pokud nevidíte projektu nebo typ souboru tady, by měl být, najdete [Visual Studio 2015 verzi tohoto článku](https://msdn.microsoft.com/library/hh266747.aspx) a pomocí možnosti "Názor dokumentace" v dolní části této stránky můžete zadat podrobnosti o projektu.

| Typ projektu | Podpora |
| --- | --- |
| Projekty .NET core (.xproj) | Projekty vytvořené pomocí sady Visual Studio 2015 používá preview nástrojů, který zahrnut soubor projektu .xproj. Při otevření souboru .xproj s Visual Studio 2017, zobrazí se výzva k migraci souboru .csproj formátu (záloha souboru .xproj přišla). Tento formát .csproj projektů .NET Core není podporována v VS2015 a starší.  Formát .xproj není podporovaný v aplikaci Visual Studio 2017 jinak než při migraci do .csproj. Další informace najdete v tématu [migrace .NET Core projekty do formátu .csproj](/dotnet/core/migration/#visual-studio-2017).|
| Webové aplikace ASP.NET a základní webové aplikace ASP.NET pomocí Application Insights povoleno | Pro každého uživatele, Visual Studio informace o prostředku je uložen v registru na uživatelskou instanci. To se používá, když uživatel není t projektu otevřít a chce vyhledávání dat Azure Application Insights. Visual Studio 2015 používá umístění v registru jiné než Visual Studio 2017 a nedošlo ke konfliktu.<br/><br/>Jakmile uživatel vytvoří webovou aplikaci ASP.NET nebo webové aplikace ASP.NET Core, uloží se prostředek do v souboru .suo. Uživatel může otevřete projekt v sadě Visual Studio 2015 nebo 2017 a informace o prostředcích se používá pro obě sady Visual Studio podporuje projekty a řešení používá napříč obě verze. Uživatelé musí ověřit jednou pro každý produkt. Například pokud projektu vytvořené pomocí sady Visual Studio 2015 a otevřít v aplikaci Visual Studio 2017, uživatel se musí ověřit na Visual Studio 2017. |
| Webový formulář nebo formulář Windows v jazyce C# nebo Visual Basic | Projekt můžete otevřít ve Visual Studio 2017 a Visual Studio 2015. |
| Databáze projektů testování částí (.csproj, .vbproj) | Starší datová jednotka projektů testů jsou načtena v Visual Studio 2017 ale použít GAC'd verzi závislostí. Upgrade projektu testů jednotek používat nejnovější závislosti, klikněte pravým tlačítkem na projekt v Průzkumníku řešení a vyberte **převést na projekt testování částí SQL Server...** . |
| F# | Visual Studio 2017 můžete otevřít projektů vytvořených v sadě Visual Studio 2013 a 2015. K povolení funkce Visual Studio 2017 v těchto projektech, ale, otevřete vlastnosti projektu a změnit cíl fsharp.core 4.1 F #. Všimněte si také, že **podporu jazyka F #** není vybraná možnost v instalačním programu sady Visual Studio ve výchozím nastavení s úlohami .NET; je nutné zahrnout vyberete tuto možnost pro úlohy, nebo výběrem z  **Jednotlivé komponenty** v části **vývoj aktivity**. |
| InstallShield<br/>Instalační program MSI | Instalační program projektů vytvořených v sadě Visual Studio 2010 lze otevřít v novějších verzích pomocí [rozšíření projektů Instalační program sady Visual Studio](https://marketplace.visualstudio.com/items?itemName=UnniRavindranathan-MSFT.MicrosoftVisualStudio2013InstallerProjects). Viz také [WiX Toolset 2017 rozšíření sady Visual Studio](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension). InstallShield Limited Edition je už součástí sady Visual Studio. Obraťte se na [Flexera softwaru](http://learn.flexerasoftware.com/content/IS-EVAL-InstallShield-Limited-Edition-Visual-Studio) o dostupnosti pro Visual Studio 2017. |
| LightSwitch | LightSwitch již není podporována v Visual Studio 2017. Projekty vytvořené pomocí sady Visual Studio 2012 a starších otevřít v sadě Visual Studio 2013 nebo Visual Studio 2015 upgradují a lze je po tomto datu otevřít pouze v sadě Visual Studio 2013 nebo Visual Studio 2015. |
| Nástroje Microsoft Azure pro sadu Visual Studio | Chcete-li otevřít tyto typy projektů, nejprve nainstalovat [Azure SDK for .NET](http://azure.microsoft.com/downloads/), otevřete projekt. V případě potřeby se aktualizuje projektu. |
| Framework Model-View-Controller (ASP.NET MVC) | Podpora pro verze MVC a Visual Studio:<ul><li>Visual Studio 2010 SP1 podporuje MVC 2 a MVC 3; Prostřednictvím je přidána podpora MVC 4 [ASP.NET 4 MVC 4 ke stažení pro Visual Studio 2010 SP1](https://www.microsoft.com/download/details.aspx?id=30683)</li><li>Visual Studio 2012 podporuje jenom MVC 3 a MVC 4</li><li>Visual Studio 2013 podporuje jenom MVC 4 a MVC 5</li><li>Visual Studio 2017 a Visual Studio 2015 podporuje MVC 4 (můžete otevřít stávající projekty ale není vytvořit nové) a MVC 5</li></ul><br/><br/>Upgrade MVC verzí:<ul><li>Informace o tom, jak automaticky upgradovat z MVC 2 MVC 3 najdete v tématu [ASP.NET MVC 3 aplikace Upgrader](http://go.microsoft.com/fwlink/?LinkID=238178).</li><li>Informace o tom, jak ručně upgradovat z MVC 2 na MVC 3 najdete v tématu [upgrade projektu ASP.NET MVC 2 na ASP.NET MVC 3 nástroje aktualizace](http://go.microsoft.com/fwlink/?linkid=238178).</li><li>Informace o tom, jak ručně upgradovat z MVC3 na MVC 4 najdete v tématu [upgrade projektu ASP.NET MVC 3, ASP.NET MVC 4](http://www.asp.net/whitepapers/mvc4-release-notes). Pokud je cílem vašeho projektu je .NET Framework 3.5 SP1, musíte změnit cílový ho na použití rozhraní .NET Framework 4.</li><li>Informace o tom, jak ručně upgradovat z MVC 4 na MVC 5 najdete v tématu [postup upgradu služby ASP.NET MVC 4 a projekt webového rozhraní API ASP.NET MVC 5 a webovém rozhraní API 2](https://www.asp.net/mvc/overview/releases/how-to-upgrade-an-aspnet-mvc-4-and-web-api-project-to-aspnet-mvc-5-and-web-api-2)</li></ul> |
| Modelování | Pokud chcete automaticky aktualizovat projekt Visual Studio povolíte, můžete ho otevřít v sadě Visual Studio 2015, Visual Studio 2013 nebo Visual Studio 2012.<br/><br/>Formát projektem modelování nezměnil mezi Visual Studio 2015 a Visual Studio 2017 a projekt můžete otevřít a upravit v kterékoli verzi. Existují však rozdíly v chování v aplikaci Visual Studio 2017:<ul><li>Projekty modelování se nyní označuje jako "Závislosti ověření" projekty v nabídkách a šablony.</li><li>Diagramy UML již nejsou podporovány v aplikaci Visual Studio 2017. UML soubory jsou uvedeny v Průzkumníku řešení jako před, ale jsou otevřené jako soubory XML. Zobrazit, vytvořit nebo upravit diagramů UML pomocí sady Visual Studio 2015.</li><li>V aplikaci Visual Studio 2017 architektury závislosti se už provádí ověřování při sestavení projektu modelování. Místo toho jak sestavení každého projektu kódu se provádí ověření. Tato změna nemá vliv na projektem modelování, ale nevyžaduje změny kódu projektů ověřován. Visual Studio 2017 můžete automaticky proveďte potřebné změny k projektům kódu ([informace](http://go.microsoft.com/fwlink/?LinkId=827800)).</li></ul> |
| Instalační program MSI (.vdproj) | Zobrazit projekty InstallShield výše. | 
| Sada Office 2007 VSTO | Jednosměrné upgrade vyžaduje pro Visual Studio 2017. |
| Office 2010 VSTO | Pokud projekt cílí na rozhraní .NET Framework 4, můžete ho otevřít v sadě Visual Studio 2010 SP1 nebo novější. Všechny ostatní projekty vyžadují jednosměrnou aktualizaci. |
| SharePoint 2010 | Po otevření projektu řešení služby SharePoint s Visual Studio 2017 bude inovována na SharePoint 2013 nebo SharePoint 2016. "Desktop .NET – vývoj" zatížení musí být nainstalován v Visual Studio 2017 pro upgrade.<br/><br/>Další informace o tom, jak upgradovat projektů služby SharePoint, naleznete v části [upgradovat na SharePoint 2013](https://technet.microsoft.com/library/cc303420.aspx), [pracovního postupu aktualizací v SharePoint Server 2013](https://technet.microsoft.com/library/dn133867.aspx), a [vytvořit farmu služby SharePoint Server 2016 pro databázi připojte upgradu](https://technet.microsoft.com/library/cc263026(v=office.16).aspx). |
| SharePoint 2016 | Add-In služby SharePoint projektů vytvořených v Office Developer Tools Preview 2 nelze otevřít ve Visual Studio 2017. Toto omezení obejít, aktualizujte `MinimumVisualStudioVersion` k 12.0 a `MinimumOfficeToolsVersion` k 12.2 v `.csproj` nebo `.vbproj` souboru. |
| Silverlight | V Visual Studio 2017 nepodporuje projekty Silverlight. Chcete-li udržovat aplikace Silverlight, používejte nadále Visual Studio 2015. |
| SQL Server Reporting Services a SQL Server Analysis Services (SSRS, rozšíření SSDT, SSAS, účty spravované služby) | Pro tyto typy projektů je poskytována prostřednictvím podpory dvě rozšíření v Galerii Visual Studio: [projekty modelování služby Microsoft Analysis Services](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftAnalysisServicesModelingProjects) a [Microsoft Reporting Services projekty](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftReportProjectsforVisualStudio). Podpora rozšíření SSDT je také součástí úložiště dat a zpracování úloh ve Visual Studio 2017. |
| SQL Server Integration Services (služby SSIS) | Podpora pro Visual Studio 2017 je k dispozici prostřednictvím SQL Server Data Tools (SSDT). Další informace najdete v tématu [SQL Server Integration Services blog](https://blogs.msdn.microsoft.com/ssis/2017/08/23/ssis-designer-is-now-available-for-visual-studio-2017/). |
| Visual C++ | Visual Studio 2017 můžete otevřít řešení a projekty, které byly vytvořeny ve Visual Studiu 2015 jako-je. Projekty vytvořené v starší verze sady Visual Studio může vyžadovat upgrade projektu nebo změna orientace na novější nástrojů k sestavení s Visual Studio 2017. Další informace najdete v tématu [průvodce Visual C++ přenosem a upgradováním](https://docs.microsoft.com/cpp/porting/visual-cpp-porting-and-upgrading-guide). |
| Rozšíření sady Visual Studio nebo VSIX | Deklarovat 15.0 MinimumVersion, což zabrání projektu otevíráte ve starších verzích sady Visual Studio se aktualizují projektů s MinimumVersion 14.0 nebo méně. Chcete-li povolit projektu otevřete v dřívějších verzích, nastavte MinimumVersion `$(VisualStudioVersion)`. Viz také [postup: migrace rozšiřitelnost projektů na Visual Studio 2017](../extensibility/how-to-migrate-extensibility-projects-to-visual-studio-2017.md). |
| Visual Studio Lab Management | Můžete použít nástroje Microsoft Test Manager nebo Visual Studio 2010 SP1 a novější otevřete prostředí vytvořena v některém z těchto verzí. Ale pro Visual Studio 2010 SP1 na verzi nástroje Microsoft Test Manager musí shodovat s verzí produktu Team Foundation Server před vytvořením prostředí. |
| Visual Studio Tools pro Apache Cordova | Projekty můžete otevřít ve Visual Studio 2017, ale nejsou zpětně kompatibilní. Po otevření projektu ze sady Visual Studio 2015, se zobrazí výzva k povolení úprav do projektu. Tato úprava upgraduje projekt, který používá modulové místo `taco.json` souboru ke správě verzí knihovně Cordova, jeho platformy a modulů plug-in, jakož i jeho závislé součásti uzlu nebo npm. Najdete v článku [příručka k migraci](https://docs.microsoft.com/visualstudio/cross-platform/tools-for-cordova/first-steps/migrate-from-visual-studio-2015) Další informace. |
| Windows Communication Foundation modelu Windows Workflow Foundation | Tento projekt můžete otevřít ve Visual Studio 2017, Visual Studio 2015, Visual Studio 2013 a Visual Studio 2012 |
| Windows Presentation Foundation | Tento projekt můžete otevřít v sadě Visual Studio 2013, Visual Studio 2012 a Visual Studio 2010 SP1. |
| Windows Store, telefonní aplikace | Visual Studio 2017 nepodporuje projekty pro Windows Store 8.1 a 8.0 a Windows Phone 8.1 a 8.0. Chcete-li tyto aplikace udržovat, používejte nadále Visual Studio 2015. Chcete-li udržovat projekty pro Windows Phone 7.x, používejte Visual Studio 2012. |