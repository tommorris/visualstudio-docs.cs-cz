---
title: PROGRAM_DESTROY_FLAGS | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- PROGRAM_DESTROY_FLAGS enumeration
ms.assetid: be00d4a3-d5b8-4159-b632-64577f534883
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 47c1482d5ad2e748bb2664b796e272ce8e9c03d5
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31126946"
---
# <a name="programdestroyflags"></a>PROGRAM_DESTROY_FLAGS
Vytvoří výčet platném hodnoty programu destroy příznaky.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
enum enum_PPROGRAM_DESTROY_FLAGS  
{  
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1  
};  
typedef DWORD PROGRAM_DESTROY_FLAGS;  
```  
  
```csharp  
public enum enum_PPROGRAM_DESTROY_FLAGS  
{  
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1  
};  
```  
  
## <a name="terms"></a>Podmínky  
 PROGRAM_DESTROY_CONTINUE_DEBUGGING  
 Destroy – program, ale nadále ladění.  
  
## <a name="remarks"></a>Poznámky  
 Výčet je vrácený [getflags –](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md) metoda.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Getflags –](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)