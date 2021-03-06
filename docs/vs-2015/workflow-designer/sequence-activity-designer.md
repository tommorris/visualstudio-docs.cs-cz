---
title: Návrhář aktivity pořadí | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Sequence.UI
ms.assetid: 51c8d3cb-4d43-458f-9631-b63755f9ac94
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: d3f005ba61ad93eb2b1dd2663831b33a133b64e7
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674297"
---
# <a name="sequence-activity-designer"></a>Návrhář aktivity Sequence
<xref:System.Activities.Statements.Sequence> Aktivita obsahuje uspořádanou kolekci podřízené aktivity, které se provede v pořadí.  
  
 Dalším způsobem, jak provést sadu aktivit v pořadí se má používat <xref:System.Activities.Statements.Flowchart> aktivity. Zvažte použití [vývojový diagram](../workflow-designer/flowchart-activity-designer.md) Pokud máte jednoduchou větvení nebo opakování ve smyčce toku programu, který chcete model diagramem.  
  
## <a name="using-the-sequence-activity-designer"></a>Pomocí Návrhář aktivity Sequence  
 Přidat <xref:System.Activities.Statements.Sequence> aktivity, přetáhněte **pořadí** Návrhář aktivity z **nástrojů** a umístěte ho do [!INCLUDE[wfd1](../includes/wfd1-md.md)] povrchu. Chcete-li přidat podřízené aktivity k tomuto <xref:System.Activities.Statements.Sequence> aktivity, přetáhněte další aktivitu z **nástrojů** a umístěte ho na trojúhelník do pole text nápovědy "Sem přetáhněte aktivitu".  
  
### <a name="sequence-activity-properties-in-the-workflow-designer"></a>Vlastnosti aktivity pořadí v Návrháři postupu provádění  
 Následující tabulka ukazuje <xref:System.Activities.Statements.Sequence> vlastnosti a popisuje, jak se používají v návrháři. Tyto vlastnosti můžete upravit v mřížce vlastností nebo na návrhové ploše.  
  
|Název vlastnosti|Požadováno|Použití|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Určuje popisný název <xref:System.Activities.Statements.Sequence> návrháře aktivit v záhlaví. Výchozí hodnota je sekvence. Hodnotu lze upravit v mřížce vlastností nebo přímo v hlavičce návrháře aktivit.<br /><br /> I když <xref:System.Activities.Activity.DisplayName%2A> není bezpodmínečně nutné, je osvědčeným postupem je použití jednoho.|  
  
## <a name="see-also"></a>Viz také  
 [Vývojový diagram](../workflow-designer/flowchart-activity-designer.md)   
 [Tok řízení](../workflow-designer/control-flow-activity-designers.md)