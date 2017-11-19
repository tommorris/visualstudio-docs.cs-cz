---
title: "Postupy: Přidání ovládacích prvků graf do listů | Microsoft Docs"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Chart control [Office development in Visual Studio], adding to worksheets
- controls [Office development in Visual Studio], adding to worksheets
ms.assetid: f02568e7-5caa-45b4-aa2a-4f73b0565d4e
caps.latest.revision: "44"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 1ba31b5577090c3aef01ad974ba51a72e6f9980e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-add-chart-controls-to-worksheets"></a>Postupy: Přidání ovládacích prvků Graf do listů
  Můžete přidat <xref:Microsoft.Office.Tools.Excel.Chart> ovládacích prvků na list aplikace Microsoft Office Excel v době návrhu a v době běhu v přizpůsobeních na úrovni dokumentu. Můžete také přidat <xref:Microsoft.Office.Tools.Excel.Chart> ovládacích prvků za běhu v doplňcích VSTO.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
 Toto téma popisuje následující úlohy:  
  
-   [Přidání ovládacích prvků grafu v době návrhu](#designtime)  
  
-   [Přidání ovládacích prvků graf za běhu v projektech na úrovni dokumentu](#runtimedoclevel)  
  
-   [Přidání ovládacích prvků graf za běhu v projektu doplňku VSTO](#runtimeaddin)  
  
 Další informace o <xref:Microsoft.Office.Tools.Excel.Chart> najdete v části ovládací prvky, [ovládací prvek graf](../vsto/chart-control.md).  
  
##  <a name="designtime"></a>Přidání ovládacích prvků grafu v době návrhu  
 Můžete přidat <xref:Microsoft.Office.Tools.Excel.Chart> ovládacího prvku do listu stejným způsobem, měli byste přidat graf z v aplikaci.  
  
> [!NOTE]  
>  <xref:Microsoft.Office.Tools.Excel.Chart> Ovládací prvek není k dispozici **sada nástrojů** nebo **zdroje dat** okno.  
  
#### <a name="to-add-a-chart-host-control-to-a-worksheet-in-excel"></a>Přidání ovládacího prvku grafu hostitele do sešitu v aplikaci Excel  
  
1.  Na **vložit** ve **grafy** klikněte na možnost **sloupec**, klikněte na kategorii grafů a pak klikněte na typ grafu chcete.  
  
2.  V **vložit graf** dialogové okno, klikněte na tlačítko **OK**.  
  
3.  Na **návrhu** ve **Data** klikněte na možnost **vyberte Data**.  
  
4.  V **vybrat zdroj dat** dialogové okno, klikněte v **grafu** **oblast dat** a zrušte všechny výchozí výběr.  
  
5.  V **Data grafu** list, vyberte oblast buněk, která obsahuje data grafu (buněk **A5** prostřednictvím **D8**).  
  
6.  V **vybrat zdroj dat** dialogové okno, klikněte na tlačítko **OK**.  
  
##  <a name="runtimedoclevel"></a>Přidání ovládacích prvků graf za běhu v projektech na úrovni dokumentu  
 Můžete přidat <xref:Microsoft.Office.Tools.Excel.Chart> řízení dynamicky za běhu. V dokumentu nejsou trvalé dynamicky vytvořený grafy jako umisťování ovládacích prvků při zavření dokumentu. Další informace najdete v tématu [přidání ovládacích prvků do dokumentů Office za běhu](../vsto/adding-controls-to-office-documents-at-run-time.md).  
  
#### <a name="to-add-a-chart-control-to-a-worksheet-programmatically"></a>Přidání ovládacího prvku grafu do listu prostřednictvím kódu programu  
  
1.  V <xref:Microsoft.Office.Tools.Excel.Worksheet.Startup> obslužné rutiny události z `Sheet1`, vložte následující kód do přidat <xref:Microsoft.Office.Tools.Excel.Chart> ovládacího prvku.  
  
     [!code-csharp[Trin_VstcoreHostControlsExcel#1](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#1)]
     [!code-vb[Trin_VstcoreHostControlsExcel#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#1)]  
  
##  <a name="runtimeaddin"></a>Přidání ovládacích prvků graf za běhu v projektu doplňku VSTO  
 Můžete přidat <xref:Microsoft.Office.Tools.Excel.Chart> řízení prostřednictvím kódu programu k žádné otevřete sešit v projektu doplňku VSTO. Další informace najdete v tématu [rozšíření dokumentů aplikace Word a sešitů aplikace Excel v doplňcích VSTO za běhu](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).  
  
 Ovládací prvky dynamicky vytvořený grafu nejsou trvalé do listu jako umisťování ovládacích prvků při uzavření listu. Další informace najdete v tématu [přidání ovládacích prvků do dokumentů Office za běhu](../vsto/adding-controls-to-office-documents-at-run-time.md).  
  
#### <a name="to-add-a-chart-control-to-a-worksheet-programmatically"></a>Přidání ovládacího prvku grafu do listu prostřednictvím kódu programu  
  
1.  Následující kód vytvoří hostitelská položka worksheet, která je založena na otevřete list a pak přidá <xref:Microsoft.Office.Tools.Excel.Chart> ovládacího prvku.  
  
     [!code-csharp[Trin_Excel_Dynamic_Controls#9](../vsto/codesnippet/CSharp/Trin_Excel_Dynamic_Controls/ThisAddIn.cs#9)]
     [!code-vb[Trin_Excel_Dynamic_Controls#9](../vsto/codesnippet/VisualBasic/Trin_Excel_Dynamic_Controls/ThisAddIn.vb#9)]  
  
## <a name="compiling-the-code"></a>Probíhá kompilace kódu  
 V tomto příkladu má následující požadavky:  
  
-   Data grafu zobrazena, uložené v rozsahu od A5 do D8 v listu.  
  
## <a name="see-also"></a>Viz také  
 [Rozšíření dokumentů aplikace Word a sešitů aplikace Excel v doplňcích VSTO za běhu](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)   
 [Ovládací prvky v dokumentech Office](../vsto/controls-on-office-documents.md)   
 [Ovládací prvek graf](../vsto/chart-control.md)   
 [Automatizace aplikace Excel s použitím rozšířených objektů](../vsto/automating-excel-by-using-extended-objects.md)   
 [Přehled ovládacích prvků hostitele a hostitelské položky](../vsto/host-items-and-host-controls-overview.md)   
 [Vazba dat k ovládacím prvkům v řešeních pro systém Office](../vsto/binding-data-to-controls-in-office-solutions.md)   
 [Programová omezení hostitelských položek a hostitelských ovládacích prvků](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)  
  
  