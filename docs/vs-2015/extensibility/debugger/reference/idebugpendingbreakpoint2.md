---
title: IDebugPendingBreakpoint2 | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugPendingBreakpoint2
helpviewer_keywords:
- IDebugPendingBreakpoint2 interface
ms.assetid: d416b095-917e-475e-b796-ec0a03ffb8da
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f979af5789d6e695c5ca33c8cc9acdc74cc66815
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633570"
---
# <a name="idebugpendingbreakpoint2"></a>IDebugPendingBreakpoint2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugPendingBreakpoint2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugpendingbreakpoint2).  
  
Toto rozhraní představuje zarážku, která jsou připravená k vytvoření vazby na místa v kódu.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugPendingBreakpoint2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Ladicí stroj (DE) implementuje toto rozhraní jako součást jeho podporu pro zarážky.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Volání [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md) vytvoří čekající zarážkou ze [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md) rozhraní. Volání [svázat](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) vytvoří `IDebugBreakpoint2` rozhraní, které představuje vázaná zarážka v aplikaci.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 V následující tabulce jsou uvedeny metody objektu `IDebugPendingBreakpoint2`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[CanBind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md)|Určuje, zda tento čekající zarážka mohl vytvořit vazbu k umístění kódu.|  
|[Vytvoření vazby](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)|Vytvoří vazbu zarážka čeká na jeden nebo více umístění kódu.|  
|[GetState](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getstate.md)|Získá stav tohoto čekajících zarážek.|  
|[GetBreakpointRequest](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getbreakpointrequest.md)|Získá požadavek zarážku, která byla použita k vytvoření této čekající zarážka.|  
|[Virtualizovat](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-virtualize.md)|Přepíná virtualizované stavu tohoto objektu čekajících zarážek.|  
|[Povolit](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enable.md)|Přepíná povoleného stavu této čekající zarážka.|  
|[SetCondition](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setcondition.md)|Nastavuje nebo mění podmínky spojené s tímto čekajících zarážek.|  
|[SetPassCount](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setpasscount.md)|Nastavuje nebo mění pass počet, přidružený k tomuto čekajících zarážek.|  
|[EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)|Zobrazí všechny zarážky, které z této čekající zarážka vázána.|  
|[EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)|Zobrazí všechny zarážky chyb, které je výsledkem této čekající zarážka.|  
|[Odstranit](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-delete.md)|Odstraní tuto čekající zarážka a všechny zarážky, které jsou vázány z něj.|  
  
## <a name="remarks"></a>Poznámky  
 `IDebugPendingBreakpoint2` můžete představit jako poskytovatel všechny potřebné informace potřebné k vytvoření vazby zarážky na kód, který lze použít na jeden nebo více programů.  
  
 Čekající zarážkou může potenciálně způsobit více než jeden vázaná zarážka. Například zarážky v šabloně stylu C++ by mohla vést vázaná zarážka pro každou jedinečnou instanci této šablony.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md)   
 [GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointboundevent2-getpendingbreakpoint.md)   
 [GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getpendingbreakpoint.md)   
 [GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md)

