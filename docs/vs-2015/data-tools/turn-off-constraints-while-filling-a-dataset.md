---
title: Vypnutí omezení při naplňování datové sady | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- DataRow.BeginEdit
- DataRow.EndEdit
- DataRow.CancelEdit
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- updating datasets, constraints
- constraints [Visual Basic], datasets
- datasets [Visual Basic], constraints
- constraints [Visual Basic], suspending during dataset update
ms.assetid: 553f7d0c-2faa-4c17-b226-dd02855bf1dc
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4b14830b7ed4922b4e383ef245c0366c184b606e
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668198"
---
# <a name="turn-off-constraints-while-filling-a-dataset"></a>Vypnutí omezení při naplňování datové sady
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [vypnutí omezení při naplňování datové sady](https://docs.microsoft.com/visualstudio/data-tools/turn-off-constraints-while-filling-a-dataset).  
  
  
Pokud datová sada obsahuje omezení (například omezení foreign key), theycan vyvolat chyby související s odpovídajícího pořadí operací, které jsou provedeny datové sadě. Například načítá podřízené záznamy před loadingrelated nadřazené záznamy může narušit omezení a způsobit chybu. Jakmile načtete podřízený záznam, omezení kontroluje související nadřazený záznam a vyvolá chybu.  
  
 Kdyby existovalo žádný mechanismus pro omezení dočasné pozastavení, by vyvolána chyba pokaždé, když se pokusila načíst záznam do podřízené tabulky. Dalším způsobem, jak pozastavit všechna omezení v datové sadě je <xref:System.Data.DataRow.BeginEdit%2A>, a <xref:System.Data.DataRow.EndEdit%2A> vlastnosti.  
  
> [!NOTE]
>  Události ověření (třeba <xref:System.Data.DataTable.ColumnChanging> a<xref:System.Data.DataTable.RowChanging>) nebude vyvolána, když jsou vypnuté omezení.  
  
### <a name="to-suspend-update-constraints-programmatically"></a>Pozastavit aktualizace omezení prostřednictvím kódu programu  
  
-   Následující příklad ukazuje, jak dočasně vypnout kontrolu v datové sadě omezení:  
  
     [!code-csharp[VbRaddataEditing#10](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataEditing/CS/Form1.cs#10)]
     [!code-vb[VbRaddataEditing#10](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataEditing/VB/Form1.vb#10)]  
  
### <a name="to-suspend-update-constraints-using-the-dataset-designer"></a>Pozastavit aktualizace omezení pomocí návrháře datových sad  
  
1.  Otevřete svou datovou sadu v [vytváření a úpravy typované datové sady](../data-tools/creating-and-editing-typed-datasets.md). Další informace najdete v tématu [postupy: otevření datové sady v návrháři datových sad](http://msdn.microsoft.com/library/36fc266f-365b-42cb-aebb-c993dc2c47c3).  
  
2.  V **vlastnosti** okno, nastaveno <xref:System.Data.DataSet.EnforceConstraints%2A> vlastnost `false`.  
  
## <a name="see-also"></a>Viz také  
 [Vyplnění datové sady s použitím objektů TableAdapter](../data-tools/fill-datasets-by-using-tableadapters.md)   
 [Vztahy v datových sadách](../data-tools/relationships-in-datasets.md)

