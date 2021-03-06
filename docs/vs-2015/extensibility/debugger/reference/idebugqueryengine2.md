---
title: IDebugQueryEngine2 | Dokumentace Microsoftu
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
- IDebugQueryEngine2
helpviewer_keywords:
- IDebugQueryEngine2 interface
ms.assetid: 8f0e1838-a818-4459-9138-a3dceb7408de
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f80e8b44326cb082c8f6428365bad2575c317da6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668945"
---
# <a name="idebugqueryengine2"></a>IDebugQueryEngine2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugQueryEngine2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugqueryengine2).  
  
Toto rozhraní umožňuje relace ladění správci načíst rozhraní, které představuje ladicího stroje (DE).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugQueryEngine2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 DE implementuje toto rozhraní pro objekty, které implementují rozhraní nejběžnější DE (například [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md), [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md), a [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)) v pořadí pro povolení přístupu k [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) rozhraní DE samotný.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Volání [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) na typické DE rozhraní k získání tohoto rozhraní.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 V následující tabulce jsou uvedeny metody objektu `IDebugQueryEngine2`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[GetEngineInterface](../../../extensibility/debugger/reference/idebugqueryengine2-getengineinterface.md)|Získá rozhraním vlastního ladicího stroje (DE).|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní je zpravidla implementovaní v objektu, který implementuje [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) rozhraní za účelem podpory seřazené příčinnou souvislost krokování funkce; to znamená, když je ladicí program krokování ve funkci Další funkce pro spuštění nemusí být předchozí funkce v zásobníku, ale funkce v jiném vlákně úplně se vynechá. Definice "příčiny", najdete v článku [Glosář ladicího programu Visual Studio](../../../extensibility/debugger/reference/visual-studio-debugger-glossary.md).  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)

