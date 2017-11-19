---
title: "Vytváření balíčku Instalační služby systému Windows | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- .msi files, VSPackages
- msi files, VSPackages
ms.assetid: 0ce7c21d-0d3f-47fe-a0bb-eed506e32609
caps.latest.revision: "20"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5f646e2234adf0eb0117f154838b15d7b3aa200e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="authoring-a-windows-installer-package"></a>Vytváření balíčku Instalační služby systému Windows
Datových jednotkách modelu Instalační služby systému Windows. Místo psaní procedurální skriptu ke zkopírování souborů a zápis položky registru, například vytváříte řádků a sloupců v tabulkách databáze, které obsahují data souboru a registru.  
  
## <a name="database-entries"></a>Položky databáze  
 Pokud chcete nainstalovat VSPackage, balíček Instalační služby systému Windows musí obsahovat položky databáze k provádění následujících úloh:  
  
-   Vyhledávání systému najít verze [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] podporuje vaše VSPackage (pomocí tabulky Instalační služby systému Windows, které zahrnují AppSearch, CompLocator, RegLocator, DrLocator a podpis).  
  
-   Instalaci zrušit, pokud žádné podporovanou verzi [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] je nainstalován, nebo pokud jiný požadavek na systém VSPackage není splněná (pomocí tabulky LaunchCondition).  
  
-   Nainstalujte VSPackage a závislé soubory (pomocí adresáře, součásti a soubor tabulky).  
  
-   Přidejte příslušné informace o VSPackage do registru (pomocí registru tabulky).  
  
-   Integrovat VSPackage v [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] voláním **/Setup devenv.exe** (pomocí tabulky CustomAction).  
  
 Další informace najdete v tématu [Instalační služby systému Windows](http://msdn.microsoft.com/library/cc185688\(VS.85\).aspx).  
  
## <a name="setup-tools"></a>Instalační program nástroje  
 Celou řadu nástrojů jiných výrobců instalace zadejte vývojového prostředí pro balíčky Instalační služby systému Windows. Dva bezplatných nástrojů jsou následující:  
  
-   InstallShield Limited Edition  
  
     Omezené verzi InstallShield můžete získat pomocí sady Visual Studio **nový projekt** dialogové okno. Rozbalte položku **jiné typy projektů** a pak vyberte **instalace a nasazení**. Vyberte šablonu InstallShield.  
  
-   Sada nástrojů XML pro Instalační službu systému Windows  
  
     Sada nástrojů vytvoří balíčky Instalační služby systému Windows ze zdrojových souborů XML. Sada nástrojů je open source projektu společnosti Microsoft. Můžete si stáhnout zdrojového kódu a spustitelné soubory z [http://sourceforge.net/projects/wix](http://sourceforge.net/projects/wix).  
  
 Pro komerční produkty, které se integrují do [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] pomocí [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)], najdete v části [http://visualstudiogallery.com](http://visualstudiogallery.com/).  
  
## <a name="see-also"></a>Viz také  
 [Instalace VSPackages pomocí Instalační služby systému Windows](../../extensibility/internals/installing-vspackages-with-windows-installer.md)