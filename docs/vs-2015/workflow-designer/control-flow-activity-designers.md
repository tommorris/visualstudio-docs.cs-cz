---
title: Návrháři aktivit toku řízení | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ba74af23-5398-4e62-bd90-c50612e3bfef
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 58ddd15d37e36494fef9488638727c7bc2142aa3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675641"
---
# <a name="control-flow-activity-designers"></a>Návrháři aktivit toku řízení
[!INCLUDE[wfd1](../includes/wfd1-md.md)] obsahuje několik poskytované systémem aktivit, které můžete použít při vytváření pracovního postupu. Tato část obsahuje poskytované systémem aktivit používaných pro řízení toku v rámci pracovního postupu. Následující témata obsahují jejich popis a pokyny, jak je používat.  
  
## <a name="in-this-section"></a>V tomto oddílu  
 [DoWhile](../workflow-designer/dowhile-activity-designer.md)  
 Spustí aktivitu obsažené v těle alespoň jednou, dokud je zadaná podmínka vyhodnocena jako **true**.  
  
 [ForEach\<T >](http://msdn.microsoft.com/en-us/a680cddd-2760-497a-b27b-c023fcbc6f33)  
 Spustí aktivitu obsažené v těle pro každou položku v zadané kolekci.  
  
 [If](../workflow-designer/if-activity-designer.md)  
 Vyhodnocuje podmínku a provede aktivitu v závislosti na výsledcích hodnocení.  
  
 [paralelní](../workflow-designer/parallel-activity-designer.md)  
 Souběžně spustí sadu podřízených aktivit.  
  
 [ParallelForEach\<T>](../workflow-designer/parallelforeach-t-activity-designer.md)  
 Vytvoří výčet prvků kolekce a spustí vloženým příkazem pro každý prvek kolekce paralelně  
  
 [Výběr](../workflow-designer/pick-activity-designer.md)  
 Spustí jednu s několika větvemi v reakci na nějakou událost, která poskytuje řízení toku založeného na událostech.  
  
 [Operace PickBranch](../workflow-designer/pickbranch-activity-designer.md)  
 Poskytuje potenciální cesta provádění v rámci <xref:System.Activities.Statements.Pick> aktivity.  
  
 [Pořadí](../workflow-designer/sequence-activity-designer.md)  
 Obsahuje uspořádanou kolekci podřízené aktivity, které se provede v pořadí.  
  
 [Přepínač\<T >](http://msdn.microsoft.com/en-us/ce1aa634-c4db-4475-a1c8-a88478a57212)  
 Vyhodnotí zadaný výraz a spustí aktivity z kolekce aktivit, jejichž přidružené klíč odpovídá hodnotě získané z hodnocení.  
  
 [Při](../workflow-designer/while-activity-designer.md)  
 Spustí aktivitu obsažené v těle, když je zadaná podmínka vyhodnocena jako **true**.  
  
## <a name="reference"></a>Odkaz  
 <xref:System.Activities.Activity>  
  
 <xref:System.Activities.Statements.DoWhile>  
  
 <xref:System.Activities.Statements.ForEach%601>  
  
 <xref:System.Activities.Statements.If>  
  
 <xref:System.Activities.Statements.Parallel>  
  
 <xref:System.Activities.Statements.ParallelForEach%601>  
  
 <xref:System.Activities.Statements.Pick>  
  
 <xref:System.Activities.Statements.PickBranch>  
  
 <xref:System.Activities.Statements.Sequence>  
  
 <xref:System.Activities.Statements.Switch%601>  
  
 <xref:System.Activities.Statements.While>  
  
## <a name="related-sections"></a>Související oddíly  
 U jiných typů návrháři aktivit naleznete v následujících tématech.  
  
 [Používání návrhářů aktivit](../workflow-designer/using-the-activity-designers.md)  
  
 [Vývojový diagram](../workflow-designer/flowchart-activity-designers.md)  
  
 [Zasílání zpráv](../workflow-designer/messaging-activity-designers.md)  
  
 [Modul runtime](../workflow-designer/runtime-activity-designers.md)  
  
 [Primitivní elementy](../workflow-designer/primitives-activity-designers.md)  
  
 [Transakce](../workflow-designer/transaction-activity-designers.md)  
  
 [Kolekce](../workflow-designer/collection-activity-designers.md)  
  
 [Zpracování chyb](../workflow-designer/error-handling-activity-designers.md)  
  
## <a name="external-resources"></a>Externí zdroje  
 [Používání návrhářů aktivit](../workflow-designer/using-the-activity-designers.md)