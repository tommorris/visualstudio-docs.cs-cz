---
title: Přizpůsobení úvodní stránky pro sadu Visual Studio | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.startpage
- VS.StartPage.HowDoI
- vs.ToolsOptionsPages.Startup
helpviewer_keywords:
- Start Page [Visual Studio]
- customizing Start Page [Visual Studio]
- Visual Studio Start page
ms.assetid: 925d42eb-ec34-426e-ad81-19db8630e536
caps.latest.revision: 48
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7bc8c27c98127bbbdfd7a1dddbab7124b8dc1d32
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629452"
---
# <a name="customizing-the-start-page-for-visual-studio"></a>Přizpůsobení úvodní stránky pro sadu Visual Studio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [přizpůsobení úvodní stránky pro sadu Visual Studio](https://docs.microsoft.com/visualstudio/ide/customizing-the-start-page-for-visual-studio).  
  
Můžete přizpůsobit úvodní stránku pro Visual Studio několika výchozími způsoby, například zobrazením **otevřít projekt** dialogové okno nebo otevřením řešení, který byl načten jako poslední. Můžete také zobrazit vlastní úvodní stránku, což je stránka XAML Windows Presentation Foundation (WPF) spuštěná v okně nástroje a lze v rámci ní spouštět interní příkazy sady Visual Studio.  
  
## <a name="customizing-the-default-start-page"></a>Přizpůsobení výchozí úvodní stránky  
  
1.  V panelu nabídky zvolte **nástroje**, **možnosti**.  
  
2.  Rozbalte **prostředí**a klikněte na tlačítko **spuštění**.  
  
3.  V **při spuštění** seznamu, zvolte položku pro přizpůsobení, které chcete.  
  
## <a name="show-a-custom-start-page"></a>Zobrazení vlastní úvodní stránky  
  
1.  Vlastní úvodní stránku nainstalujte jedním z následujících způsobů:  
  
    -   Nainstalujte ji z [Galerie sady Visual Studio](http://visualstudiogallery.msdn.microsoft.com/site/search?f%5B0%5D.Type=SearchText&f%5B0%5D.Value=start%20page), jiného webu nebo stránku na místním intranetu.  
  
        > [!NOTE]
        >  Pokud se vám líbí stránka, která je určena pro starší verzi sady Visual Studio, můžete stránku upgradovat pomocí sady Visual Studio SDK. Zobrazit [postupy: Upgrade vlastní úvodní stránku sady Visual Studio](../misc/how-to-upgrade-a-visual-studio-custom-start-page.md).  
  
         Otevřete soubor .vsix, který obsahuje vlastní úvodní stránku, nebo zkopírujte a vložte soubory úvodní stránky do **% USERPROFILE % Documents\Visual Studio 2015\StartPages** složky na vašem počítači.  
  
    -   Vytvořte si vlastní úvodní stránku, pokud jste nainstalovali sadu Visual Studio SDK.  
  
         Zobrazit [vytvářet své vlastní úvodní stránku](../misc/creating-your-own-start-page.md).  
  
2.  V panelu nabídky zvolte **nástroje**, **možnosti**.  
  
3.  Rozbalte **prostředí**a klikněte na tlačítko **spuštění**.  
  
4.  V **přizpůsobit úvodní stránku** , zvolte na stránce, který chcete.  
  
> [!NOTE]
>  Pokud chyba na vlastní úvodní stránce způsobí chybu sady Visual Studio, můžete sadu Visual Studio spustit v nouzovém režimu a pak ji nastavit tak, aby používala výchozí úvodní stránku. Zobrazit [/safemode (devenv.exe)](../ide/reference/safemode-devenv-exe.md).  
  
## <a name="see-also"></a>Viz také  
 [Přizpůsobení nastavení pro vývoj v sadě Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Vytvoření vlastní úvodní stránky](../misc/creating-your-own-start-page.md)



