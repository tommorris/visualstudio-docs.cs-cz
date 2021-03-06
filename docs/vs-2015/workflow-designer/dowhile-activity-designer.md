---
title: Návrhář aktivity DoWhile | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.DoWhile.UI
ms.assetid: 948deb35-d72f-462b-bea6-4b119c10a148
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 911e6d6d94090ddcdd43fcd9511624e209f7c03c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674110"
---
# <a name="dowhile-activity-designer"></a>Návrhář aktivity DoWhile
<xref:System.Activities.Statements.DoWhile> Aktivita provádí aktivity obsažené v jeho <xref:System.Activities.Statements.DoWhile.Body%2A> alespoň jednou, dokud je zadaná podmínka vyhodnocena jako **false**. Pokud potřebujete aktivity obsažené v těle smyčky mají být provedeny nulakrát nebo vícekrát, použijte <xref:System.Activities.Statements.While> aktivity místo.  
  
## <a name="dowhile-properties-in-the-workflow-designer"></a>Vlastnosti DoWhile v Návrháři postupu provádění  
 V následující tabulce jsou uvedeny nejužitečnější <xref:System.Activities.Statements.DoWhile> vlastnosti aktivit a popisuje, jak je používat v návrháři.  
  
|Název vlastnosti|Požadováno|Použití|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Statements.DoWhile.Body%2A>|False|Aktivity ke spuštění, dokud podmínka **true**. Chcete-li přidat <xref:System.Activities.Statements.DoWhile.Body%2A> aktivity, rozevírací aktivitu z panelu nástrojů do **tělo** pole na **DoWhile** Návrhář aktivity s text nápovědy "Aktivity Sem přetáhněte".|  
|<xref:System.Activities.Statements.DoWhile.Condition%2A>|Hodnota TRUE|Podmínka k vyhodnocení po každé iteraci smyčky. Chcete-li nastavit <xref:System.Activities.Statements.DoWhile.Condition%2A>, zadejte [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] výrazu v **podmínku** pole na **DoWhile** aktivity návrháře nebo v mřížce vlastností.|  
  
## <a name="see-also"></a>Viz také  
 [Při](../workflow-designer/while-activity-designer.md)   
 [Tok řízení](../workflow-designer/control-flow-activity-designers.md)