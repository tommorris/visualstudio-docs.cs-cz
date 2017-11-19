---
title: "Postupy: vytváření nových dokumentů aplikace Visio prostřednictvím kódu programu | Microsoft Docs"
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
- Visio [Office development in Visual Studio], creating Visio documents
- documents [Office development in Visual Studio], creating Visio documents
ms.assetid: a0294d4c-be49-4cd0-b22e-3ec7568f3ec7
caps.latest.revision: "22"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: fa4a4d021ee0610d4fdd80a1966df6a8280c9523
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-programmatically-create-new-visio-documents"></a>Postupy: Vytváření nových dokumentů aplikace Visio prostřednictvím kódu programu
  Když vytváříte vykreslení dokumentu nové aplikace Microsoft Office Visio, přidejte do kolekce Microsoft.Office.Interop.Visio.Documents otevřené dokumenty Visio. V důsledku toho Microsoft.Office.Interop.Visio.Documents.Add metoda vytvoří novou vykreslování dokumentů aplikace Visio. Další informace najdete v tématu referenční dokumentaci VBA pro [Microsoft.Office.Interop.Visio.Documents.Add](http://msdn.microsoft.com/library/office/ff766868.aspx) metoda.  
  
## <a name="creating-new-blank-documents"></a>Vytvoření nové prázdné dokumenty  
  
#### <a name="to-create-a-new-document"></a>Chcete-li vytvořit nový dokument  
  
-   Použijte metodu Microsoft.Office.Interop.Visio.Documents.Add k vytvoření nového prázdného dokumentu, který není na základě šablony.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#1](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#1)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#1](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#1)]  
  
## <a name="creating-documents-copied-from-existing-documents"></a>Vytváření dokumentů zkopírovány z existující dokumentů  
 Metoda Microsoft.Office.Interop.Visio.Documents.Add můžete vytvořit nový dokument, který je kopií existujícího dokumentu aplikace Visio. Je třeba zadat název souboru a plně kvalifikovanou cestu diagramu.  
  
#### <a name="to-create-a-new-document-that-is-copied-from-an-existing-document"></a>Vytvořit nový dokument, který se zkopíruje z existujícího dokumentu  
  
-   Volání metody Microsoft.Office.Interop.Visio.Documents.Add a zadejte cestu diagram aplikace Visio.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#2](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#2)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#2](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#2)]  
  
## <a name="creating-stencils-copied-from-existing-stencils"></a>Vytváření vzorníky zkopírovány z existující vzorníky  
 [Microsoft.Office.Interop.Visio.Documents.Add](http://msdn.microsoft.com/library/office/ff766868.aspx) metoda můžete vytvořit nový vzorník, který je kopií existujícího vzorníku aplikace Visio. Je třeba zadat název souboru a plně kvalifikovanou cestu vzorníku.  
  
#### <a name="to-create-a-new-stencil-that-is-copied-from-an-existing-stencil"></a>Chcete-li vytvořit nový vzorník, která se zkopírují z existujícího vzorníku  
  
-   Volání metody Microsoft.Office.Interop.Visio.Documents.Add a zadejte cestu vzorníku.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#3](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#3)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#3](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#3)]  
  
## <a name="creating-documents-based-on-existing-templates"></a>Vytváření dokumentů na základě existujících šablon  
 Metoda Microsoft.Office.Interop.Visio.Documents.Add můžete vytvořit nový dokument (soubor .vsd), který je založen na existující šablony aplikace Visio (soubor VST). Tato metoda zkopíruje vzorníky, styly a nastavení, které jsou součástí šablony pracovního prostoru. Je třeba zadat název souboru a plně kvalifikovanou cestu šablony.  
  
#### <a name="to-create-a-new-document-that-is-based-on-an-existing-template"></a>Vytvořit nový dokument, který je založen na existující šablony  
  
-   Volání metody Microsoft.Office.Interop.Visio.Documents.Add a zadat cestu k šabloně.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#4](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#4)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#4](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#4)]  
  
## <a name="compiling-the-code"></a>Probíhá kompilace kódu  
 Tento příklad kódu vyžaduje následující:  
  
-   Dokumentů aplikace Visio s názvem `myDrawing.vsd` musí být umístěn v adresáři s názvem `Test` ve složce Dokumenty (pro Windows XP a starší) nebo ve složce Dokumenty (pro systém Windows Vista).  
  
-   Dokumentů aplikace Visio s názvem `myStencil.vss` musí být umístěn v adresáři s názvem `Test` ve složce Dokumenty (pro Windows XP a starší) nebo ve složce Dokumenty (pro systém Windows Vista).  
  
-   Dokumentů aplikace Visio s názvem `myTemplate.vst` musí být umístěn v adresáři s názvem `Test` ve složce Dokumenty (pro Windows XP a starší) nebo ve složce Dokumenty (pro systém Windows Vista).  
  
## <a name="see-also"></a>Viz také  
 [Řešení pro aplikaci Visio](../vsto/visio-solutions.md)   
 [Přehled modelu objektů aplikace Visio](../vsto/visio-object-model-overview.md)   
 [Postupy: otevírání dokumentů aplikace Visio prostřednictvím kódu programu](../vsto/how-to-programmatically-open-visio-documents.md)   
 [Postupy: zavírání dokumentů aplikace Visio prostřednictvím kódu programu](../vsto/how-to-programmatically-close-visio-documents.md)   
 [Postupy: ukládání dokumentů aplikace Visio prostřednictvím kódu programu](../vsto/how-to-programmatically-save-visio-documents.md)   
 [Postupy: tisk dokumentů aplikace Visio prostřednictvím kódu programu](../vsto/how-to-programmatically-print-visio-documents.md)  
  
  