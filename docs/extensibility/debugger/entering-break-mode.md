---
title: "Režim pozastavení zadávání | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- break mode
- debugging [Debugging SDK], entering break mode
ms.assetid: e9a8a241-cd21-4d4e-999a-283554c288b1
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 33dd97cf627ae10e71a2aa2213a9763e86818b70
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="entering-break-mode"></a>Přejít do režimu pozastavení
Následující část popisuje proces, který nastane, když je zarážku došlo po zanoříte se do funkce, běží na řádek zdrojový kód, který se nachází kurzor nebo k zarážku.  
  
## <a name="break-mode-process"></a>Proces v režimu pozastavení  
  
1.  Modul ladění (DE) odešle [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md), [IDebugExceptionEvent2](../../extensibility/debugger/reference/idebugexceptionevent2.md), nebo jiná událost zastavení způsobí IDE k zadání režimu pozastavení.  
  
2.  SDM získá informace zásobníku volání z vlákna, následujícím způsobem:  
  
    -   [IDebugThread2::EnumFrameInfo](../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)  
  
    -   [IEnumDebugFrameInfo2::GetCount](../../extensibility/debugger/reference/ienumdebugframeinfo2-getcount.md)  
  
    -   [IEnumDebugFrameInfo2::Next](../../extensibility/debugger/reference/ienumdebugframeinfo2-next.md)  
  
    -   [IDebugStackFrame2::GetDocumentContext](../../extensibility/debugger/reference/idebugstackframe2-getdocumentcontext.md) získání informací o zdrojovém kódu  
  
    -   [IDebugDocumentContext2::GetName](../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md) získání názvu souboru  
  
    -   [IDebugDocumentContext2::GetStatementRange](../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md) získat rozsah – příkaz  
  
    -   [IDebugStackFrame2::GetCodeContext](../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md) získat informace o paměti  
  
## <a name="see-also"></a>Viz také  
 [Události volání ladicí program](../../extensibility/debugger/calling-debugger-events.md)