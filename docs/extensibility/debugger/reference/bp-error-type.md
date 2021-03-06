---
title: BP_ERROR_TYPE | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- BP_ERROR_TYPE
helpviewer_keywords:
- BP_ERROR_TYPE enumeration
ms.assetid: c483eaab-db29-46de-bfdb-5c2a9a9cfb68
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 676ec19fec1406d85e6a7d9e66865b2794f72aa6
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31103003"
---
# <a name="bperrortype"></a>BP_ERROR_TYPE
Určuje typ chyby zarážky.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
enum enum_BP_ERROR_TYPE {   
   BPET_NONE            = 0x00000000,  
   BPET_TYPE_WARNING    = 0x00000001,  
   BPET_TYPE_ERROR      = 0x00000002,  
   BPET_SEV_HIGH        = 0x0F000000,  
   BPET_SEV_GENERAL     = 0x07000000,  
   BPET_SEV_LOW         = 0x01000000,  
   BPET_TYPE_MASK       = 0x0000ffff,  
   BPET_SEV_MASK        = 0xffff0000,  
   BPET_GENERAL_WARNING = BPET_SEV_GENERAL | BPET_TYPE_WARNING,  
   BPET_GENERAL_ERROR   = BPET_SEV_GENERAL | BPET_TYPE_ERROR,  
   BPET_ALL             = 0xffffffff  
};  
typedef DWORD BP_ERROR_TYPE;  
```  
  
```csharp  
public enum enum_BP_ERROR_TYPE {   
   BPET_NONE            = 0x00000000,  
   BPET_TYPE_WARNING    = 0x00000001,  
   BPET_TYPE_ERROR      = 0x00000002,  
   BPET_SEV_HIGH        = 0x0F000000,  
   BPET_SEV_GENERAL     = 0x07000000,  
   BPET_SEV_LOW         = 0x01000000,  
   BPET_TYPE_MASK       = 0x0000ffff,  
   BPET_SEV_MASK        = 0xffff0000,  
   BPET_GENERAL_WARNING = BPET_SEV_GENERAL | BPET_TYPE_WARNING,  
   BPET_GENERAL_ERROR   = BPET_SEV_GENERAL | BPET_TYPE_ERROR,  
   BPET_ALL             = 0xffffffff  
};  
```  
  
## <a name="members"></a>Členové  
 BPET_NONE  
 Určuje žádná chyba zarážek.  
  
 BPET_TYPE_WARNING  
 Určuje zarážek upozornění stylu chyby.  
  
 BPET_TYPE_ERROR  
 Určuje chybu zarážek stylu chyby.  
  
 BPET_SEV_HIGH  
 Určuje chyba zarážek vysokou závažností.  
  
 BPET_SEV_GENERAL  
 Určuje zarážek střední závažnosti chyby.  
  
 BPET_SEV_LOW  
 Určuje nízkou závažností zarážek chyby.  
  
 BPET_TYPE_MASK  
 Určuje k chybě zarážek maska stylu.  
  
 BPET_SEV_MASK  
 Určuje závažnost maska style zarážek chyby.  
  
 BPET_GENERAL_WARNING  
 Určuje Obecné upozornění style zarážek chyby.  
  
 BPET_GENERAL_ERROR  
 Určuje zarážek stylu chyby obecné chybě.  
  
 BPET_ALL  
 Určuje všechny typy chyb zarážek.  
  
## <a name="remarks"></a>Poznámky  
 Tyto hodnoty mohou být kombinovány s bitové `OR` a slouží pro `dwType` členem [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md) struktury. Předá jako parametr, který se [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md) metoda.  
  
 Typ chyby zarážek se skládá z typu závažnosti. Znamená, že je chyba typ zarážek nikdy právě typu (například `BPET_TYPE_ERROR`,) nebo závažnosti (například `BPET_SEV_GENERAL`) sám o sobě. `BPET_GENERAL_WARNING` a `BPET_GENERAL_ERROR` zadejte předem definovaných hodnot pro obecné upozornění a chyb zarážky.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)   
 [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)