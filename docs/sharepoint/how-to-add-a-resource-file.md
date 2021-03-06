---
title: 'Postupy: Přidání zdrojového souboru | Dokumentace Microsoftu'
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
- resource files [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, resource files
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 2a2a89a0c838a91559c6066bea341924e5ca627e
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/05/2018
ms.locfileid: "43774645"
---
# <a name="how-to-add-a-resource-file"></a>Postupy: Přidání zdrojového souboru
  Příkazy pro přidání souborů prostředků je v místní nabídce řešení uzlů a uzly funkce v Průzkumníku řešení. Další informace najdete v tématu [řešení služby SharePoint lokalizace](../sharepoint/localizing-sharepoint-solutions.md).  
  
### <a name="to-add-a-global-resource-file-to-a-sharepoint-solution"></a>Chcete-li přidat globální soubor prostředků pro řešení služby SharePoint  
  
1.  V [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], otevřete řešení služby SharePoint.  
  
2.  V **Průzkumníka řešení**, zvolte uzel projektu služby SharePoint a pak na panelu nabídek zvolte **projektu** > **přidat novou položku**.  
  
3.  V **přidat novou položku** dialogového okna zvolte **globální soubor prostředků** šablony a klikněte na tlačítko **přidat** tlačítko.  
  
    > [!NOTE]  
    >  Globální soubor prostředků šablony položky projektu se zobrazí, jenom když vyberete položku Sharepointového projektu.  
  
4.  V **přidat prostředek** dialogového okna zvolte jazykovou verzi pro soubor prostředků, jako je například angličtina (Spojené státy).  
  
     Tento krok přidává globální soubor prostředků do vašeho řešení ve formátu Resource_x_**.** _jazykovou verzi_**.** resx, jako jsou například *Resource1.en US.resx*.  
  
5.  Když **Editor prostředků** se otevře v [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], přidat prostředky do souboru prostředků.  
  
### <a name="to-add-a-feature-resource-file-to-a-sharepoint-feature"></a>Přidání souborů prostředků funkce do funkce služby SharePoint  
  
1.  Pokud řešení služby SharePoint již není otevřen v [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], otevřete řešení.  
  
2.  V **Průzkumníka řešení**, otevřete místní nabídku pro název funkce v rámci **funkce** uzel a klikněte na tlačítko **přidat prostředek funkce**.  
  
     Tento krok přidá soubor prostředků pro funkce ve formátu, _ResourceFileName_**.** _jazykovou verzi_**RESX**, jako jsou například *Feature1.en US.resx*.  
  
3.  Když **Editor prostředků** se otevře v [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], přidat prostředky do souboru prostředků.  
  
## <a name="see-also"></a>Viz také:
 [Vývoj řešení služby SharePoint](../sharepoint/developing-sharepoint-solutions.md)  
  
 
