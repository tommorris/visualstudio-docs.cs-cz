---
title: Návrhář aktivity stavu | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.State.UI
ms.assetid: 9455ab37-93a0-4c46-9eb8-b6611ca23167
caps.latest.revision: 5
author: steved0x
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 3c1d0019179d0a8e3f82001c371e760172251c2d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42686715"
---
# <a name="state-activity-designer"></a>Návrhář aktivity State
A <xref:System.Activities.Statements.State> představuje stavu, ve kterém může být stavového stroje v.  
  
## <a name="using-the-state-activity-designer"></a>Pomocí Návrhář aktivity State  
 Přidat <xref:System.Activities.Statements.State> do pracovního postupu, přetáhněte **stavu** Návrhář aktivity z **stavového stroje** část **nástrojů** a umístěte ho na <xref:System.Activities.Statements.StateMachine> aktivity [!INCLUDE[wfd1](../includes/wfd1-md.md)] povrchu. A <xref:System.Activities.Statements.State> aktivity může být přetaženy <xref:System.Activities.Statements.StateMachine> a přechody přidat později; nebo přechodu lze vytvořit jako <xref:System.Activities.Statements.State> aktivity se zahodí. Přidání <xref:System.Activities.Statements.State> aktivity a vytvoření přechodu v jednom kroku, přetáhněte **stavu** aktivita z **stavového stroje** část **nástrojů** a při najetí myší nad druhým Stav v Návrháři pracovních postupů. Když přetaženou <xref:System.Activities.Statements.State> je před jiným <xref:System.Activities.Statements.State>, čtyři trojúhelníky se zobrazí kolem nich <xref:System.Activities.Statements.State>. Pokud <xref:System.Activities.Statements.State> se ukončí na jednom ze čtyř trojúhelníků, přidá se do stavového stroje a vytvoření přechodu ze zdroje <xref:System.Activities.Statements.State> do vynechané cíle <xref:System.Activities.Statements.State>. Další informace najdete v tématu [přechod](../workflow-designer/transition-activity-designer.md).  
  
### <a name="state-activity-properties-in-the-workflow-designer"></a>Vlastnosti stavu aktivity v Návrháři postupu provádění  
 Následující tabulka ukazuje <xref:System.Activities.Statements.State> vlastnosti, které lze nastavit pomocí návrháře pracovních postupů a popisuje, jak se používají v návrháři. Některé z těchto vlastností můžete upravovat v mřížce vlastností a některé lze upravit na návrhové ploše.  
  
|Název vlastnosti|Požadováno|Použití|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Statements.State.DisplayName%2A>|False|Určuje popisný název <xref:System.Activities.Statements.State> návrháře aktivit v záhlaví. Výchozí hodnota je **stavu**. Hodnotu lze upravit v mřížce vlastností nebo přímo v hlavičce návrháře aktivit. <xref:System.Activities.Statements.State.DisplayName%2A> Se používá v navigace s popisem cesty, který se zobrazí v horní části návrháře postupu provádění.<br /><br /> I když <xref:System.Activities.Statements.State.DisplayName%2A> není bezpodmínečně nutné, je osvědčeným postupem je použití jednoho.|  
|<xref:System.Activities.Statements.State.Entry%2A>|False|Určuje akci, která nastane, pokud se tento stav je převeden na. Při <xref:System.Activities.Statements.State> aktivity rozbalen, tuto hodnotu můžete nastavit tak, že přetáhnete aktivity z **nástrojů** a vyřadit ho do **položka** oddíl stavu.|  
|<xref:System.Activities.Statements.State.Exit%2A>|False|Určuje akci, která nastane, pokud se tento stav se postoupí klávesou. Při <xref:System.Activities.Statements.State> aktivity rozbalen, tuto hodnotu můžete nastavit tak, že přetáhnete aktivity z **nástrojů** a vyřadit ho do **ukončovací** oddíl stavu.|  
|<xref:System.Activities.Statements.State.Transitions%2A>|False|Obsahuje seznam možných přechodů, které pocházejí z <xref:System.Activities.Statements.State>. Každá položka v seznamu obsahuje odkaz na přidruženou <xref:System.Activities.Statements.Transition> a cíl <xref:System.Activities.Statements.State>. Kliknutím na odkaz se přepnout návrháře na rozbalené zobrazení <xref:System.Activities.Statements.Transition> nebo <xref:System.Activities.Statements.State>.|  
  
## <a name="see-also"></a>Viz také  
 [Stavový stroj StateMachine](../workflow-designer/statemachine-activity-designer.md)   
 [FinalState](../workflow-designer/finalstate-activity-designer.md)   
 [Přechod](../workflow-designer/transition-activity-designer.md)