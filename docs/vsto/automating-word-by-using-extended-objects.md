---
title: Automatizace aplikace Word s použitím rozšířených objektů
ms.custom: ''
ms.date: 02/02/2017
ms.technology: office-development
ms.prod: visual-studio-dev15
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Word [Office development in Visual Studio], automating
- extended objects [Office development in Visual Studio], Word
- automation [Office development in Visual Studio], Word
- host items [Office development in Visual Studio], Word
- automating Word
- controls [Office development in Visual Studio], Word host controls
- host controls, Word
- host controls [Office development in Visual Studio], Word
- Word [Office development in Visual Studio], host controls
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 8ac9c610cdc7111eaeb5204e1b9d4fe6cde27a9c
ms.sourcegitcommit: 209c2c068ff0975994ed892b62aa9b834a7f6077
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/17/2018
ms.locfileid: "34264857"
---
# <a name="automate-word-by-using-extended-objects"></a>Automatizace aplikace Word s použitím rozšířených objektů
  Při vývoji řešení aplikace Word v sadě Visual Studio, můžete použít *hostitele položky* a *hostování ovládacího prvku*s v řešení. Jedná se o objekty, které rozšiřují určité běžně používané objekty ve model objektů aplikace Word (tedy model objektu zveřejněného prostřednictvím primární spolupracující sestavení pro aplikaci Word), jako například <xref:Microsoft.Office.Interop.Word.Document> a <xref:Microsoft.Office.Interop.Word.ContentControl> objekty. Rozšířené objekty chovají jako Word objekty, které jsou založené na, ale přidat další události a možnosti pro datové vazby k objektům.  
  
 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]  
  
 Hostitelských položek a hostitelských ovládacích prvků jsou k dispozici v doplňků VSTO a úpravy na úrovni dokumentů, i když se liší pro jednotlivé typy řešení kontext, ve kterém ty mohou být použity. Další informace najdete v tématu [hostitele položky a hostitelem Přehled ovládacích prvků](../vsto/host-items-and-host-controls-overview.md).  
  
## <a name="document-host-item"></a>Hostitelská položka Document  
 Přístup k udělení projekty aplikace Word <xref:Microsoft.Office.Tools.Word.Document> hostitelská položka. <xref:Microsoft.Office.Tools.Word.Document> Hostitelská položka slouží jako kontejner pro další ovládací prvky, včetně hostitelů a ovládacích prvků Windows Forms, a udržuje informace o ovládacích prvcích na jeho povrchu. <xref:Microsoft.Office.Tools.Word.Document> Hostitelská položka nabízí většinu členy stejné, jako <xref:Microsoft.Office.Interop.Word.Document> třída, která je odpovídající – třída v modelu objektů aplikace Word.  
  
 Další informace najdete v tématu [hostitelská položka Document](../vsto/document-host-item.md).  
  
## <a name="word-host-controls"></a>hostitelské ovládací prvky aplikace Word  
 Existuje několik hostitele ovládací prvky pro Word, které vám pomůžou vytvořit, organizovat a automatizovat dokumenty. Většina jejich funkce zahrnuje import, prezentace a chránit data. Tyto hostitelské ovládací prvky poskytují události a možnosti vazby dat, které nemají své protějšky v nativní model objektů aplikace Word.  
  
 V projektech na úrovni dokumentu přidáním jakékoli hostitelského ovládacího prvku do vašeho dokumentu v době návrhu nebo můžete přidat ovládací prvky obsahu a ovládacích prvků záložek za běhu. V doplňku VSTO projekty můžete přidat ovládací prvky obsahu a ovládacích prvků záložek do libovolného otevřete dokumentu za běhu.  
  
 Další informace o hostitelských ovládacích prvcích můžete použít v projekty aplikace Word, najdete v následujících tématech:  
  
-   [Ovládací prvky obsahu](../vsto/content-controls.md)  
  
-   [BOOKMARK – ovládací prvek](../vsto/bookmark-control.md)  
  
-   [XmlNode – ovládací prvek](../vsto/xmlnode-control.md)  
  
-   [XmlNodes – ovládací prvek](../vsto/xmlnodes-control.md)  
  
## <a name="see-also"></a>Viz také  
 [Postupy: Přidání ovládacích prvků obsahu do dokumentů aplikace Word](../vsto/how-to-add-content-controls-to-word-documents.md)   
 [Postupy: Přidání ovládacích prvků záložek do dokumentů aplikace Word](../vsto/how-to-add-bookmark-controls-to-word-documents.md)   
 [Postupy: Přidání ovládacích prvků XMLNode do dokumentů aplikace Word](../vsto/how-to-add-xmlnode-controls-to-word-documents.md)   
 [Postupy: Přidání ovládacích prvků XMLNodes do dokumentů aplikace Word](../vsto/how-to-add-xmlnodes-controls-to-word-documents.md)   
 [Postupy: Změna velikosti ovládacích prvků záložek](../vsto/how-to-resize-bookmark-controls.md)   
 [Návod: Vytvoření šablony s použitím ovládacích prvků obsahu](../vsto/walkthrough-creating-a-template-by-using-content-controls.md)   
 [Návod: Vytvoření vazby ovládacích prvků obsahu do vlastní části XML](../vsto/walkthrough-binding-content-controls-to-custom-xml-parts.md)   
 [Návod: Vytváření místních nabídek pro záložky](../vsto/walkthrough-creating-shortcut-menus-for-bookmarks.md)   
 [Řešení aplikace Word](../vsto/word-solutions.md)   
 [Přehled ovládacích prvků hostitele a hostitelské položky](../vsto/host-items-and-host-controls-overview.md)   
 [Programová omezení hostitelských položek a hostitelských ovládacích prvků](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)   
 [Rozšíření dokumentů aplikace Word a sešitů aplikace Excel v doplňcích VSTO za běhu](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)  
  
  