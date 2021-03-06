---
title: BP_UNBOUND_REASON | Dokumentace Microsoftu
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
- BP_UNBOUND_REASON
helpviewer_keywords:
- BP_UNBOUND_REASON enumeration
ms.assetid: 939b6f9c-113b-471d-9f30-b03871af6285
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 554bdd9def52cfbde5b4fe535f017f762f1c8edc
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633151"
---
# <a name="bpunboundreason"></a>BP_UNBOUND_REASON
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [BP_UNBOUND_REASON](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/bp-unbound-reason).  
  
Poskytuje z důvodů, proč nevázaná zarážku.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum enum_BP_UNBOUND_REASON {   
   BPUR_UNKNOWN           = 0x0000,  
   BPUR_CODE_UNLOADED     = 0x0002,  
   BPUR_BREAKPOINT_REBIND = 0x0003,  
   BPUR_BREAKPOINT_ERROR  = 0x0004  
};  
typedef DWORD BP_UNBOUND_REASON;  
```  
  
```csharp  
public enum enum_BP_UNBOUND_REASON {   
   BPUR_UNKNOWN           = 0x0000,  
   BPUR_CODE_UNLOADED     = 0x0002,  
   BPUR_BREAKPOINT_REBIND = 0x0003,  
   BPUR_BREAKPOINT_ERROR  = 0x0004  
};  
```  
  
## <a name="members"></a>Členové  
 BPUR_UNKNOWN  
 Důvodem neznámý.  
  
 BPUR_CODE_UNLOADED  
 Kód, který obsahuje zarážku byl uvolněn.  
  
 BPUR_BREAKPOINT_REBIND  
 Zarážku bylo znovu připojeno, do jiného umístění. To může dojít po úpravě a pokračovat v operacích přesun zarážku nebo zarážku je vázán na soubor s cestou, která již není platný.  
  
 BPUR_ BREAKPOINT_ERROR  
 Zarážka je určena jako chybu po je vázán. K tomu dochází na spravovaných zarážky, jejíž podmínky už nejsou platné.  
  
## <a name="remarks"></a>Poznámky  
 Vrácené [getreason –](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md) metody.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Getreason –](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md)

