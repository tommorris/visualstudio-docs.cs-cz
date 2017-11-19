---
title: "Dialogové okno požadavky | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: Microsoft.VisualStudio.Publish.BaseProvider.Dialog.Bootstrapper
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords: Prerequisites dialog box
ms.assetid: 53ac863c-77a0-409b-91e5-7a4bd8b8474e
caps.latest.revision: "75"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 68e326d8045733fc4f491c51405ed51414a92afd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="prerequisites-dialog-box"></a>Dialogové okno Požadavky
Toto dialogové okno určuje požadovaných součástí, které jsou nainstalovány, způsobu instalace a které pořadí, jestli že jsou nainstalované balíčky.  
  
 Pro přístup k tohoto dialogového okna, vyberte uzel projektu v **Průzkumníku řešení**a pak klikněte na **projektu** nabídky, klikněte na tlačítko **vlastnosti**. Když **Návrhář projektu** se zobrazí, klikněte na tlačítko **publikovat** kartě. Na **publikovat** klikněte na tlačítko **požadavky**. Pro projekty instalace na **projektu** nabídky, klikněte na tlačítko **vlastnosti**. Když **stránky vlastností** se zobrazí dialogové okno, klikněte na tlačítko **požadavky**.  
  
## <a name="uielement-list"></a>Seznam prvků uživatelského rozhraní  
  
|Prvek|Popis|  
|-------------|-----------------|  
|**Vytvořit instalační program pro instalaci požadovaných součástí**|Obsahuje součásti, které ve vaší aplikaci instalačního programu (Setup.exe) tak, aby se nainstalují před vaší aplikace, v pořadí podle závislostí. Ve výchozím nastavení je tato možnost vybrána. Pokud není zaškrtnuto, vytvoří se žádné Setup.exe.|  
|**Vyberte, které požadavky pro instalaci**|Určuje, zda chcete nainstalovat komponenty, jako [!INCLUDE[dnprdnshort](../../code-quality/includes/dnprdnshort_md.md)], Crystal Reports a tak dále.<br /><br /> Například podle zaškrtněte políčko vedle **SQL Server 2005 Express Edition SP2**, určíte, že instalační program ověřte, jestli tato součást je nainstalován v cílovém počítači a nainstalujte ji, pokud již není nainstalována.<br /><br /> Podrobné informace o jednotlivých požadovaných součástí balíčku najdete v tabulce informací o požadavcích později v tomto tématu.|  
|**Kontrolovat více distribuovatelné součásti Microsoft Update**|Kliknutím na tento odkaz přejdete na [balíčků zaváděcího nástroje znovu distribuovat součástí](http://go.microsoft.com/fwlink/?LinkId=208835) webu ke kontrole aktualizací.|  
|**Stažení požadované součásti z webu dodavatele součásti**|Určuje, že požadované součásti nainstalovat z webu dodavatele. Toto je výchozí možnost.|  
|**Stáhnout požadavky ze stejného umístění jako Moje aplikace**|Určuje, že požadované součásti nainstalovat ze stejného umístění jako aplikace. Zkopíruje všechny požadované balíčky do umístění pro publikování. Tato možnost bude fungovat, pouze pokud jsou balíčky požadovaných součástí ve vývojovém počítači.|  
|**Stažení požadované součásti z následujícího umístění**|Určuje, že požadované součásti nainstalovat z umístění, které vyberete. Můžete použít **Procházet** tlačítko vyberte umístění.|  
  
## <a name="prerequisites-information"></a>Informací o požadavcích  
 Požadované součásti, které se zobrazují v **požadavky** dialogové okno mohou lišit od těch v následujícím seznamu. Požadované balíčky uvedené v **dialogové okno požadavky** jsou automaticky nastavit poprvé otevřete dialogové okno. Pokud později změníte cílový framework projektu na, je nutné vybrat požadavky ručně tak, aby odpovídala nové cílové rozhraní.  
  
|Prvek|Popis|  
|-------------|-----------------|  
|**Rozhraní .NET framework 3.5 SP1**|Tento balíček nainstaluje následující:<br /><br /> -Rozhraní .NET framework verze 2.0, 3.0 a 3.5.<br />-Podpora pro všechny verze rozhraní .NET Framework na 32bitové (x86) a (x64) 64bitové operační systémy.<br />-Jazykové sady pro každou verzi rozhraní .NET Framework, která se instaluje se balíček.<br />-Služba sady pro rozhraní .NET Framework 2.0 a 3.0.<br /><br /> Rozhraní .NET framework 3.0 je součástí systému Windows Vista a rozhraní .NET Framework 3.5 je součástí [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Rozhraní .NET framework 3.5 je vyžadována pro všechny jazyka Visual Basic a Visual C# zkompilovaných projektů pro 32bitové operační systémy a pro který cílovém Frameworku, který je nastaven na **rozhraní .NET Framework 3.5**a pro projekty Visual Basic a Visual C# zkompilovat pro 64bitové operační systémy. (IA64 není podporována.) Všimněte si, že jsou projekty Visual Basic a Visual C# zkompilovaném pro všechny architektura procesoru ve výchozím nastavení. Další informace najdete v tématu [přehled cílení na více Visual Studio](../../ide/visual-studio-multi-targeting-overview.md), [Redistribuce rozhraní .NET Framework](http://msdn.microsoft.com/en-us/a18d0456-fd89-493e-97f4-756505bfe287), a [nasazení požadovaných součástí pro 64bitové aplikace](../../deployment/deploying-prerequisites-for-64-bit-applications.md).<br /><br /> Ve výchozím nastavení je vybraná tato položka.|  
|**Profil klienta .NET framework 3.5 SP1**|Profil klienta rozhraní .NET Framework je podmnožinu rozhraní úplné rozhraní .NET Framework 3.5 SP1 zacílený klientské aplikace. Poskytuje zjednodušenou podmnožinu Windows Presentation Foundation (WPF), Windows Forms, Windows Communication Foundation (WCF) a ClickOnce funkcí. To umožňuje rychlé nasazení scénáře pro WPF, Windows Forms, WCF a konzolové aplikace cílených rozhraní .NET Framework Client Profile. Další informace najdete v tématu [profil klienta rozhraní .NET Framework](/dotnet/framework/deployment/client-profile).|  
|**Rozhraní Microsoft .NET Framework 4 (x86 a x64)**|Tento balíček nainstaluje rozhraní .NET Framework 4 pro x86 a x64 platformy.<br /><br /> Další informace najdete v tématu [přehled cílení na více Visual Studio](../../ide/visual-studio-multi-targeting-overview.md), [Redistribuce rozhraní .NET Framework](http://msdn.microsoft.com/en-us/a18d0456-fd89-493e-97f4-756505bfe287), a [nasazení požadovaných součástí pro 64bitové aplikace](../../deployment/deploying-prerequisites-for-64-bit-applications.md).<br /><br /> Ve výchozím nastavení je vybraná tato položka.|  
|**Rozhraní Microsoft .NET Framework 4 Client Profile (x86 a x64)**|Profil klienta rozhraní .NET Framework 4 je podmnožinou úplné rozhraní .NET Framework 4, která je cílena klientské aplikace. Poskytuje zjednodušenou podmnožinu Windows Presentation Foundation (WPF), Windows Forms, Windows Communication Foundation (WCF) a ClickOnce funkcí. To umožňuje rychlé nasazení scénáře pro WPF Windows Forms a konzolové aplikace cílených rozhraní .NET Framework 4 Client Profile. Další informace najdete v tématu [profil klienta rozhraní .NET Framework](/dotnet/framework/deployment/client-profile).|  
|**Primární zprostředkovatel komunikace s objekty sestavení sady Microsoft Office 2007**|Tento balíček nainstaluje primární zprostředkovatel komunikace s objekty sestavení pro 2007 produktů Microsoft Office. Primární spolupracující sestavení umožňuje spravovaného kódu k interakci s modelem COM na objekt z aplikace Microsoft Office. Další informace najdete v tématu [primární zprostředkovatel komunikace s objekty sestavení sady Office](/office-dev/office-dev/office-primary-interop-assemblies).|  
|**Microsoft PowerPacks jazyka Visual Basic verze 10.0.**|Power Pack jsou doplňky, ovládací prvky, komponenty a nástroje, které vám pomohou při vývoji aplikací jazyka Visual Basic. Tato verze obsahuje <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> komponenta, která umožňuje tisknout obsah formuláře Windows a knihovně tiskárny, který umožňuje spuštění beze změny kódu jazyka Visual Basic 6.0 tiskárny.|  
|**Microsoft Visual F # Runtime pro rozhraní .NET 2.0**|Tento balíček nainstaluje knihovny runtime Visual F # pro x86 a x64 operační systémy, které poskytují podporu pro funkční programování, jakož i tradiční objektově orientované a imperativní programování (procedurální). Tento balíček musí být nainstalován, pokud aplikace nebo jeho součástí je vytvořen ve Visual F # a rozhraní .NET Framework 2.0, .NET Framework 3.0 nebo rozhraní .NET Framework 3.5.<br /><br /> Další informace najdete v tématu [referenční dokumentace jazyka F #](http://msdn.microsoft.com/Library/16b706f8-b5f2-4ff7-b2c1-64df33cd6adf).|  
|**Microsoft Visual F # Runtime pro rozhraní .NET 4.0**|Tento balíček nainstaluje knihovny runtime Visual F # pro x86 a x64 operační systémy, které poskytují podporu pro funkční programování, jakož i tradiční objektově orientované a imperativní programování (procedurální). Tento balíček musí být nainstalován, pokud aplikace nebo jeho součástí je vytvořen ve Visual F # a rozhraní .NET Framework 4.<br /><br /> Další informace najdete v tématu [referenční dokumentace jazyka F #](http://msdn.microsoft.com/Library/16b706f8-b5f2-4ff7-b2c1-64df33cd6adf).|  
|**Prohlížeč sestav Microsoft Visual Studio 2010**|Tento balíček nainstaluje ovládací prvky prohlížeče sestav, které můžete použít k přidání bohaté dat reporting Windows Forms a aplikací ASP.NET.|  
|**Sadu Microsoft Visual Studio 2010 pro modul Runtime sady Office (x86 a x64)**|Sada Office developer tools v sadě Visual Studio nabízí snadné použití, integrované nástroje pro vytváření vlastní obchodní řešení s Microsoft Office. Můžete vytvořit řešení spravované inteligentní klienta, která používají aplikace Office jako uživatelské rozhraní. Nástroje umožňují vývojářům vytvářet zabezpečené řešení, které se snadno nasadit a udržovat.<br /><br /> Další informace najdete v tématu [postupy: publikování aplikací ClickOnce pomocí řešení Office](http://msdn.microsoft.com/en-us/2b6c247e-bc04-4ce4-bb64-c4e79bb3d5b8).|  
|**SQL Server 2005 Express Edition SP2 (x 86)**|Tento balíček nainstaluje Microsoft SQL Server 2005 Express Edition SP2, databázovou aplikaci, která je založená na [!INCLUDE[sqprsqext](../../ide/reference/includes/sqprsqext_md.md)]. SQL Server Express je nahrazení pro Microsoft SQL Server Desktop Engine (MSDE). SQL Server Express je zdarma a můžete znovu distribuovat (přičemž podléhá smlouvě) a funguje jako klient databázi a databázi základní server. Je stejný jako SQL Server 2005, vyjma následujících rozdílů:<br /><br /> -Žádné funkce organizace podporovat.<br />-Omezeno na jeden procesor.<br />-limit paměti 1 gigabajt (GB) pro fond vyrovnávací paměti.<br />– Maximální velikost 4 GB pro databáze.|  
|**SQL Server 2008 Express.**|Tento balíček nainstaluje Microsoft SQL Server 2008 Express, bezplatná edice systému Microsoft SQL Server 2008, databázi ideální pro malé webové, server nebo aplikací klasické pracovní plochy. Může sloužit zdarma pro vývoj a produkci. Bezplatný [registrace](http://go.microsoft.com/fwlink/?LinkId=130380) je vyžadována pro distribuci SQL Server 2008 Express s aplikací.<br /><br /> Chování zavaděč je následující:<br /><br /> – Pokud má počítač již systému SQL Server 2008 Express nebo novější, počítač zůstává na SQL Server 2008 Express nebo novější.<br />– Pokud počítač nemá žádné verzi systému SQL Server 2008 Express nebo novější, balíček nainstaluje nejnovější verzi SQL Server 2008 Express SP1.<br /><br /> Další informace o SQL Server 2008 Express, navštivte [http://go.microsoft.com/fwlink/?LinkId=183586](http://go.microsoft.com/fwlink/?LinkId=183586).|  
|**Visual C++ 2010 Runtime knihovny (IA64)**|Tento balíček nainstaluje běhové knihovny jazyka Visual C++ pro architekturu Itanium, které poskytují rutiny pro programování pro operační systém Microsoft Windows. Tyto rutiny automatizovat mnoho běžných programovacích úloh, které nejsou k dispozici jazyky C a C++.<br /><br /> Další informace najdete v tématu [referenční dokumentace knihoven C Run-Time](/cpp/c-runtime-library/c-run-time-library-reference).|  
|**Visual C++ 2010 Runtime knihovny (x64)**|Tento balíček nainstaluje běhové knihovny jazyka Visual C++ pro x64 operační systémy, které poskytují rutiny pro programování pro operační systém Microsoft Windows. Tyto rutiny automatizovat mnoho běžných programovacích úloh, které nejsou k dispozici jazyky C a C++.<br /><br /> Další informace najdete v tématu [referenční dokumentace knihoven C Run-Time](/cpp/c-runtime-library/c-run-time-library-reference).|  
|**Visual C++ 2010 Runtime knihovny (x86)**|Tento balíček nainstaluje běhové knihovny jazyka Visual C++ pro x86 operační systémy, které poskytují rutiny pro programování pro operační systém Microsoft Windows. Tyto rutiny automatizovat mnoho běžných programovacích úloh, které nejsou k dispozici jazyky C a C++.<br /><br /> Další informace najdete v tématu [referenční dokumentace knihoven C Run-Time](/cpp/c-runtime-library/c-run-time-library-reference).|  
|**Instalační služba systému Windows verze 3.1**|Tento balíček nainstaluje verzi redistributable, na Instalační služby systému Windows 3.1, což umožňuje instalaci projekty instalace Instalační služby systému Windows. Je je předinstalován v systému Windows Server 2003 s aktualizací SP1 a novější.<br /><br /> Ve výchozím nastavení je vybraná tato položka.|  
|**Instalační služba systému Windows 4.5**|Tento balíček nainstaluje instalační služby systému Windows distribuovatelnou, verzi 4.5, která umožňuje instalaci projekty instalace Instalační služby systému Windows.|  
  
## <a name="see-also"></a>Viz také  
 [Publikovat stránku, Návrhář projektu](../../ide/reference/publish-page-project-designer.md)   
 [Požadavky na nasazení aplikací](../../deployment/application-deployment-prerequisites.md)   
 [Redistribuce rozhraní .NET Framework](http://msdn.microsoft.com/en-us/a18d0456-fd89-493e-97f4-756505bfe287)   
 [Nasazení nezbytných součástí pro 64bitové aplikace](../../deployment/deploying-prerequisites-for-64-bit-applications.md)   
 [Cílení na více verzí sady Visual Studio – přehled](../../ide/visual-studio-multi-targeting-overview.md)