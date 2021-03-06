---
title: Vytváření balíčku Instalační služby systému Windows | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- .msi files, VSPackages
- msi files, VSPackages
ms.assetid: 0ce7c21d-0d3f-47fe-a0bb-eed506e32609
caps.latest.revision: 21
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a9b56ea9120e3cbee18d8018420a94748dc52eec
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629644"
---
# <a name="authoring-a-windows-installer-package"></a>Vytvoření balíčku Instalační služby systému Windows
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [vytváření balíček Instalační služby systému Windows](https://docs.microsoft.com/visualstudio/extensibility/internals/authoring-a-windows-installer-package).  
  
Datové jednotky modelu Instalační služby systému Windows. Místo psaní skriptu procedury kopírování souborů a zápis položky registru, například vytváříte řádků a sloupců do tabulek databáze, které obsahují data souborů a registru.  
  
## <a name="database-entries"></a>Položky databáze  
 K instalaci VSPackage balíček Instalační služby systému Windows musí obsahovat položky databáze k provádění následujících úloh:  
  
-   Hledat systému k vyhledání verze [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] podporuje vašeho balíčku VSPackage (pomocí tabulek Instalační služby systému Windows, které zahrnují AppSearch CompLocator, RegLocator, DrLocator a podpis).  
  
-   Zrušit instalaci, pokud žádné podporovanou verzi [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] je nainstalovaná, nebo pokud jiné požadavky na systém ze sady VSPackage není splněná (pomocí tabulky LaunchCondition).  
  
-   Instalace balíčku VSPackage a závislé soubory (pomocí adresáře, komponenty a soubor tabulky).  
  
-   Přidejte do registru (pomocí tabulky registru) odpovídajícími informacemi pro sady VSPackage.  
  
-   Integrace sady VSPackage v [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] voláním **/Setup devenv.exe** (pomocí tabulky CustomAction).  
  
 Další informace najdete v tématu [Instalační služby systému Windows](http://msdn.microsoft.com/library/cc185688\(VS.85\).aspx).  
  
## <a name="setup-tools"></a>Instalační program nástroje  
 Různé nástroje třetích stran instalace nabízejí vývojové prostředí pro balíčky Instalační služby systému Windows. Dva bezplatné nástroje vám budou následující:  
  
-   InstallShield Limited Edition  
  
     Pomocí sady Visual Studio můžete získat omezenou verzi InstallShield **nový projekt** dialogového okna. Rozbalte **ostatní typy projektů** a pak vyberte **instalace a nasazení**. Vyberte šablonu InstallShield.  
  
-   Sada nástrojů XML pro Instalační službu systému Windows  
  
     Sada nástrojů sestavení balíčky Instalační služby systému Windows ze zdrojových souborů XML. Sada nástrojů je projekt open source Microsoftu. Stáhněte si zdrojový kód a spustitelné soubory z [ http://sourceforge.net/projects/wix ](http://sourceforge.net/projects/wix).  
  
 Pro komerční produkty, které se integrují do [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] pomocí [!INCLUDE[vsipsdk](../../includes/vsipsdk-md.md)], naleznete v tématu [ http://visualstudiogallery.com ](http://visualstudiogallery.com/).  
  
## <a name="see-also"></a>Viz také  
 [Instalace balíčků VSPackage pomocí Instalační služby systému Windows](../../extensibility/internals/installing-vspackages-with-windows-installer.md)

