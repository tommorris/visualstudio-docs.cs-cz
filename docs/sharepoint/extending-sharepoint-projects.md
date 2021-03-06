---
title: Rozšíření projektů SharePoint | Microsoft Docs
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- projects [SharePoint development in Visual Studio], extending
- SharePoint development in Visual Studio, extending projects
- SharePoint projects, extending
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 76648e128db23415d6a986a7d0087968c549bd13
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2018
ms.locfileid: "36326005"
---
# <a name="extend-sharepoint-projects"></a>Rozšíření projektů služby SharePoint
  Vytváření rozšíření projektu, pokud chcete přizpůsobit funkce na úrovni projektu projektů SharePoint. Například můžete přidat vlastní vlastnosti projektu nebo reakce na události na úrovni projektu, které se vyvolá, když uživatel sama vyvinula řešení služby SharePoint v sadě Visual Studio.  
  
## <a name="create-project-extensions"></a>Vytváření rozšíření projektu
 Do rozšíření položky projektu, sestavení sestavení rozšíření sady Visual Studio, který implementuje <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> rozhraní. Další informace najdete v tématu [postupy: vytváření rozšíření projektu služby SharePoint](../sharepoint/how-to-create-a-sharepoint-project-extension.md).  
  
 Při vytváření rozšíření projektu, můžete také přidat následující funkce do projektů služby SharePoint:  
  
-   Přidání položky místní nabídky. Položky nabídky se zobrazí, když spustíte místní nabídce uzlu projektu služby SharePoint v **Průzkumníku řešení** tak, že kliknete pravým tlačítkem na uzel nebo výběr ho a pak vyberete **Shift** +  **F10** klíče. Další informace najdete v tématu [postupy: Přidání položky místní nabídky do projektů služby SharePoint](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md).  
  
-   Přidáte vlastní vlastnost. Vlastnost se zobrazí v **vlastnosti** okno když zvolíte projektu služby SharePoint v **Průzkumníku řešení**. Další informace najdete v tématu [postupy: Přidání vlastnosti do projektů služby SharePoint](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md).  
  
 Návod, jak vytvořit, nasadit a testování rozšíření projektu najdete v tématu [návod: vytváření rozšíření projektu služby SharePoint](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md).  
  
## <a name="understand-the-relationship-between-project-extensions-and-project-instances"></a>Pochopení vztah mezi rozšíření projektu a instancí projektu
 Při vytváření rozšíření projektu rozšíření načte, když jakýkoli druh projektu služby SharePoint je otevřen v [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] obsahuje několik šablon projektu služby SharePoint, jako je například seznam definic, typů obsahu a přijímače událostí. Je však pouze jeden typ projektu služby SharePoint. Typy projektů, které se zobrazují v **nový projekt** dialogové okno jsou pouze šablony, které váže dohromady jeden nebo více položek projektu služby SharePoint. Vzhledem k tomu, že existuje pouze jeden typ projektu služby SharePoint, rozšíření, které jsou vytvořené pro jeden projekt platí pro všechny projekty SharePoint. Nelze například vytvořit rozšíření, které se vztahuje se jenom **typ obsahu** projektu.  
  
 Pro přístup k instanci konkrétního projektu se zpracovat jeden z <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents> události *projectService* parametr ve vaší implementace nástroje <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension.Initialize%2A> metoda. Například pokud chcete zjistit, kdy je projektu služby SharePoint do řešení, zpracování <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectAdded> událostí. Další informace najdete v tématu [postupy: vytváření rozšíření projektu služby SharePoint](../sharepoint/how-to-create-a-sharepoint-project-extension.md).  
  
## <a name="see-also"></a>Viz také:
 [Postupy: vytváření rozšíření projektu SharePoint](../sharepoint/how-to-create-a-sharepoint-project-extension.md)   
 [Postupy: Přidání položky místní nabídky do projektů služby SharePoint](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md)   
 [Postupy: Přidání vlastnosti do projektů služby SharePoint](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md)   
 [Návod: Vytváření rozšíření projektu SharePoint](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md)   
 [Definování vlastních typů položek projektu služby SharePoint](../sharepoint/defining-custom-sharepoint-project-item-types.md)   
 [Rozšíření položek projektu služby SharePoint](../sharepoint/extending-sharepoint-project-items.md)   
 [Rozšíření balení a nasazení SharePoint](../sharepoint/extending-sharepoint-packaging-and-deployment.md)   
 [Rozšíření systému projektu služby SharePoint](../sharepoint/extending-the-sharepoint-project-system.md)  
  
  
