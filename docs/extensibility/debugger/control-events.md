---
title: "Řízení události | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: debugging [Debugging SDK], events
ms.assetid: 0fc63484-5fb6-4887-9ea4-1905b459ca9d
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3220e3c6ef1a20b8a434fbfab13b419beb331032
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="control-events"></a>Události ovládacího prvku
Během provádění řízené vašeho programu musí odesílat události. Všechny události jsou odesílány s [IDebugEvent2](../../extensibility/debugger/reference/idebugevent2.md) rozhraní a mají atributy, které vyžadují, abyste implementovat [IDebugEvent2::GetAttributes](../../extensibility/debugger/reference/idebugevent2-getattributes.md) metoda.  
  
## <a name="additional-methods"></a>Další metody  
 Některé události vyžadovat provedení další metody, následujícím způsobem:  
  
-   Odesílání [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) rozhraní při inicializaci modulu ladění (DE) vyžaduje, abyste implementovat [IDebugEngineCreateEvent2::GetEngine](../../extensibility/debugger/reference/idebugenginecreateevent2-getengine.md) metoda.  
  
-   Řízení provádění vyžaduje implementaci takové události ovládacího prvku jako [IDebugBreakEvent2](../../extensibility/debugger/reference/idebugbreakevent2.md) a[IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) rozhraní. **IDebugBreakEvent2** se vyžaduje jenom pro asynchronní zalomení.  
  
-   Zanoříte se do funkce vyžaduje implementaci [IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) rozhraní a její metody.  
  
 Odvozování z zarážky události vyžadují implementace [IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md), [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md), a [IDebugBreakpointBoundEvent2](../../extensibility/debugger/reference/idebugbreakpointboundevent2.md) rozhraní, a taky [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../../extensibility/debugger/reference/idebugbreakpointboundevent2-getpendingbreakpoint.md) a [EnumBoundBreakpoints](../../extensibility/debugger/reference/idebugbreakpointboundevent2-enumboundbreakpoints.md) metody.  
  
 Vyhodnocení výrazu asynchronní vyžaduje, abyste implementovat [IDebugExpressionEvaluationCompleteEvent2](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) rozhraní a jeho [IDebugExpressionEvaluationCompleteEvent2::GetExpression](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getexpression.md) [a GetResult](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getresult.md) metody.  
  
 Synchronní události vyžadují implementace [IDebugEngine2::ContinueFromSynchronousEvent](../../extensibility/debugger/reference/idebugengine2-continuefromsynchronousevent.md) metoda.  
  
 Pro vaše modul pro zápis výstupu řetězec stylu musí implementovat [IDebugOutputStringEvent2::GetString](../../extensibility/debugger/reference/idebugoutputstringevent2-getstring.md) metoda.  
  
## <a name="see-also"></a>Viz také  
 [Řízení provádění a stavu vyhodnocení](../../extensibility/debugger/execution-control-and-state-evaluation.md)