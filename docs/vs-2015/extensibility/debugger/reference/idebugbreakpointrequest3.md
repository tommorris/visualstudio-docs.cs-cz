---
title: IDebugBreakpointRequest3 | Dokumentace Microsoftu
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
- IDebugBreakpointRequest3
helpviewer_keywords:
- IDebugBreakpointRequest3
ms.assetid: 8a042beb-b319-48e3-b3c8-9c8336ab371b
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 922c21c8d202f12a1ce06e049fd604c9e6d9b67a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672213"
---
# <a name="idebugbreakpointrequest3"></a>IDebugBreakpointRequest3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugBreakpointRequest3](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugbreakpointrequest3).  
  
Toto rozhraní představuje informace potřebné k vytvoření a připojení jakýkoli typ zarážky. Je rozšířením [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugBreakpointRequest3 : IDebugBreakpointRequest2  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Správce ladění relace (SDM) obvykle implementuje toto rozhraní.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Ladicí stroj (DE) toto rozhraní má přístup k voláním [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) na rozhraní IDebugBreakpointRequest2 obdrželi volání [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md).  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Kromě metod zděděných z [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md), `IDebugBreakpointRequest3` rozhraní poskytuje následující metody.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[GetRequestInfo2](../../../extensibility/debugger/reference/idebugbreakpointrequest3-getrequestinfo2.md)|Získá informace o požadavku zarážky, popisující tuto zarážku žádost.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní se používá na další informace na DE prostřednictvím [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) struktury. Tyto další informace obsahuje ID dodavatele je DE (ve formě identifikátoru GUID), název zarážku s trasováním a název omezení zarážku.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md)   
 [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)

