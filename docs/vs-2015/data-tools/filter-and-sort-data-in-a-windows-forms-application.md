---
title: Filtrování a řazení dat v aplikaci Windows Forms | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- row states, filtering
- data views, sorting
- row version, filtering
- row states
- data views, filtering
- sorting datasets, using data views
- dataset filtering, using data views
ms.assetid: f4f100f1-776d-46dc-b2fd-5b35b98d9561
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: e32e64672fc01f328643e78e572e12d57b751f39
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42696372"
---
# <a name="filter-and-sort-data-in-a-windows-forms-application"></a>Filtrování a řazení dat ve formulářové aplikaci Windows
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [filtrování a řazení dat v aplikaci Windows Forms](https://docs.microsoft.com/visualstudio/data-tools/filter-and-sort-data-in-a-windows-forms-application).  
  
  
Filtrování dat tím, že nastavíte <xref:System.Windows.Forms.BindingSource.Filter%2A> řetězcového výrazu, které vrací záznamy požadovanou vlastnost.  
  
 Řazení dat tím, že nastavíte <xref:System.Windows.Forms.BindingSource.Sort%2A> vlastnost na název sloupce chcete řadit, připojit `DESC` seřadit v sestupném pořadí, nebo připojit `ASC` seřadit v vzestupném pořadí.  
  
> [!NOTE]
>  Pokud vaše aplikace nepoužívá <xref:System.Windows.Forms.BindingSource> součásti, můžete filtrovat a řadit data s využitím <xref:System.Data.DataView> objekty. Další informace najdete v tématu [zobrazení dat](http://msdn.microsoft.com/library/0fe5dfa2-c1cd-435f-90b6-b4dd2e3ef34b).  
  
## <a name="to-filter-data-by-using-a-bindingsource-component"></a>K filtrování dat pomocí komponenty BindingSource  
  
-   Nastavte <xref:System.Windows.Forms.BindingSource.Filter%2A> vlastnost na výraz, který chcete vrátit. Například následující kód vrátí zákazníkům `CompanyName` , který začíná písmenem "B":  
  
     [!code-csharp[VbRaddataDisplaying#6](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataDisplaying/CS/Form1.cs#6)]
     [!code-vb[VbRaddataDisplaying#6](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataDisplaying/VB/Form1.vb#6)]  
  
## <a name="to-sort-data-by-using-a-bindingsource-component"></a>Řazení dat s použitím komponenty BindingSource  
  
-   Nastavte <xref:System.Windows.Forms.BindingSource.Sort%2A> vlastnost do sloupce, které chcete řadit. Například následující kód se seřadí zákazníci `CompanyName` sloupec v sestupném pořadí:  
  
     [!code-csharp[VbRaddataDisplaying#7](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataDisplaying/CS/Form1.cs#7)]
     [!code-vb[VbRaddataDisplaying#7](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataDisplaying/VB/Form1.vb#7)]  
  
## <a name="see-also"></a>Viz také  
 [Vytvoření vazby ovládacích prvků k datům v sadě Visual Studio](../data-tools/bind-controls-to-data-in-visual-studio.md)

