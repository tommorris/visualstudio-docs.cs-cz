---
title: EXCEPTION_INFO | Dokumentace Microsoftu
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
- EXCEPTION_INFO
helpviewer_keywords:
- EXCEPTION_INFO structure
ms.assetid: d046957a-b97d-420b-b46b-c67cbaef709e
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 152ddae9ad5c3c6b6119c146d428024bc2e26a95
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674122"
---
# <a name="exceptioninfo"></a>EXCEPTION_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [EXCEPTION_INFO](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/exception-info).  
  
Popisuje výjimku nebo chyb za běhu vyvolané laděnému programu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
typedef struct tagEXCEPTION_INFO {   
   IDebugProgram2* pProgram;  
   BSTR            bstrProgramName;  
   BSTR            bstrExceptionName;  
   DWORD           dwCode;  
   EXCEPTION_STATE dwState;  
   GUID            guidType;  
} EXCEPTION_INFO;  
```  
  
```csharp  
public struct EXCEPTION_INFO {   
   public IDebugProgram2 pProgram;  
   public string         bstrProgramName;  
   public string         bstrExceptionName;  
   public uint           dwCode;  
   public uint           dwState;  
   public Guid           guidType;  
};  
```  
  
## <a name="members"></a>Členové  
 pProgram  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) objekt, který reprezentuje program, ve kterém k výjimce došlo.  
  
 bstrProgramName  
 Název programu, ve kterém k výjimce došlo.  
  
 bstrExceptionName  
 Název výjimky.  
  
 dwCode  
 Identifikační kód chyby výjimky nebo za běhu.  
  
 dwState  
 Hodnota z [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md) výčet, který definuje stav výjimky.  
  
 guidType  
 Identifikátor GUID jazyka, buď `guidLang` nebo `guidEng`.  
  
## <a name="remarks"></a>Poznámky  
 Tato struktura je předán jako parametr [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) a [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md) metody. Tato struktura je také předat [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) metoda být vyplněna.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Struktury a sjednocení](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)   
 [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)   
 [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)

