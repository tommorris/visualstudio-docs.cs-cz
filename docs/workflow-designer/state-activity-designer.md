---
title: Návrhář postupu provádění – Návrhář stavu aktivity
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.State.UI
ms.assetid: 9455ab37-93a0-4c46-9eb8-b6611ca23167
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 9d4c919347b42229bd0c73164281f3cbf2254a66
ms.sourcegitcommit: 30f653d9625ba763f6b58f02fb74a24204d064ea
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/25/2018
ms.locfileid: "36757702"
---
# <a name="state-activity-designer"></a>Návrhář aktivity State

A <xref:System.Activities.Statements.State> představuje stavu, ve kterém může být stav stavového stroje v.

## <a name="using-the-state-activity-designer"></a>Pomocí návrháře stavu aktivity

Přidat <xref:System.Activities.Statements.State> do pracovního postupu, přetáhněte **stavu** Návrhář aktivity z **stavu počítače** části **sada nástrojů** a umístěte jej do <xref:System.Activities.Statements.StateMachine> aktivita na plochu návrháře pracovních postupů. A <xref:System.Activities.Statements.State> aktivity může být přetažen na <xref:System.Activities.Statements.StateMachine> a přechody přidat později; nebo přechod se dá vytvořit jako <xref:System.Activities.Statements.State> aktivity se ukončí. Přidat <xref:System.Activities.Statements.State> aktivity a vytvoření přechodu v jednom kroku, přetáhněte **stavu** aktivity z **stavový stroj** části **sada nástrojů** a pozastavte ukazatel myši nad jiného Stav v Návrháři pracovních postupů. Když taženou <xref:System.Activities.Statements.State> je oproti jinému <xref:System.Activities.Statements.State>, kolem druhé se zobrazí čtyři trojúhelníčky <xref:System.Activities.Statements.State>. Pokud <xref:System.Activities.Statements.State> vyřazen na jednom ze čtyř trojúhelníčky, se přidá do stavu počítače a vytvoření přechodu ze zdroje <xref:System.Activities.Statements.State> vynechaných cílovou <xref:System.Activities.Statements.State>. Další informace najdete v tématu [přechod](../workflow-designer/transition-activity-designer.md).

### <a name="state-activity-properties-in-the-workflow-designer"></a>Vlastnosti stavu aktivity v Návrháři pracovních postupů

Následující tabulce je zobrazena <xref:System.Activities.Statements.State> vlastnosti, které se dá nastavit pomocí návrháře pracovních postupů a popisuje, jak se používají v návrháři. Některé z těchto vlastností můžete upravovat v tabulce vlastností a lze upravit některé na plochu návrháře.

|Název vlastnosti|Požadováno|Použití|
|-------------------|--------------|-----------|
|<xref:System.Activities.Statements.State.DisplayName%2A>|False|Určuje popisný název <xref:System.Activities.Statements.State> Návrhář aktivity v hlavičce. Výchozí hodnota je **stavu**. Hodnota se dá upravit v mřížku vlastností, nebo přímo v hlavičce Návrhář aktivity. <xref:System.Activities.Statements.State.DisplayName%2A> Se používá v cestě, která se zobrazí v horní části návrháře pracovních postupů.<br /><br /> I když <xref:System.Activities.Statements.State.DisplayName%2A> striktně nevyžaduje, je osvědčeným postupem použít.|
|<xref:System.Activities.Statements.State.Entry%2A>|False|Určuje akci, která nastane, když je tento stav se kvůli. Při <xref:System.Activities.Statements.State> je rozšířena aktivity, tato hodnota se dá nastavit tak, že přetáhnete aktivitu z **sada nástrojů** a vyřadit ho do **položka** části stavu.|
|<xref:System.Activities.Statements.State.Exit%2A>|False|Určuje akci, která nastane, když tento stav převedena směrem od. Při <xref:System.Activities.Statements.State> je rozšířena aktivity, tato hodnota se dá nastavit tak, že přetáhnete aktivitu z **sada nástrojů** a vyřadit ho do **ukončovací** části stavu.|
|<xref:System.Activities.Statements.State.Transitions%2A>|False|Zobrazí seznam možných přechodů, které pocházejí z <xref:System.Activities.Statements.State>. Každá položka v seznamu obsahuje odkaz na přidruženého <xref:System.Activities.Statements.Transition> a cíl <xref:System.Activities.Statements.State>. Kliknutím na odkaz se změní návrháře rozbalené zobrazení <xref:System.Activities.Statements.Transition> nebo <xref:System.Activities.Statements.State>.|

## <a name="see-also"></a>Viz také:

- [StateMachine](../workflow-designer/statemachine-activity-designer.md)
- [FinalState](../workflow-designer/finalstate-activity-designer.md)
- [Přechod](../workflow-designer/transition-activity-designer.md)