---
title: ForEach&lt;T&gt; Návrhář aktivity | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.ForEach`1.UI
ms.assetid: 67097b3a-fcf5-4a72-beb1-2c7784151a86
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: b118eb62f3055486e26f9d90a4e3abb74fe38660
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668694"
---
# <a name="foreachlttgt-activity-designer"></a>ForEach&lt;T&gt; návrháře aktivit
<xref:System.Activities.Statements.ForEach%601> Aktivita provádí aktivity obsažené v jeho <xref:System.Activities.Statements.ForEach%601.Body%2A> pro každou položku v zadané <xref:System.Activities.Statements.ForEach%601.Values%2A> kolekce.  
  
## <a name="foreacht-properties-in-the-workflow-designer"></a>ForEach\<T > vlastnosti v Návrháři postupu provádění  
 V následující tabulce jsou uvedeny nejužitečnější <xref:System.Activities.Statements.ForEach%601> vlastnosti aktivit a popisuje, jak je používat v návrháři.  
  
|Název vlastnosti|Požadováno|Použití|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Popisný název <xref:System.Activities.Statements.ForEach%601> aktivity. Výchozí hodnota je ForEach\<Int32 >. I když <xref:System.Activities.Activity.DisplayName%2A> hodnota není bezpodmínečně nutné, je osvědčeným postupem je použití jednoho.|  
|<xref:System.Activities.Statements.ForEach%601.Values%2A>|Hodnota TRUE|Kolekce položek, které chcete iterovat. Chcete-li nastavit <xref:System.Activities.Statements.ForEach%601.Values%2A>, zadejte [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] výrazu v **hodnoty** pole na **ForEach\<T >** aktivity návrháře nebo v mřížce vlastností.|  
|*TypeArgument*|Hodnota TRUE|Typ položky v <xref:System.Activities.Statements.ForEach%601.Values%2A> kolekci specifikované souborem obecný parametr *T*. Ve výchozím nastavení *TypeArgument* je nastavena na **Int32**. Chcete-li změnit typ, změňte hodnotu *TypeArgument* – pole se seznamem v mřížce vlastností.|  
  
 Ve výchozím nastavení, iterace smyčky název **položky**. Můžete změnit název proměnné iterátoru v <xref:System.Activities.Statements.ForEach%601> návrháře aktivit. Iterace smyčky můžete použít ve výrazech v podřízených položek <xref:System.Activities.Statements.ForEach%601> aktivity.  
  
## <a name="see-also"></a>Viz také  
 [ParallelForEach\<T >](../workflow-designer/parallelforeach-t-activity-designer.md)   
 [Tok řízení](../workflow-designer/control-flow-activity-designers.md)