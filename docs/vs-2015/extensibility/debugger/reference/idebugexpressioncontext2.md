---
title: IDebugExpressionContext2 | Dokumentace Microsoftu
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
- IDebugExpressionContext2
helpviewer_keywords:
- IDebugExpressionContext2 interface
ms.assetid: 577fdaae-4b2d-4112-9839-ab899535fa6f
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8e69f15da81d95e92ffd344fc44b7aa1c44ccf8d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42671167"
---
# <a name="idebugexpressioncontext2"></a>IDebugExpressionContext2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugExpressionContext2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugexpressioncontext2).  
  
Toto rozhraní představuje kontext pro vyhodnocení výrazu.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugExpressionContext2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Ladicí stroj (DE) implementuje toto rozhraní představující kontext, ve kterém můžete vyhodnotit výraz.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Volání [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) vrátí tohoto rozhraní. Toto rozhraní je přístupný pouze v případě, že byl pozastaven laděnému programu a rámec zásobníku je k dispozici.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 V následující tabulce jsou uvedeny metody objektu `IDebugExpressionContext2`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[GetName –](../../../extensibility/debugger/reference/idebugexpressioncontext2-getname.md)|Načte název kontext vyhodnocení.|  
|[ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)|Analyzuje výrazu založený na textu pro hodnocení.|  
  
## <a name="remarks"></a>Poznámky  
 Objekt context hodnocení můžete představit jako obor pro provádění vyhodnocení výrazu.  
  
 Když program se zastavil, Správce ladění relace (SDM) získává rámec zásobníku z DE voláním [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md). Pak zavolá SDM [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) zobrazíte `IDebugExpressionContext2` rozhraní. Následuje volání [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) k vytvoření [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md) rozhraní, které představuje analyzovaný výraz, který je připravený k vyhodnocení.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md)   
 [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md)

