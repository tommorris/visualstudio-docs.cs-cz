---
title: "Postupy: Přidání vlastních částí XML do přizpůsobení na úrovni dokumentu | Microsoft Docs"
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
- document-level customizations [Office development in Visual Studio], custom XML parts
- Office documents [Office development in Visual Studio, custom XML parts
- Word [Office development in Visual Studio], custom XML parts
- Excel [Office development in Visual Studio], custom XML parts
- custom XML parts [Office development in Visual Studio], adding
- documents [Office development in Visual Studio], custom XML parts
ms.assetid: e305a3d6-3a0e-4e72-ab8c-6a87a3590068
caps.latest.revision: "27"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: office
ms.openlocfilehash: b01646196e0bb755b351c02b4225a60bbfe1ad63
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-add-custom-xml-parts-to-document-level-customizations"></a>Postupy: Přidání vlastních částí XML do přizpůsobení na úrovni dokumentu
  Můžete uložit XML data v sešitu aplikace Microsoft Office Excel nebo dokument aplikace Microsoft Office Word tak, že vytvoříte vlastní část XML do přizpůsobení na úrovni dokumentu. Další informace najdete v tématu [přehled částí XML vlastní](../vsto/custom-xml-parts-overview.md).  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
> [!NOTE]  
>  Visual Studio neposkytuje projekty na úrovni dokumentu pro aplikaci Microsoft Office PowerPoint. Informace o přidání na vlastní část XML do Powerpointovou prezentaci pomocí doplňku VSTO najdete v tématu [postupy: Přidání vlastních částí XML do dokumentů podle pomocí doplňků VSTO](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md).  
  
### <a name="to-add-a-custom-xml-part-to-an-excel-workbook"></a>Chcete-li přidat vlastní část XML do sešitu aplikace Excel  
  
1.  Přidejte nový <xref:Microsoft.Office.Core.CustomXMLPart> do objektu <xref:Microsoft.Office.Core.CustomXMLParts> kolekce v sešitu. <xref:Microsoft.Office.Core.CustomXMLPart> Obsahuje řetězec XML, který chcete uložit v sešitu.  
  
     [!code-csharp[Trin_AddCustomXmlPartExcelDocLevel#1](../vsto/codesnippet/CSharp/Trin_AddCustomXmlPartExcelDocLevel/ThisWorkbook.cs#1)]
     [!code-vb[Trin_AddCustomXmlPartExcelDocLevel#1](../vsto/codesnippet/VisualBasic/Trin_AddCustomXmlPartExcelDocLevel/ThisWorkbook.vb#1)]  
  
2.  Přidat `AddCustomXmlPartToWorkbook` metodu `ThisWorkbook` – třída v projektech na úrovni dokumentu pro Excel.  
  
3.  Volejte metodu z jiných kódu v projektu. Například pokud chcete vytvořit vlastní část XML, když uživatel otevře sešit, volejte metodu z `ThisWorkbook_Startup` obslužné rutiny události.  
  
### <a name="to-add-a-custom-xml-part-to-a-word-document"></a>Přidat na vlastní část XML do dokumentů aplikace Word  
  
1.  Přidejte nový <xref:Microsoft.Office.Core.CustomXMLPart> do objektu <xref:Microsoft.Office.Core.CustomXMLParts> kolekce v dokumentu. <xref:Microsoft.Office.Core.CustomXMLPart> Obsahuje řetězec XML, který chcete uložit v dokumentu.  
  
     [!code-vb[Trin_AddCustomXmlPartWordDocLevel#1](../vsto/codesnippet/VisualBasic/Trin_AddCustomXmlPartWordDocLevel/ThisDocument.vb#1)]
     [!code-csharp[Trin_AddCustomXmlPartWordDocLevel#1](../vsto/codesnippet/CSharp/Trin_AddCustomXmlPartWordDocLevel/ThisDocument.cs#1)]  
  
2.  Přidat `AddCustomXmlPartToDocument` metodu `ThisDocument` – třída v projektech na úrovni dokumentu ve Wordu.  
  
3.  Volejte metodu z jiných kódu v projektu. Například pokud chcete vytvořit vlastní část XML, když uživatel otevře dokument, volejte metodu z `ThisDocument_Startup` obslužné rutiny události.  
  
## <a name="robust-programming"></a>Robustní programování  
 Pro zjednodušení tento příklad používá řetězec XML, který je definován jako místní proměnné v metodě. Obvykle opatřete si kód XML z externího zdroje, jako je například soubor nebo databázi.  
  
## <a name="see-also"></a>Viz také  
 [Přehled vlastních částí XML](../vsto/custom-xml-parts-overview.md)   
 [Návody: Přidání vlastních částí XML do dokumentů s použitím doplňků VSTO](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md)  
  
  