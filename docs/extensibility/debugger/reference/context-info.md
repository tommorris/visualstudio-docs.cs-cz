---
title: CONTEXT_INFO | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- CONTEXT_INFO
helpviewer_keywords:
- CONTEXT_INFO structure
ms.assetid: 6b513f4e-e7b0-4969-adf0-2205ccc1e09b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: fb634f59a3a7eb3b37e70dd87f48b22a07251d0e
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31100429"
---
# <a name="contextinfo"></a>CONTEXT_INFO
Tato struktura popisuje kontextu paměti nebo kontext kódu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
typedef struct _tagCONTEXT_INFO {   
   CONTEXT_INFO_FIELDS dwFields;  
   BSTR                bstrModuleUrl;  
   BSTR                bstrFunction;  
   TEXT_POSITION       posFunctionOffset;  
   BSTR                bstrAddress;  
   BSTR                bstrAddressOffset;  
   BSTR                bstrAddressAbsolute;  
} CONTEXT_INFO;  
```  
  
```csharp  
public struct CONTEXT_INFO {  
   public uint          dwFields;  
   public string        bstrModuleUrl;  
   public string        bstrFunction;  
   public TEXT_POSITION posFunctionOffset;  
   public string        bstrAddress;  
   public string        bstrAddressOffset;  
   public string        bstrAddressAbsolute;  
};  
```  
  
## <a name="members"></a>Členové  
 dwFields  
 Kombinace příznaků z mu [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md) výčet, který určuje pole, která jsou doplnit **.**  
  
 bstrModuleUrl  
 Název modulu, kde se nachází kontextu.  
  
 bstrFunction  
 Název funkce, kde je umístěn daný kontext.  
  
 posFunctionOffset  
 A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) struktura, která identifikuje posun řádku a ve sloupci funkce spojený s kontextem kódu.  
  
 bstrAddress  
 Adresa v kódu, kde se nachází daném kontextu.  
  
 bstrAddressOffset  
 Posun adresu v kódu, kde se nachází daném kontextu.  
  
 bstrAddressAbsolute  
 Absolutní adresa v paměti, kde se nachází daném kontextu.  
  
## <a name="remarks"></a>Poznámky  
 Tato struktura je vrácená z volání [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md) metoda.  
  
 Typické použití tato struktura je v podporu **paměti** okno ladění.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Struktury a sjednocení](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md)   
 [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md)   
 [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)