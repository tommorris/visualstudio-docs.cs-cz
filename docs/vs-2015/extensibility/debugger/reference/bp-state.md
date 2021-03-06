---
title: BP_STATE | Dokumentace Microsoftu
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
- BP_STATE
helpviewer_keywords:
- BP_STATE enumeration
ms.assetid: 08aa6a3f-3e5f-4c83-8eca-7b7b5f8e208d
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f6fc9cdcdedb9b733da27489232558f394879cc1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42686656"
---
# <a name="bpstate"></a>BP_STATE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [BP_STATE](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/bp-state).  
  
Určuje existenci vázaná zarážka a také určuje, jestli je povolené.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum enum_BP_STATE {   
   BPS_NONE     = 0x0000,  
   BPS_DELETED  = 0x0001,  
   BPS_DISABLED = 0x0002,  
   BPS_ENABLED  = 0x0003  
};  
typedef DWORD BP_STATE;  
```  
  
```csharp  
public enum enum_BP_STATE {   
   BPS_NONE     = 0x0000,  
   BPS_DELETED  = 0x0001,  
   BPS_DISABLED = 0x0002,  
   BPS_ENABLED  = 0x0003  
};  
```  
  
## <a name="members"></a>Členové  
 BPS_NONE  
 Určuje, že neexistuje žádná zarážka.  
  
 BPS_DELETED  
 Určuje, že zarážka byla odstraněna.  
  
 BPS_DISABLED  
 Určuje, že je zakázaná zarážka.  
  
 BPS_ENABLED  
 Určuje, zda je povolena zarážka.  
  
## <a name="remarks"></a>Poznámky  
 Vrátilo [GetState](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getstate.md) metody.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetState](../../../extensibility/debugger/reference/idebugboundbreakpoint2-getstate.md)

