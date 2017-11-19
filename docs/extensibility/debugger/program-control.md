---
title: "Programové řízení | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: debugging [Debugging SDK], control of execution
ms.assetid: 6be80904-e66c-4cae-8891-1113b799fb01
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: cb69afe513010a7da4b4a85669bbc5f145f8dbc5
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="program-control"></a>Řízení programu
V sadě Visual Studio ladění, všechny následující krokování a budete pokračovat rutiny dochází na úrovni programu:  
  
-   Příkaz Další nastavení, to znamená, nastavení počítače na další instrukce spouštění v prostředí s konkrétní rámce  
  
-   Provádění, tedy budete pokračovat, ukončete z taktování režimu  
  
-   Krokování s na další pokyny  
  
-   Pokračovat s aktuální taktování režim  
  
-   Pozastavení vláken obsažený v programu  
  
-   Obnovení vláken obsažený v programu  
  
> [!NOTE]
>  Zobrazení zásobníku volání je implementováno na úrovni přístup z více vláken. Chcete-li provést výčet informací rámečku, při zobrazení zásobníku volání vlákna, musíte implementovat všechny metody [IEnumDebugFrameInfo2](../../extensibility/debugger/reference/ienumdebugframeinfo2.md) rozhraní.  
  
## <a name="methods-of-program-control"></a>Metody řízení programu  
 Následující tabulka uvádí metody [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) , je nutné implementovat pro modul minimálně funkční ladění (DE) a řízení provádění.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[IDebugProgram2::Execute](../../extensibility/debugger/reference/idebugprogram2-execute.md)|Pokračuje všechna vlákna obsažena program z zastaveném stavu. Vyžaduje se pro řízení provádění.|  
|[IDebugProgram2::Continue](../../extensibility/debugger/reference/idebugprogram2-continue.md)|Pokračuje všechna vlákna obsažena program z zastaveném stavu. Vyžaduje se pro řízení provádění.|  
|[IDebugProgram2::Step](../../extensibility/debugger/reference/idebugprogram2-step.md)|Krok provádí dané vlákno. Pokračuje všechna vlákna obsažený v programu. Vyžaduje se pro řízení provádění.|  
  
 Programy s více vlákny, je nutné také implementovat [IDebugProgram2::EnumThreads](../../extensibility/debugger/reference/idebugprogram2-enumthreads.md) metoda a všechny metody [IEnumDebugThreads2](../../extensibility/debugger/reference/ienumdebugthreads2.md) rozhraní.  
  
## <a name="see-also"></a>Viz také  
 [Řízení provádění a stavu vyhodnocení](../../extensibility/debugger/execution-control-and-state-evaluation.md)