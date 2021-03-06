---
title: MODULE_FLAGS | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- MODULE_FLAGS
helpviewer_keywords:
- MODULE_FLAGS enumeration
ms.assetid: 0e555b42-b846-4dbb-812e-8e3d11c85b2d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 945a4a0fd5a7de1e9d04d409390caddfc718d92d
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31124820"
---
# <a name="moduleflags"></a>MODULE_FLAGS
Používají k popisu modul.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
enum enum_MODULE_FLAGS {   
   MODULE_FLAG_NONE        = 0x0000,  
   MODULE_FLAG_SYSTEM      = 0x0001,  
   MODULE_FLAG_SYMBOLS     = 0x0002,  
   MODULE_FLAG_64BIT       = 0x0004,  
   MODULE_FLAG_OPTIMIZED   = 0x0008,  
   MODULE_FLAG_UNOPTIMIZED = 0x0010  
};  
typedef DWORD MODULE_FLAGS;  
```  
  
```csharp  
public enum enum_MODULE_FLAGS {   
   MODULE_FLAG_NONE        = 0x0000,  
   MODULE_FLAG_SYSTEM      = 0x0001,  
   MODULE_FLAG_SYMBOLS     = 0x0002,  
   MODULE_FLAG_64BIT       = 0x0004,  
   MODULE_FLAG_OPTIMIZED   = 0x0008,  
   MODULE_FLAG_UNOPTIMIZED = 0x0010  
};  
```  
  
## <a name="members"></a>Členové  
 MODULE_FLAG_NONE  
 Určuje žádný modul.  
  
 MODULE_FLAG_SYSTEM  
 Určuje modul systému.  
  
 MODULE_FLAG_SYMBOLS  
 Určuje symbol modulu.  
  
 MODULE_FLAG_64BIT  
 Určuje modul 64-bit.  
  
 MODULE_FLAG_OPTIMIZED  
 Určuje, že bylo optimalizováno modul. Tento stav se odrazí v **moduly** okno.  
  
 MODULE_FLAG_UNOPTIMIZED  
 Určuje, že modul není optimalizovaný. Tento stav se odrazí v **moduly** okno. Toto je výchozí stav.  
  
## <a name="remarks"></a>Poznámky  
 Použít pro `m_dwModuleFlags` členem [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) struktury.  
  
 Tyto příznaky mohou být kombinovány s bitové `OR`.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)