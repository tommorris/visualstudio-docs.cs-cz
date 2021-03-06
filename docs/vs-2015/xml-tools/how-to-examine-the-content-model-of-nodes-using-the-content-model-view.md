---
title: 'Postupy: prozkoumání modelu obsahu uzlů pomocí zobrazení modelu obsahu | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c42ddac8-b0e3-48d6-9832-112a19d6c104
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 25e47eed752a78caebcbae66a527cc847ac7d8f7
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42632396"
---
# <a name="how-to-examine-the-content-model-of-nodes-using-the-content-model-view"></a>Postupy: prozkoumání modelu obsahu uzlů pomocí zobrazení modelu obsahu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: prozkoumání modelu z uzlů pomocí zobrazení modelu obsahu](https://docs.microsoft.com/visualstudio/xml-tools/how-to-examine-the-content-model-of-nodes-using-the-content-model-view).  
  
  
Toto téma popisuje, jak prozkoumat uzly pomocí [zobrazení modelu obsahu](../xml-tools/content-model-view.md).  
  
### <a name="to-create-a-new-xsd-file-and-display-the-root-element-in-the-content-model-view"></a>Vytvořte nový soubor XSD a zobrazte kořenový element v zobrazení modelu obsahu  
  
1.  Vytvořte nový soubor schématu XML.  
  
2.  Klikněte na tlačítko **pomocí editoru XML k zobrazení a úpravě základního souboru schématu XML** na zobrazení spuštění.  
  
3.  Zkopírujte ukázkový kód XML schéma z [ukázky XML schématu: nákupní pořadí schématu](../xml-tools/sample-xsd-file-purchase-order-schema.md) a vložte ji nahradit kód, který byl přidán do nového souboru XSD ve výchozím nastavení.  
  
4.  Vyberte `purchaseOrder` element ve schématu Explorer kliknutím pravým tlačítkem myši `purchaseOrder` element v editoru XML a vyberete **zobrazit v Průzkumníkovi XML**.  
  
5.  Klikněte pravým tlačítkem myši `purchaseOrder` v Průzkumníku XML a vyberte **zobrazit v zobrazení modelu obsahu**.  
  
     Zobrazení modelu obsahu se zobrazí `purchaseOrder` prvek na jeho návrhovou plochu.  
  
6.  Rozbalte `shipTo`, `billTo`, a `items` uzlů poklepáním na každém uzlu nebo kliknutím na dvojitou šipku vpravo od každého uzlu.  
  
     Uzly `purchaseOrder` prvek nyní rozbaleny a zobrazí se model obsahu prvku.  
  
7.  Klikněte na libovolný uzel v rámci `purchaseOrder` elementu a podívejte se na panelu s popisem cesty chcete zobrazit, kde v sadě schémat vybraný uzel se nachází.  
  
8.  Klikněte na tlačítko **zobrazit dokumentaci** tlačítko na panelu nástrojů XSD, chcete-li přepnout jejich. Klikněte pravým tlačítkem na návrhové ploše, chcete-li přepnout v dokumentaci.  
  
9. Rick kliknutím `purchaseOrder` uzel a vyberte možnost **generovat ukázkové XML** zobrazíte instance dokumentu XML.



