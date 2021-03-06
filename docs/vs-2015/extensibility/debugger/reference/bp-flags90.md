---
title: BP_FLAGS90 | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- BP_FLAGS90 enumeration
ms.assetid: 3e5a06c5-fb30-4b8a-b2d5-4a0570fc80bd
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c983356d3a808d523ddd8a5cb87912f0a2638d7f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670904"
---
# <a name="bpflags90"></a>BP_FLAGS90
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [BP_FLAGS90](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/bp-flags90).  
  
Vytvoří výčet platných hodnot pro volitelné příznaky. Volitelné příznaky slouží k určení dalších informací při nastavení zarážky. Tento výčet rozšiřuje [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md) výčtu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum enum_BP_FLAGS90  
{  
   // VS 8.0 values  
   BP90_FLAG_NONE               = 0x0000,  
   BP90_FLAG_MAP_DOCPOSITION    = 0x0001,  
   BP90_FLAG_DONT_STOP          = 0x0002,  
  
   // Values added in VS 9.0  
   BP90_FLAG_TRACEPOINT_CONTINUE = 0x0004,  
};  
typedef DWORD BP_FLAGS90;  
```  
  
```csharp  
public enum enum_BP_FLAGS90  
{  
   // VS 8.0 values  
   BP90_FLAG_NONE                = 0x0000,  
   BP90_FLAG_MAP_DOCPOSITION     = 0x0001,  
   BP90_FLAG_DONT_STOP           = 0x0002,  
  
   // Values added in VS 9.0  
   BP90_FLAG_TRACEPOINT_CONTINUE = 0x0004,  
};  
```  
  
#### <a name="parameters"></a>Parametry  
 BP90_FLAG_NONE  
 Určuje příznak bez zarážek.  
  
 BP90_FLAG_MAP_DOCPOSITION  
 Určuje, že ladicí stroj (DE) by měl mapovat zarážky pomocí pozice dokumentu. To se vztahuje pouze na zarážky nastavené v skript orientovaného zdrojových souborech, jako je například stránek ASP (Active Server).  
  
 BP90_FLAG_DONT_STOP  
 Určuje, že zarážka by měla být zpracovány ladicího stroje, ale, že ladicí stroj nakonec by neměl zastavit To znamená [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md) nesmí být rozesílaná objektu události. Tento příznak slouží k používá hlavně s body trasování.  
  
 BP90_FLAG_TRACEPOINT_CONTINUE  
 Použít nativní ladicí modul k určení, zda krokování stavu by měla zůstat nezaškrtnutá. Se liší od BP90_FLAG_DONT_STOP protože BP90_FLAG_DONT_STOP není nastavená, pokud bod trasování provede makro.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: Msdbg90.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)

