---
title: IDebugProcessDestroyEvent2 | Dokumentace Microsoftu
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
- IDebugProcessDestroyEvent2
helpviewer_keywords:
- IDebugProcessDestroyEvent2
ms.assetid: 1b8e0528-95bc-48fa-9653-2cea66c8dc3a
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: dcb785119c673137432c3ad1241ce00f88ef08ce
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42631407"
---
# <a name="idebugprocessdestroyevent2"></a>IDebugProcessDestroyEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugProcessDestroyEvent2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprocessdestroyevent2).  
  
Toto rozhraní se odešle, když je proces je ukončeno, ukončí atypicky nebo je odpojen od.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugProcessDestroyEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Ladicí stroj (DE) nebo dodavatele port. Tento vlastní port implementovat toto rozhraní oznamuje, že proces byl ukončen. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) na stejný objekt jako toto rozhraní musí implementovat rozhraní. Používá SDM [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) přístup `IDebugEvent2` rozhraní.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 DE nebo dodavatele port. Tento vlastní port vytvoří a odešle tento objekt událostí k hlášení ukončení procesu. DE posílání této události [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) funkce zpětného volání, který je poskytnut pomocí SDM, když je připojen k laděnému programu. Dodavatel port. Tento vlastní port odešle pomocí této události [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md) rozhraní.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md)

