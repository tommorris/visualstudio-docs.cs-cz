---
title: "Rozšíření funkcí TableAdapter | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Visual Studio], TableAdapters
- data [Visual Studio], extending TableAdapters
- TableAdapters, adding functionality
ms.assetid: 418249c8-c7f3-47ef-a94c-744cb6fe6aaf
caps.latest.revision: "11"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 0fda0f47084370cd41440311f0cf31c43a69a408
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="extend-the-functionality-of-a-tableadapter"></a>Rozšíření funkcí TableAdapter
Funkce TableAdapter můžete rozšířit přidáním kód do souboru TableAdapter třídu.  
  
 Znovu vygeneruje kód, který definuje TableAdapter při provedení změny TableAdapter v **návrháře Dataset**, nebo když Průvodce upraví konfiguraci TableAdapter. Chcete-li zabránit odstranění během opětovné vygenerování TableAdapter kódu, přidejte kód do souboru TableAdapter třídu.  
  
 Částečné třídy povolit kód pro určité třídy rozdělit mezi několik fyzických souborů. Další informace najdete v tématu [částečné](/dotnet/visual-basic/language-reference/modifiers/partial) nebo [partial (typ)](/dotnet/csharp/language-reference/keywords/partial-type).  
  
## <a name="locate-tableadapters-in-code"></a>Vyhledejte TableAdapters v kódu  
 Během TableAdapters jsou navrženy s **návrháře Dataset**, TableAdapter třídy, které jsou generovány nejsou vnořené třídy <xref:System.Data.DataSet>. TableAdapters se nacházejí v oboru názvů založeného na názvu TableAdapter přidružené datové sady. Například pokud vaše aplikace obsahuje datovou sadu s názvem `HRDataSet`, TableAdapters umístěna na `HRDataSetTableAdapters` oboru názvů. (Tento vzor odpovídá zásady vytváření názvů: *DatasetName* + `TableAdapters`).  
  
 Následující příklad předpokládá TableAdapter s názvem `CustomersTableAdapter`je v projektu s `NorthwindDataSet`.  
  
#### <a name="to-create-a-partial-class-for-a-tableadapter"></a>Pro vytvoření částečné třídy pro TableAdapter  
  
1.  Přidejte novou třídu do projektu přechodem na **projektu** nabídky a výběrem **přidat třídu**.  
  
2.  Název třídy `CustomersTableAdapterExtended`.  
  
3.  Vyberte **přidat**.  
  
4.  Nahraďte kód správný obor názvů a název třídu pro váš projekt následujícím způsobem:  
  
     [!code-csharp[VbRaddataTableAdapters#2](../data-tools/codesnippet/CSharp/extend-the-functionality-of-a-tableadapter_1.cs)]
     [!code-vb[VbRaddataTableAdapters#2](../data-tools/codesnippet/VisualBasic/extend-the-functionality-of-a-tableadapter_1.vb)]  
  
## <a name="see-also"></a>Viz také  
 [Vyplnění datové sady s použitím objektů TableAdapters](../data-tools/fill-datasets-by-using-tableadapters.md)