---
title: Instalace sady Visual Studio verze vedle sebe | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-install
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- side-by-side installations [Visual Studio]
- Help [Visual Studio], installing
- install multiple versions of Visual Studio
ms.assetid: 4d00f240-4910-4699-aaf3-cda6461f0c29
caps.latest.revision: 48
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: ae67e83b2f1444c09129ed5242afac2c3939c954
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674632"
---
# <a name="install-visual-studio-versions-side-by-side"></a>Instalace sady Visual Studio verze vedle sebe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tuto verzi sady Visual Studio můžete nainstalovat na počítači s již nainstalovanou starší verzí. Pokud dojde k selhání instalace, můžete použít [nástroj pro shromažďování protokolů](http://go.microsoft.com/fwlink/?LinkId=262077) ke shromažďování informací o selhání a tak mohou problémy ladit sami.  
  
> [!NOTE]
>  Doporučujeme, abyste nainstalovali [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] verze v pořadí, ve kterém byly vydány. Například Visual Studio 2013 nainstalujte před instalací sady Visual Studio 2015.  
  
 Před instalací verzí vedle sebe, zkontrolujte následující podmínky:  
  
-   Pokud používáte Visual Studio 2015 otevřete řešení, který byl vytvořen v [!INCLUDE[vs_dev12](../includes/vs-dev12-md.md)], můžete později otevřít a upravit toto řešení znovu ve starší verzi, dokud jste neimplementovali žádné funkce, které jsou specifické pro Visual Studio 2015.  
  
-   Pokud se pokusíte použít Visual Studio 2015 otevřete řešení, který byl vytvořen v [!INCLUDE[vs_dev12](../includes/vs-dev12-md.md)] nebo starší verzi, možná budete muset upravit projekty a soubory kompatibilní s Visual Studiem 2015. Další informace najdete v tématu [Port, migrace a Upgrade projektů sady Visual Studio](../misc/port-migrate-and-upgrade-visual-studio-projects-in-visual-studio-15-rc.md) stránky.  
  
-   Pokud odinstalujete verzi [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] na počítači, který má více než jedna verze nainstalovaná, přidružení souborů pro [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] se odeberou pro všechny verze. Přiřazení těchto souborů můžete přemapovat pomocí **obnovit přidružení souborů** tlačítko **prostředí**, **Obecné** stránku [možnosti](../ide/reference/general-environment-options-dialog-box.md) dialogové okno.  
  
-   Visual Studio neprovádí automatický upgrade rozšíření vzhledem k tomu, že ne všechna rozšíření jsou kompatibilní. Je třeba přeinstalovat rozšíření od [Galerie sady Visual Studio](http://go.microsoft.com/fwlink/?LinkId=178891) nebo vydavatele softwaru.  
  
## <a name="net-framework-versions-and-side-by-side-installations"></a>Verze rozhraní .NET framework a instalacemi nevyžádaného vedle sebe  
  
-   Projekty Visual Basic, Visual C# a Visual F # používají **Cílová architektura** možnost **Návrháře projektu** k určení, kterou verzi rozhraní .NET Framework projekt používá. Pro projekt jazyka C++ můžete ručně změnit cílové rozhraní úpravou souboru .vcxproj. Další informace najdete v tématu [Kompatibilita verzí](http://msdn.microsoft.com/library/2f25e522-456a-48c3-8a53-e5f39275649f).  
  
     Když vytvoříte projekt, můžete určit, kterou verzi rozhraní .NET Framework je projekt cílen v **rozhraní .NET Framework** v seznamu **nový projekt** dialogové okno.  
  
     Informace specifické pro jazyk najdete v příslušném tématu v následující tabulce.  
  
    |Jazyk|Téma|  
    |--------------|-----------|  
    |[!INCLUDE[vbprvb](../includes/vbprvb-md.md)]|[Stránka Aplikace, Návrhář projektu (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md)|  
    |Visual C#|[Stránka Aplikace, Návrhář projektu (C#)](../ide/reference/application-page-project-designer-csharp.md)|  
    |Visual F#|[Konfigurace projektů](http://msdn.microsoft.com/library/a1489abb-6294-4f8f-b71f-2cb126393526)|  
    |C++|[Postupy: Změna cílové architektury a sady nástrojů](http://msdn.microsoft.com/library/031b1d54-e6e1-4da7-9868-3e75a87d9ffe)|  
    |[!INCLUDE[jsprjscript](../includes/jsprjscript-md.md)]|[Spuštění aplikace JScript na předchozí verzi modulu Common Language Runtime](http://msdn.microsoft.com/en-us/bbea51b5-ac03-4e6c-b9a6-f487ef63eda5)|  
  
## <a name="see-also"></a>Viz také  
 [Instalace sady Visual Studio](../install/install-visual-studio-2015.md) [přenos, migrace a Upgrade projektů sady Visual Studio](../misc/port-migrate-and-upgrade-visual-studio-projects-in-visual-studio-15-rc.md)   
 [Sestavení C/C++ izolovaných aplikací a sestavení vedle sebe](http://msdn.microsoft.com/library/9465904e-76f7-48bd-bb3f-c55d8f1699b6)   
 [Přizpůsobení nastavení pro vývoj v sadě Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3)