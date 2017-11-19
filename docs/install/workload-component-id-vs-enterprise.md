---
title: "ID úlohy a součást Visual Studio Enterprise 2017 | Microsoft Docs"
description: "Pomocí úloh a ID součástí k instalaci sady Visual Studio pomocí příkazového řádku nebo zadejte v závislosti na manifestu VSIX"
keywords: 
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.date: 10/09/2017
ms.topic: article
helpviewer_keywords:
- workload ID, Visual Studio
- component ID, Visual Studio
- install Visual Studio, administrator guide
ms.service: 
ms.technology:
- vs-ide-install
- vs-ide-sdk
ms.assetid: be73e3af-d87b-4d14-bd08-2e4bda074fb3
ms.openlocfilehash: b11905fd449e4f58b0c2f6525c9674b9c7aded3b
ms.sourcegitcommit: 2c7f48ad6073a81fa927568793633f26cc1f0b15
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2017
---
# <a name="visual-studio-enterprise-2017-component-directory"></a>Visual Studio Enterprise 2017 součástí adresáře

Tabulky v tomto seznamu stránky ID, můžete použít k instalaci sady Visual Studio pomocí příkazového řádku nebo je můžete zadat v závislosti na manifestu VSIX. Všimněte si, že přidáme další součásti, jako jsme vydání aktualizace pro Visual Studio.

Všimněte si také následující stránka:

* Každé zatížení má vlastní části, a potom podle ID úlohy a tabulku součásti, které jsou k dispozici pro pracovní vytížení.
* Ve výchozím nastavení **požadované** součásti se nainstalují při instalaci zatížení.
* Pokud zvolíte možnost, můžete taky nainstalovat **doporučeno** a **volitelné** součásti.
* Přidali jsme také oddíl, který uvádí další součásti, které nejsou spojit s jakoukoli úlohu.

Když nastavíte závislosti v manifestu VSIX, je nutné zadat ID součástí pouze. K určení závislostí naše minimální součástí použijte tabulky na této stránce. V některých případech to může znamenat, že zadáváte pouze jedna součást z pracovního vytížení. V jiných scénářích může znamenat, že zadáváte více součástí z jediné úlohy nebo více součástí z více úloh. Další informace najdete v tématu [postup: migrace rozšiřitelnost projektů pro Visual Studio 2017](../extensibility/how-to-migrate-extensibility-projects-to-visual-studio-2017.md) stránky.

Další informace o tom, jak používat tyto identifikátory najdete v tématu [pomocí parametrů příkazového řádku pro instalaci Visual Studio 2017](use-command-line-parameters-to-install-visual-studio.md) stránky. A seznam úloh a ID součástí pro ostatní produkty, naleznete v části [zatížení 2017 Visual Studio a ID součástí](workload-and-component-ids.md) stránky.

## <a name="visual-studio-core-editor-included-with-visual-studio-enterprise-2017"></a>Visual Studio základní editor (je součástí Visual Studio Enterprise 2017)

**ID:** Microsoft.VisualStudio.Workload.CoreEditor

**Popis:** prostředí prostředí sady Visual Studio jádra, včetně syntaxe využívající kód úpravy, pro řízení zdrojového kódu a pracovní položky správy.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.VisualStudio.Component.CoreEditor | Editor základní Visual Studio | 15.0.26606.0 | Požadováno


## <a name="azure-development"></a>Vývoj pro Azure

**ID:** Microsoft.VisualStudio.Workload.Azure

**Popis:** Azure SDK, nástroje a projektů pro vývoj cloudové aplikace a vytváření prostředků.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Požadováno
Component.Microsoft.VisualStudio.Web.AzureFunctions | Nástroje Microsoft Azure WebJobs | 15.0.26720.2 | Požadováno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Požadováno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Požadováno
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Požadováno
Microsoft.Component.NetFX.Core.Runtime | .NET core runtime | 15.0.26208.0 | Požadováno
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Požadováno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Požadováno
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Požadováno
Microsoft.Net.Core.Component.SDK | Nástroje pro vývoj 1.0 1.1 základní rozhraní .NET | 15.0.26606.0 | Požadováno
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Požadováno
Microsoft.NetCore.ComponentGroup.Web | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Požadováno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Nástroje pro tvorbu Azure | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.Azure.ClientLibs | Knihovny Azure pro .NET | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulátoru služby výpočty Azure | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulátor úložiště Azure | 15.0.26823.1 | Požadováno
Microsoft.VisualStudio.Component.Azure.Waverton | Základní nástroje Azure Cloud Services | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.CloudExplorer | Průzkumník cloudu | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Požadováno
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Požadováno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL runtime | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.CMDUtils | Nástroje příkazového řádku systému SQL Server | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.DataSources | Zdroje dat pro podporu systému SQL Server | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Požadováno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.Azure.Prerequisites | Požadavky na vývoj pro Azure | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Nástroje Microsoft Azure WebJobs | 15.0.26720.2 | Požadováno
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Požadováno
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake a Stream Analytics nástroje | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Azure.MobileAppsSdk | Azure SDK mobilní aplikace | 15.0.26504.0 | Doporučeno
Microsoft.VisualStudio.Component.Azure.ResourceManager.Tools | Základní nástroje Azure Resource Manager | 15.0.26906.1 | Doporučeno
Microsoft.VisualStudio.Component.Azure.ServiceFabric.Tools | Nástroje Service Fabricu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.Azure.CloudServices | Nástroje Azure Cloud Services | 15.0.26504.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.Azure.ResourceManager.Tools | Nástroje Azure Resource Manager | 15.0.26919.1 | Doporučeno
Microsoft.Net.Component.4.6.2.SDK | Rozhraní .NET framework 4.6.2 SDK | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.6.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.2 | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.7.SDK | Rozhraní .NET framework 4.7 SDK | 15.0.26419.1 | Nepovinné
Microsoft.Net.Component.4.7.TargetingPack | Rozhraní .NET framework 4.7 cílení pack | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | Nástroje pro vývoj rozhraní .NET framework 4.6.2 | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | Nástroje pro vývoj 4.7 rozhraní .NET framework | 15.0.26606.0 | Nepovinné
Microsoft.Net.Core.Component.SDK.1x | .NET core 1.0 1.1 vývojových nástrojů pro plochu | 15.0.26919.1 | Nepovinné
Microsoft.NetCore.1x.ComponentGroup.Web | .NET core 1.0 1.1 vývojových nástrojů pro Web | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.Azure.Storage.AzCopy | AzCopy úložiště Azure | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.PowerShell.Tools | Nástroje pro prostředí PowerShell | 3.0.552 | Nepovinné
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Nepovinné


## <a name="data-storage-and-processing"></a>Úložiště dat a zpracování

**ID:** Microsoft.VisualStudio.Workload.Data

**Popis:** připojit, vývoj a testování pomocí serveru SQL Azure Data Lake, Hadoop nebo Azure ML řešení data.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Component.Redgate.ReadyRoll | Redgate ReadyRoll Core | 1.14.2.3918 | Doporučeno
Component.Redgate.SQLPrompt.VsPackage | Redgate SQL Prompt Core | 8.0.2.1513 | Doporučeno
Component.Redgate.SQLSearch.VSExtension | Hledání v Redgate SQL | 2.4.2.1439 | Doporučeno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Doporučeno
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake a Stream Analytics nástroje | 15.0.26823.1 | Doporučeno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Doporučeno
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Doporučeno
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Doporučeno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Doporučeno
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Nástroje pro tvorbu Azure | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.ClientLibs | Knihovny Azure pro .NET | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulátoru služby výpočty Azure | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulátor úložiště Azure | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Waverton | Základní nástroje Azure Cloud Services | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.CloudExplorer | Průzkumník cloudu | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Doporučeno
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Doporučeno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL runtime | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CMDUtils | Nástroje příkazového řádku systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.DataSources | Zdroje dat pro podporu systému SQL Server | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.FSharp | Podpora jazyka F # | 15.0.26606.0 | Nepovinné


## <a name="data-science-and-analytical-applications"></a>Vědecké zpracování dat a analytických aplikací

**ID:** Microsoft.VisualStudio.Workload.DataScience

**Popis:** jazyky a nástrojů pro vytváření dat vědecké účely aplikací, včetně Python, R a F #.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Anaconda3.x64 | Anaconda3 64-bit (4.4.0) | 4.4.0 | Doporučeno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Microsoft.Component.CookiecutterTools | Podpora Cookiecutter šablony | 15.0.26621.2 | Doporučeno
Microsoft.Component.PythonTools | Podpora jazyka Python | 15.0.26823.1 | Doporučeno
Microsoft.Component.PythonTools.Web | Podpora webového Python | 15.0.26606.0 | Doporučeno
Microsoft.Component.VC.Runtime.UCRTSDK | Sady Windows Universal CRT SDK | 15.0.26208.0 | Doporučeno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Doporučeno
Microsoft.VisualStudio.Component.FSharp | Podpora jazyka F # | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.R.Open | Microsoft R klienta (3.3.2) | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.RHost | Podpora modulu runtime pro nástroje pro vývoj R | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.RTools | Podpora jazyka R | 15.0.26919.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Windows81SDK | Windows 8.1 SDK | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno
Component.Anaconda2.x64 | Anaconda2 64-bit (4.4.0) | 4.4.0 | Nepovinné
Component.Anaconda2.x86 | 32bitový Anaconda2 (4.4.0) | 4.4.0 | Nepovinné
Component.Anaconda3.x86 | 32bitový Anaconda3 (4.4.0) | 4.4.0 | Nepovinné
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Nástroje pro nativní vývoj Python | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.Component.Graphics.Tools | Ladicího programu grafiky a GPU profileru pro rozhraní DirectX | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafické nástroje Windows 8.1 SDK | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.140 | Sada nástrojů v140 VC ++ 2015.3 pro plochu (x86, x64) | 15.0.26720.2 | Nepovinné
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ nástroje pro profilaci | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK | Prostředí Windows Universal C Runtime | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) pro plochy C++ [x86 a x64] | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) pro UPW: C++ | 15.0.27004.2002 | Nepovinné


## <a name="net-desktop-development"></a>Vývoj aplikací rozhraní .NET

**ID:** Microsoft.VisualStudio.Workload.ManagedDesktop

**Popis:** sestavení WPF Windows Forms a konzolové aplikace pomocí jazyka C#, Visual Basic a F #.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Požadováno
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Požadováno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Požadováno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Debugger.JustInTime | Ladicí program za běhu | 15.0.26823.1 | Požadováno
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Požadováno
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | Nástroje pro vývoj aplikací rozhraní .NET | 15.0.26906.1 | Požadováno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Požadováno
Microsoft.ComponentGroup.Blend | Blend for Visual Studio | 15.0.26711.1 | Doporučeno
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Doporučeno
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 nástrojů | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.LiveUnitTesting | Testování částí za provozu | 15.0.26720.2 | Doporučeno
Component.Dotfuscator | Preemptivní ochrana – Dotfuscatoru | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.6.2.SDK | Rozhraní .NET framework 4.6.2 SDK | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.6.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.2 | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.7.SDK | Rozhraní .NET framework 4.7 SDK | 15.0.26419.1 | Nepovinné
Microsoft.Net.Component.4.7.TargetingPack | Rozhraní .NET framework 4.7 cílení pack | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | Nástroje pro vývoj rozhraní .NET framework 4.6.2 | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | Nástroje pro vývoj 4.7 rozhraní .NET framework | 15.0.26606.0 | Nepovinné
Microsoft.Net.Core.Component.SDK | Nástroje pro vývoj 1.0 1.1 základní rozhraní .NET | 15.0.26606.0 | Nepovinné
Microsoft.Net.Core.Component.SDK.1x | .NET core 1.0 1.1 vývojových nástrojů pro plochu | 15.0.26919.1 | Nepovinné
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.CodeClone | Klonování kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Ověření za provozu závislostí | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.FSharp | Podpora jazyka F # | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Architektura a analytických nástrojích | 15.0.26208.0 | Nepovinné


## <a name="game-development-with-unity"></a>Vývoj her s Unity

**ID:** Microsoft.VisualStudio.Workload.ManagedGame

**Popis:** vytvořit 2D a 3D hry s Unity, výkonné a platformy prostředí pro vývoj.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.Net.Component.3.5.DeveloperTools | Nástroje pro vývoj rozhraní .NET framework 3.5 | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Unity | Visual Studio Tools for Unity | 15.0.26823.1 | Požadováno
Component.UnityEngine.x64 | Editor 64-bit Unity 2017.1 | 15.0.26919.1 | Doporučeno
Component.UnityEngine.x86 | Editor Unity 5.6 32-bit | 15.0.26919.1 | Doporučeno


## <a name="linux-development-with-c"></a>Vývoj pro Linux s C++

**ID:** Microsoft.VisualStudio.Workload.NativeCrossPlat

**Popis:** vytvořit a ladění aplikace běžící v prostředí Linux.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.MDD.Linux | Visual C++ vývoje pro Linux | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Windows10SDK | Prostředí Windows Universal C Runtime | 15.0.26621.2 | Požadováno
Component.Linux.CMake | Nástroje sady Visual C++ pro CMake a Linux | 15.0.27004.2002 | Doporučeno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) pro plochy C++ [x86 a x64] | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) pro UPW: C++ | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno


## <a name="desktop-development-with-c"></a>Vývoj aplikací s C++

**ID:** Microsoft.VisualStudio.Workload.NativeDesktop

**Popis:** sestavení classic aplikace pro systém Windows pomocí power nástrojů Visual C++, ATL a volitelné funkce, například MFC a C + +/ CLI.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.ClassDesigner | Návrhář tříd | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Debugger.JustInTime | Ladicí program za běhu | 15.0.26823.1 | Požadováno
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Požadováno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | Aktualizace Visual C++ 2017 Redistributable | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Native | Nástroje pro architekturu pro jazyk C++ | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | Visual C++ hlavní plochy funkce | 15.0.26621.2 | Požadováno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Microsoft.VisualStudio.Component.Graphics.Tools | Ladicího programu grafiky a GPU profileru pro rozhraní DirectX | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafické nástroje Windows 8.1 SDK | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.VC.CMake.Project | Nástroje sady Visual C++ pro CMake | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ nástroje pro profilaci | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) pro plochy C++ [x86 a x64] | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) pro UPW: C++ | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno
Component.Incredibuild | IncrediBuild - akcelerace sestavení | 15.0.26919.1 | Nepovinné
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.1 | Nepovinné
Microsoft.Component.VC.Runtime.UCRTSDK | Sady Windows Universal CRT SDK | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.VC.140 | Sada nástrojů v140 VC ++ 2015.3 pro plochu (x86, x64) | 15.0.26720.2 | Nepovinné
Microsoft.VisualStudio.Component.VC.ATL | Podpora Visual C++ ATL | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.ATLMFC | Podpora MFC a knihovny ATL (x86 a x64) | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.VC.ClangC2 | Clang/C2 (experimentální) | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.CLI.Support | C + +/ CLI podpory | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | Moduly pro standardní knihovny (experimentální) | 15.0.26720.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.15063.Desktop | Windows 10 SDK (10.0.15063.0) pro plochy C++ [x86 a x64] | 15.0.26929.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) pro UPW: C#, VB, JS | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) pro UPW: C++ | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows81SDK | Windows 8.1 SDK | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.WinXP | Podpora Windows XP pro C++ | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Win81 | Windows 8.1 SDK a sadu SDK UCRT | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.WinXP | Podpora Windows XP pro C++ | 15.0.26208.0 | Nepovinné


## <a name="game-development-with-c"></a>Vývoj her s C++

**ID:** Microsoft.VisualStudio.Workload.NativeGame

**Popis:** pomocí potenciál C++ můžete vytvářet profesionální hry používá technologii DirectX, nerealiz nebo Cocos2d.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | Aktualizace Visual C++ 2017 Redistributable | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Graphics.Tools | Ladicího programu grafiky a GPU profileru pro rozhraní DirectX | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafické nástroje Windows 8.1 SDK | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ nástroje pro profilaci | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) pro plochy C++ [x86 a x64] | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) pro UPW: C++ | 15.0.27004.2002 | Doporučeno
Component.Android.NDK.R12B | Android NDK (R12B) | 12.1.9 | Nepovinné
Component.Android.SDK23.Private | Instalační program Android SDK (úroveň rozhraní API 23) (místní instalace) | 15.0.26906.1 | Nepovinné
Component.Ant | Apache Ant (1.9.3) | 1.9.3.7 | Nepovinné
Component.Cocos | Cocos | 15.0.26906.1 | Nepovinné
Component.Incredibuild | IncrediBuild - akcelerace sestavení | 15.0.26919.1 | Nepovinné
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.1 | Nepovinné
Component.JavaJDK | Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Nepovinné
Component.MDD.Android | Nástroje pro vývoj C++ Android | 15.0.26606.0 | Nepovinné
Component.Unreal | Instalační program Unreal Engine | 15.0.26621.2 | Nepovinné
Component.Unreal.Android | Visual Studio pro Android, podporují pro Unreal Engine | 15.0.26919.1 | Nepovinné
Microsoft.Component.VC.Runtime.UCRTSDK | Sady Windows Universal CRT SDK | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Nepovinné
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK | Prostředí Windows Universal C Runtime | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.15063.Desktop | Windows 10 SDK (10.0.15063.0) pro plochy C++ [x86 a x64] | 15.0.26929.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) pro UPW: C#, VB, JS | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) pro UPW: C++ | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows81SDK | Windows 8.1 SDK | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Win81 | Windows 8.1 SDK a sadu SDK UCRT | 15.0.26208.0 | Nepovinné


## <a name="mobile-development-with-c"></a>Mobilní vývoj s C++

**ID:** Microsoft.VisualStudio.Workload.NativeMobile

**Popis:** vytvářet multiplatformní aplikace pro iOS, Android nebo Windows pomocí C++.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Požadováno
Component.Android.NDK.R13B | Android NDK (R13B) | 13.1.6 | Doporučeno
Component.Android.SDK19 | Instalační program Android SDK (API úrovně 19 a 21) | 15.0.26621.2 | Doporučeno
Component.Android.SDK22 | Instalační program Android SDK (API úrovně 22) | 15.0.26208.0 | Doporučeno
Component.Android.SDK25 | Instalační program Android SDK (API úrovně 25) | 15.0.26919.1 | Doporučeno
Component.Ant | Apache Ant (1.9.3) | 1.9.3.7 | Doporučeno
Component.MDD.Android | Nástroje pro vývoj C++ Android | 15.0.26606.0 | Doporučeno
Component.Android.NDK.R12B | Android NDK (R12B) | 12.1.9 | Nepovinné
Component.Android.NDK.R12B_3264 | Android NDK (R12B) (32 bitů) | 12.1.10 | Nepovinné
Component.Android.NDK.R13B_3264 | Android NDK (R13B) (32 bitů) | 13.1.7 | Nepovinné
Component.Android.SDK23 | Instalační program Android SDK (úroveň rozhraní API 23) (globální instalace) | 15.0.26906.1 | Nepovinné
Component.Google.Android.Emulator.API23.V2 | Emulátor Google Android (API úrovně 23) (globální instalace) | 15.0.26906.1 | Nepovinné
Component.HAXM | Intel hardwaru Accelerated spuštění správce (HAXM) (globální instalace) | 15.0.26919.1 | Nepovinné
Component.Incredibuild | IncrediBuild - akcelerace sestavení | 15.0.26919.1 | Nepovinné
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.1 | Nepovinné
Component.JavaJDK | Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Nepovinné
Component.MDD.IOS | Nástroje pro vývoj iOS C++ | 15.0.26621.2 | Nepovinné


## <a name="net-core-cross-platform-development"></a>Vývoj pro různé platformy .NET core

**ID:** Microsoft.VisualStudio.Workload.NetCoreTools

**Popis:** vytvářet multiplatformní aplikace pomocí nástrojů pro vývoj .NET Core, ASP.NET Core, HTML, JavaScript a kontejneru.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.Net.Core.Component.SDK | Nástroje pro vývoj 1.0 1.1 základní rozhraní .NET | 15.0.26606.0 | Požadováno
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Požadováno
Microsoft.NetCore.ComponentGroup.Web | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Požadováno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Doporučeno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Doporučeno
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Doporučeno
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Doporučeno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Doporučeno
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Nástroje pro tvorbu Azure | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.ClientLibs | Knihovny Azure pro .NET | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulátoru služby výpočty Azure | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulátor úložiště Azure | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Waverton | Základní nástroje Azure Cloud Services | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.CloudExplorer | Průzkumník cloudu | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Doporučeno
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.DockerTools | Kontejnerové vývojové nástroje | 15.0.26724.1 | Doporučeno
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.LiveUnitTesting | Testování částí za provozu | 15.0.26720.2 | Doporučeno
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Doporučeno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL runtime | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CMDUtils | Nástroje příkazového řádku systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.DataSources | Zdroje dat pro podporu systému SQL Server | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno
Microsoft.Net.Core.Component.SDK.1x | .NET core 1.0 1.1 vývojových nástrojů pro plochu | 15.0.26919.1 | Nepovinné
Microsoft.NetCore.1x.ComponentGroup.Web | .NET core 1.0 1.1 vývojových nástrojů pro Web | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Vývoj čas podpory IIS | 15.0.26720.2 | Nepovinné


## <a name="mobile-development-with-net"></a>Mobilní vývoj pomocí rozhraní .NET

**ID:** Microsoft.VisualStudio.Workload.NetCrossPlat

**Popis:** vytvářet multiplatformní aplikace pro iOS, Android nebo Windows pomocí Xamarin.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Android.SDK25 | Instalační program Android SDK (API úrovně 25) | 15.0.26919.1 | Požadováno
Component.Google.Android.Emulator.API25 | Emulátor Google Android (API úrovně 25) | 15.0.26929.2 | Požadováno
Component.HAXM | Intel hardwaru Accelerated spuštění správce (HAXM) (globální instalace) | 15.0.26919.1 | Požadováno
Component.JavaJDK | Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Požadováno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Požadováno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Požadováno
Component.Android.NDK.R13B | Android NDK (R13B) | 13.1.6 | Doporučeno
Component.Xamarin | Xamarin | 15.0.26711.1 | Doporučeno
Component.Xamarin.Inspector | Sešity Xamarin | 15.0.26606.0 | Doporučeno
Component.Xamarin.Profiler | Xamarin profileru | 15.0.26823.1 | Doporučeno
Component.Xamarin.RemotedSimulator | Používat vzdáleně simulátoru Xamarin | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.FSharp | Podpora jazyka F # | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.Merq | Běžné interní nástroje pro Xamarin | 15.0.26720.2 | Doporučeno
Microsoft.VisualStudio.Component.MonoDebugger | Monofonní ladicí program | 15.0.26720.2 | Doporučeno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Nepovinné
Microsoft.Component.NetFX.Native | .NET Native | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.CodeClone | Klonování kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Ověření za provozu závislostí | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.Graphics | Bitové kopie a 3D editory modelu | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Phone.Emulator.15063 | Windows 10 emulátoru mobilního (Creators aktualizace) | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Architektura a analytických nástrojích | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | Univerzální platforma Windows nástroje pro Xamarin | 15.0.27004.2002 | Nepovinné


## <a name="aspnet-and-web-development"></a>ASP.NET a vývoje

**ID:** Microsoft.VisualStudio.Workload.NetWeb

**Popis:** tvorbu webových aplikací pomocí nástroje pro vývoj ASP.NET, ASP.NET Core, HTML, JavaScript a kontejneru.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.Net.Core.Component.SDK | Nástroje pro vývoj 1.0 1.1 základní rozhraní .NET | 15.0.26606.0 | Požadováno
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Požadováno
Microsoft.NetCore.ComponentGroup.Web | Nástroje pro vývoj .NET core 2.0 | 15.0.26919.1 | Požadováno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Doporučeno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Doporučeno
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Doporučeno
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Doporučeno
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Doporučeno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Doporučeno
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Nástroje pro tvorbu Azure | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.ClientLibs | Knihovny Azure pro .NET | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulátoru služby výpočty Azure | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulátor úložiště Azure | 15.0.26823.1 | Doporučeno
Microsoft.VisualStudio.Component.Azure.Waverton | Základní nástroje Azure Cloud Services | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.CloudExplorer | Průzkumník cloudu | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Doporučeno
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.DockerTools | Kontejnerové vývojové nástroje | 15.0.26724.1 | Doporučeno
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 nástrojů | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.LiveUnitTesting | Testování částí za provozu | 15.0.26720.2 | Doporučeno
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Doporučeno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL runtime | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CMDUtils | Nástroje příkazového řádku systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.DataSources | Zdroje dat pro podporu systému SQL Server | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno
Microsoft.Net.Component.4.6.2.SDK | Rozhraní .NET framework 4.6.2 SDK | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.6.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.2 | 15.0.26208.0 | Nepovinné
Microsoft.Net.Component.4.7.SDK | Rozhraní .NET framework 4.7 SDK | 15.0.26419.1 | Nepovinné
Microsoft.Net.Component.4.7.TargetingPack | Rozhraní .NET framework 4.7 cílení pack | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | Nástroje pro vývoj rozhraní .NET framework 4.6.2 | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | Nástroje pro vývoj 4.7 rozhraní .NET framework | 15.0.26606.0 | Nepovinné
Microsoft.Net.Core.Component.SDK.1x | .NET core 1.0 1.1 vývojových nástrojů pro plochu | 15.0.26919.1 | Nepovinné
Microsoft.NetCore.1x.ComponentGroup.Web | .NET core 1.0 1.1 vývojových nástrojů pro Web | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.CodeClone | Klonování kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Ověření za provozu závislostí | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.FSharp | Podpora jazyka F # | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.TestTools.WebLoadTest | Výkonnosti webů a zátěžové testování nástroje | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Architektura a analytických nástrojích | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Vývoj čas podpory IIS | 15.0.26720.2 | Nepovinné
Microsoft.VisualStudio.Web.Mvc4.ComponentGroup | ASP.NET MVC 4 | 15.0.26606.0 | Nepovinné


## <a name="nodejs-development"></a>Vývoj pro Node.js

**ID:** Microsoft.VisualStudio.Workload.Node

**Popis:** vytvářet škálovatelné síťové aplikace pomocí Node.js, asynchronní runtime jazyka JavaScript založeného na událostech.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Požadováno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Node.Tools | Podpora Node.js | 15.0.26823.1 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Doporučeno
Microsoft.VisualStudio.Component.Git | Git for Windows | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Nepovinné


## <a name="officesharepoint-development"></a>Vývoj pro Office/SharePoint

**ID:** Microsoft.VisualStudio.Workload.Office

**Popis:** doplňky vytvořit Office a SharePoint, řešení služby SharePoint a doplňků VSTO pomocí jazyka C#, VB a JavaScript.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Požadováno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Požadováno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Požadováno
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Požadováno
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Požadováno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Požadováno
Microsoft.VisualStudio.Component.Debugger.JustInTime | Ladicí program za běhu | 15.0.26823.1 | Požadováno
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Požadováno
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | Nástroje pro vývoj aplikací rozhraní .NET | 15.0.26906.1 | Požadováno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.Sharepoint.Tools | Office Developer Tools for Visual Studio | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL runtime | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.CMDUtils | Nástroje příkazového řádku systému SQL Server | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.DataSources | Zdroje dat pro podporu systému SQL Server | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Požadováno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Workflow | Windows Workflow Foundation | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.TeamOffice | Visual Studio Tools for Office (VSTO) | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Nepovinné


## <a name="python-development"></a>Vývoj Python

**ID:** Microsoft.VisualStudio.Workload.Python

**Popis:** úpravy, ladění, interaktivní vývoj a zdroj ovládacího prvku pro jazyk Python.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.CPython3.x64 | Python 3 64-bit (3.6.2) | 3.6.2 | Doporučeno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Doporučeno
Microsoft.Component.CookiecutterTools | Podpora Cookiecutter šablony | 15.0.26621.2 | Doporučeno
Microsoft.Component.PythonTools | Podpora jazyka Python | 15.0.26823.1 | Doporučeno
Microsoft.Component.PythonTools.Web | Podpora webového Python | 15.0.26606.0 | Doporučeno
Microsoft.Component.VC.Runtime.UCRTSDK | Sady Windows Universal CRT SDK | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Common.Azure.Tools | Nástroje pro připojení a publikování | 1.10.50614.2 | Doporučeno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.Windows81SDK | Windows 8.1 SDK | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Doporučeno
Component.Anaconda2.x64 | Anaconda2 64-bit (4.4.0) | 4.4.0 | Nepovinné
Component.Anaconda2.x86 | 32bitový Anaconda2 (4.4.0) | 4.4.0 | Nepovinné
Component.Anaconda3.x64 | Anaconda3 64-bit (4.4.0) | 4.4.0 | Nepovinné
Component.Anaconda3.x86 | 32bitový Anaconda3 (4.4.0) | 4.4.0 | Nepovinné
Component.CPython2.x64 | Python 2 64-bit (2.7.13) | 2.7.13 | Nepovinné
Component.CPython2.x86 | Python 2 32-bit (2.7.13) | 2.7.13 | Nepovinné
Component.CPython3.x86 | Python 3 32-bit (3.6.2) | 3.6.2 | Nepovinné
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Nepovinné
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Nepovinné
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Nepovinné
Microsoft.Component.NetFX.Native | .NET Native | 15.0.26208.0 | Nepovinné
Microsoft.Component.PythonTools.UWP | Podpora Python IoT | 15.0.26606.0 | Nepovinné
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Nástroje pro nativní vývoj Python | 15.0.27004.2002 | Nepovinné
Microsoft.Net.Component.4.5.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.1 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.5.2.TargetingPack | Cílovou sadu rozhraní .NET framework 4.5.2 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.TargetingPack | Cílení na pack rozhraní .NET framework 4 | 15.0.26621.2 | Nepovinné
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Nepovinné
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Nástroje pro vývoj rozhraní .NET framework 4 – 4.6 | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Nástroje pro tvorbu Azure | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Azure.ClientLibs | Knihovny Azure pro .NET | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulátoru služby výpočty Azure | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulátor úložiště Azure | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Azure.Waverton | Základní nástroje Azure Cloud Services | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.ClassDesigner | Návrhář tříd | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.CodeClone | Klonování kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.Graphics | Bitové kopie a 3D editory modelu | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Graphics.Tools | Ladicího programu grafiky a GPU profileru pro rozhraní DirectX | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafické nástroje Windows 8.1 SDK | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.IISExpress | Služby IIS Express  | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Jádro spravované plochy pracovního vytížení | 15.0.26419.1 | Nepovinné
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL runtime | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.SQL.CMDUtils | Nástroje příkazového řádku systému SQL Server | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.SQL.DataSources | Zdroje dat pro podporu systému SQL Server | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.140 | Sada nástrojů v140 VC ++ 2015.3 pro plochu (x86, x64) | 15.0.26720.2 | Nepovinné
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ nástroje pro profilaci | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK | Prostředí Windows Universal C Runtime | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) pro plochy C++ [x86 a x64] | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) pro UPW: C++ | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET a webové nástroje pro vývoj | 15.0.26606.0 | Nepovinné


## <a name="universal-windows-platform-development"></a>Vývoj pro univerzální platformu Windows

**ID:** Microsoft.VisualStudio.Workload.Universal

**Popis:** vytvářet aplikace pro univerzální platformu Windows pomocí jazyka C#, VB, JavaScript nebo volitelně C++.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Požadováno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Požadováno
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Požadováno
Microsoft.Component.NetFX.Native | .NET Native | 15.0.26208.0 | Požadováno
Microsoft.ComponentGroup.Blend | Blend for Visual Studio | 15.0.26711.1 | Požadováno
Microsoft.Net.Component.4.5.TargetingPack | Cílení na pack rozhraní .NET framework 4.5 | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.Graphics | Bitové kopie a 3D editory modelu | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.Component.UWP.Support | Nástroje pro univerzální platformu Windows | 15.0.26906.1 | Požadováno
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Požadováno
Microsoft.VisualStudio.ComponentGroup.UWP.Cordova | Univerzální platforma Windows nástroje pro Cordova | 15.0.27004.2002 | Požadováno
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | Univerzální platforma Windows nástroje pro Xamarin | 15.0.27004.2002 | Požadováno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) pro UPW: C#, VB, JS | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) pro UPW: C++ | 15.0.26621.2 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.Win10SDK_10.0.15063.UWP.All | Windows 10 SDK (10.0.15063.0) pro UPW | 15.0.27004.2002 | Doporučeno
Microsoft.Component.VC.Runtime.OSSupport | Visual C++ runtime pro UPW | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.CodeClone | Klonování kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Ověření za provozu závislostí | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.Graphics.Tools | Ladicího programu grafiky a GPU profileru pro rozhraní DirectX | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafické nástroje Windows 8.1 SDK | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Phone.Emulator.15063 | Windows 10 emulátoru mobilního (Creators aktualizace) | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.Tools.ARM | Kompilátory jazyka Visual C++ a knihovny pro ARM | 15.0.26906.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) pro UPW: C++ | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Architektura a analytických nástrojích | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.UWP.VC | Nástroje pro univerzální platformu Windows C++ | 15.0.27004.2002 | Nepovinné


## <a name="visual-studio-extension-development"></a>Vývoj rozšíření pro Visual Studio

**ID:** Microsoft.VisualStudio.Workload.VisualStudioExtension

**Popis:** vytvořit doplňky a rozšíření pro Visual Studio, včetně nové příkazy kód analyzátorů a nástroje systému windows.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Požadováno
Microsoft.Net.Component.4.6.1.SDK | Rozhraní .NET framework 4.6.1 SDK | 15.0.26621.2 | Požadováno
Microsoft.Net.Component.4.6.1.TargetingPack | Cílovou sadu rozhraní .NET framework 4.6.1 | 15.0.26621.2 | Požadováno
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Nástroje pro vývoj rozhraní .NET framework 4.6.1 | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.PortableLibrary | Cílení na pack přenosné knihovny .NET | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.ComponentGroup.VisualStudioExtension.Prerequisites | Visual Studio rozšíření vývoj požadavků | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.CodeClone | Klonování kódu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.CodeMap | Mapa kódu | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Ověření za provozu závislostí | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Doporučeno
Microsoft.VisualStudio.Component.GraphDocument | DGML editor | 15.0.26906.1 | Doporučeno
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 15.0.26606.0 | Doporučeno
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Systém SQL Server Express 2016 LocalDB | 15.0.26919.1 | Doporučeno
Microsoft.VisualStudio.Component.SQL.NCLI | Nativní klient SQL serveru | 15.0.26208.0 | Doporučeno
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Architektura a analytických nástrojích | 15.0.26208.0 | Doporučeno
Component.Dotfuscator | Preemptivní ochrana – Dotfuscatoru | 15.0.26208.0 | Nepovinné
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Nepovinné
Microsoft.Component.VC.Runtime.OSSupport | Visual C++ runtime pro UPW | 15.0.26621.2 | Nepovinné
Microsoft.Net.Component.4.6.TargetingPack | Cílení na pack rozhraní .NET framework 4.6. | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.ClassDesigner | Návrhář tříd | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.DslTools | Modelování SDK | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.NuGet | Správce balíčků NuGet | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.TextTemplating | Transformace textové šablony | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.ATL | Podpora Visual C++ ATL | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VC.ATLMFC | Podpora MFC a knihovny ATL (x86 a x64) | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ klíčových funkcí | 15.0.26606.0 | Nepovinné
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Sada nástrojů v141 VC ++ 2017 (x86, x64) | 15.0.26823.1 | Nepovinné
Microsoft.VisualStudio.Component.VSSDK | Visual Studio SDK | 15.0.26919.1 | Nepovinné


## <a name="mobile-development-with-javascript"></a>Mobilní vývoj pomocí jazyka JavaScript

**ID:** Microsoft.VisualStudio.Workload.WebCrossPlat

**Popis:** vývoj aplikací pro Android, iOS a UWP pomocí nástrojů pro Apache Cordova.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Component.CordovaToolset.6.3.1 | Sada nástrojů Cordova 6.3.1 | 15.0.26504.0 | Požadováno
Component.Microsoft.VisualStudio.RazorExtension | Služby jazyk Razor | 15.0.26720.2 | Požadováno
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Cordova | Mobilní vývoj s hlavní funkce jazyka JavaScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostika JavaScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.ProjectSystem | JavaScript ProjectSystem a sdílené nástrojů | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Podpora jazyků JavaScript a TypeScript | 15.0.26606.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilátory jazyka C# a Visual Basic Roslyn | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# a Visual Basic | 15.0.26711.1 | Požadováno
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statické analytické nástroje | 15.0.26208.0 | Požadováno
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 SDK | 15.0.26621.2 | Požadováno
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET a vývoje | 15.0.26606.0 | Požadováno
Component.Android.SDK23.Private | Instalační program Android SDK (úroveň rozhraní API 23) (místní instalace) | 15.0.26906.1 | Nepovinné
Component.Google.Android.Emulator.API23.Private | Emulátor Google Android (API úrovně 23) (místní instalace) | 15.0.26906.1 | Nepovinné
Component.HAXM.Private | Intel hardwaru Accelerated spuštění správce (HAXM) (místní instalace) | 15.0.26919.1 | Nepovinné
Component.JavaJDK | Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Nepovinné
Microsoft.Component.ClickOnce | Publikování ClickOnce | 15.0.26919.1 | Nepovinné
Microsoft.Component.NetFX.Native | .NET Native | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.AppInsights.Tools | Developer Analytics tools | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.DiagnosticTools | Rozhraní .NET, nástroje pro profilaci | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.Git | Git for Windows | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Graphics | Bitové kopie a 3D editory modelu | 15.0.26621.2 | Nepovinné
Microsoft.VisualStudio.Component.Phone.Emulator.15063 | Windows 10 emulátoru mobilního (Creators aktualizace) | 15.0.26711.1 | Nepovinné
Microsoft.VisualStudio.Component.SQL.CLR | Datové typy CLR systému SQL Server | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.VisualStudioData | Zdroje dat a odkazy na službu | 15.0.26208.0 | Nepovinné
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) pro UPW: C#, VB, JS | 15.0.27004.2002 | Nepovinné
Microsoft.VisualStudio.ComponentGroup.UWP.Cordova | Univerzální platforma Windows nástroje pro Cordova | 15.0.27004.2002 | Nepovinné


## <a name="unaffiliated-components"></a>Nezávislou na komponenty

Toto jsou součásti, které nejsou součástí žádné úlohy, ale může být vybraný jako jednotlivé součásti.

ID součásti | Název | Version
--- | --- | ---
Component.Android.Emulator | Emulátor sady Visual Studio pro Android | 15.0.26711.1
Component.Android.NDK.R11C | Android NDK (R11C) | 11.3.13
Component.Android.NDK.R11C_3264 | Android NDK (R11C) (32 bitů) | 11.3.15
Component.GitHub.VisualStudio | GitHub rozšíření pro Visual Studio | 2.2.0.10
Microsoft.Component.Blend.SDK.WPF | Blend for Visual Studio SDK pro .NET | 15.0.26929.2
Microsoft.Component.HelpViewer | Prohlížeč nápovědy | 15.0.26711.1
Microsoft.VisualStudio.Component.LinqToSql | Technologie LINQ to SQL nástroje | 15.0.26208.0
Microsoft.VisualStudio.Component.Phone.Emulator | Windows 10 emulátoru mobilního (Anniversary Edition) | 15.0.26711.1
Microsoft.VisualStudio.Component.TestTools.CodedUITest | Programový test UI | 15.0.26606.0
Microsoft.VisualStudio.Component.TestTools.Core | Testovací nástroje pro základní funkce | 15.0.26606.0
Microsoft.VisualStudio.Component.TestTools.FeedbackClient | Microsoft Feedback Client | 15.0.26711.1
Microsoft.VisualStudio.Component.TestTools.MicrosoftTestManager | Microsoft Test Manager | 15.0.26606.0
Microsoft.VisualStudio.Component.TypeScript.2.0 | TypeScript 2.0 SDK | 15.0.26504.0
Microsoft.VisualStudio.Component.TypeScript.2.1 | TypeScript 2.1 SDK | 15.0.26208.0
Microsoft.VisualStudio.Component.TypeScript.2.2 | TypeScript 2.2 SDK | 15.0.26504.0
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | Kompilátory jazyka Visual C++ a knihovny pro ARM64 | 15.0.26906.1
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop.arm | Windows 10 SDK (10.0.16299.0) pro plochy C++ [ARM a ARM64] | 15.0.27004.2002

## <a name="get-support"></a>Získat podporu
V některých případech může problémů. Pokud se nezdaří instalace Visual Studia, najdete v článku [problémy instalace a upgrade řešení potíží s Visual Studio 2017](troubleshooting-installation-issues.md) stránku Tipy pro odstraňování potíží. Taky můžete hlášení problémů produktu pro nás prostřednictvím [nahlásit problém](../ide/how-to-report-a-problem-with-visual-studio-2017.md) nástroj v prostředí Visual Studio IDE nebo ke sdílení návrh s nám na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Můžete sledovat problémy produktu v [Visual Studio Community vývojáře](https://developercommunity.visualstudio.com/)a klást otázky a odpovědi. Můžete také použít s námi a jinými vývojáři Visual Studio prostřednictvím našich [Visual Studio konverzace v komunitě Gitter](https://gitter.im/Microsoft/VisualStudio) (vyžaduje [Githubu](https://github.com/) účtu).

## <a name="see-also"></a>Viz také

* [ID úlohy a součást Visual Studio](workload-and-component-ids.md)
* [Příručka správce Visual Studio](visual-studio-administrator-guide.md)
* [Používání parametrů příkazového řádku pro instalaci sady Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
  * [Příklady parametr příkazového řádku](command-line-parameter-examples.md)
* [Vytvoření offline instalace sady Visual Studio](create-an-offline-installation-of-visual-studio.md)