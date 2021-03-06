---
title: 'Postupy: Přidání stávajícího souboru modelu služby BDC do projektu služby SharePoint | Microsoft Docs'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.BDC.ImportDialog
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], import a model
- Business Data Connectivity service [SharePoint development in Visual Studio], reuse a model
- BDC [SharePoint development in Visual Studio], import a model
- BDC [SharePoint development in Visual Studio], remove a model
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 8f7508cf8c66343894c16da7ff840bd275abb65c
ms.sourcegitcommit: 30f653d9625ba763f6b58f02fb74a24204d064ea
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/25/2018
ms.locfileid: "36755895"
---
# <a name="how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project"></a>Postupy: Přidání stávajícího souboru modelu služby BDC do projektu služby SharePoint
  Můžete přizpůsobit, balíčků a znovu nasadit model Business Data Connectivity (BDC) pomocí sady Visual Studio přidat soubor modelu (*.bdcm*) k žádným projektem farmy služby SharePoint. Další informace najdete v tématu [vytvoření modelu připojení obchodních dat](../sharepoint/creating-a-business-data-connectivity-model.md).  
  
### <a name="to-add-a-bdc-model-file-to-a-sharepoint-project"></a>Přidání souboru modelu služby BDC do projektu služby SharePoint  
  
1.  V **Průzkumníku**, vyberte složku pro projektu služby SharePoint.  
  
2.  Na řádku nabídek zvolte **projektu** > **přidat existující položku**.  
  
3.  V **přidat existující položku** dialogové okno, přejděte do umístění, které chcete přidat do projektu, vyberte soubor a potom vyberte soubor definice modelu **přidat** tlačítko.  
  
     Pokud model není definována *obchodnímu systému (LOB) systému typu sestavení .NET*, **sestavení .NET přidat LobSystem** otevře se dialogové okno.  
  
4.  Pokud se zobrazí dialogové okno, proveďte jeden z následujících kroků:  
  
    -   Pokud chcete psát vlastní kód a pomocí návrháře definovat metadata pro importovaný model, vyberte **Ano** tlačítko, název systému a potom vyberte **OK** tlačítko.  
  
    -   Jinak, vyberte **ne** tlačítko a potom vyberte **OK** tlačítko.  
  
     **Modelu připojení obchodních dat** položka byla přidána do projektu.  
  
## <a name="see-also"></a>Viz také:
 [Vytvoření modelu připojení obchodních dat](../sharepoint/creating-a-business-data-connectivity-model.md)   
 [Postupy: vytvoření modelu služby BDC](../sharepoint/how-to-create-a-bdc-model.md)   
 [Postupy: určení lokalizovaných názvů, vlastností a oprávnění pomocí zdrojového souboru](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)   
 [Postupy: zahrnutí vlastního sestavení ve funkci BDC](../sharepoint/how-to-include-a-custom-assembly-in-a-bdc-feature.md)   
 [Integrace obchodních dat do služby SharePoint](../sharepoint/integrating-business-data-into-sharepoint.md)  
  
 
