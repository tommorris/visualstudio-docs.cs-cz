---
title: 'Postupy: přizpůsobení balíčku řešení služby SharePoint pomocí cílů nástroje MSBuild | Microsoft Docs'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: a8842396d90eff6f3beb9c05e8916e48411e82bd
ms.sourcegitcommit: d9e4ea95d0ea70827de281754067309a517205a1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2018
ms.locfileid: "37120263"
---
# <a name="how-to-customize-a-sharepoint-solution-package-by-using-msbuild-targets"></a>Postupy: přizpůsobení balíčku řešení služby SharePoint pomocí cílů nástroje MSBuild
  Pomocí cílů nástroje MSBuild v příkazovém řádku lze přizpůsobit, jak Visual Studio vytvoří soubory balíčku SharePoint (*WSP*). Například můžete upravit vlastnosti nástroje MSBuild Chcete-li změnit adresář zprostředkující balení a skupiny nástroje MSBuild položky, které zadat výčtové soubory.  
  
## <a name="customize-and-run-msbuild-targets"></a>Přizpůsobení a spusťte cíle MSBuild  
 Pokud upravíte BeforeLayout a AfterLayout cíle, můžete provádět úlohy před rozložení balíčku, například přidání, odebrání nebo úprava souborů, které budou zabalené.  
  
#### <a name="to-customize-the-beforelayout-target"></a>Chcete-li přizpůsobit BeforeLayout cíl  
  
1.  Otevření editoru, jako je například Poznámkový blok a poté přidejte následující kód.  
  
    ```xml  
    <Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
      <Target Name="BeforeLayout">  
        <Message Importance="high" Text="In the BeforeLayout Target"></Message>  
      </Target>  
    </Project>  
    ```  
  
     Tento příklad zobrazí zprávu před balení tento cíl.  
  
2.  Název souboru **CustomLayout.SharePoint.targets**a pak ho uložte ve složce projektu služby SharePoint.  
  
3.  Otevřete projekt, otevřete jeho místní nabídce a potom zvolte **uvolnit projekt**.  
  
4.  V **Průzkumníku řešení**, otevřete místní nabídky projektu a zvolte **upravit**  *\<název projektu > .vbproj* nebo **upravit**  *\<Název projektu > .csproj*.  
  
5.  Po `Import` řádek u konce souboru projektu, přidejte následující řádek.  
  
    ```xml  
    <Import Project="CustomLayout.SharePoint.targets" />  
    ```  
  
6.  Uložte a zavřete soubor projektu.  
  
7.  V **Průzkumníku řešení**, otevřete místní nabídky projektu a zvolte **znovu načíst projekt**.  
  
 Při publikování tohoto projektu, zpráva se zobrazí ve výstupu před zahájením vytváření balíčků.  
  
#### <a name="to-customize-the-afterlayout-target"></a>Chcete-li přizpůsobit AfterLayout cíl  
  
1.  Na řádku nabídek zvolte **soubor** > **otevřete** > **soubor**.  
  
2.  V **otevření souboru** dialogové okno, přejděte do složky projektu, vyberte soubor, CustomLayout.target a potom zvolte **otevřete** tlačítko.  
  
3.  Těsně před `</Project>` značky, přidejte následující kód:  
  
    ```xml  
    <Target Name="AfterLayout">  
      <Message Importance="high" Text="In the AfterLayout Target"></Message>  
    </Target>  
    ```  
  
     Tento příklad zobrazí zprávu po zabalený tento cíl.  
  
4.  Uložte a zavřete soubor cíle.  
  
5.  Restartujte Visual Studio a pak otevřete projekt.  
  
 Při publikování tohoto projektu BeforeLayout zpráva se zobrazí před spuštěním balení a AfterLayout zpráva se zobrazí po dokončení vytváření balíčků.  
  
## <a name="see-also"></a>Viz také:
 [Zabalení a nasazení řešení služby SharePoint](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
  
