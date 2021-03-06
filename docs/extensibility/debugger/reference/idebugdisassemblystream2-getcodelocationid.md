---
title: IDebugDisassemblyStream2::GetCodeLocationId | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
helpviewer_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
ms.assetid: 567adfb8-2f54-499a-a027-e4ecb82277ef
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 86682bb64f041cd8ee1b08bbec02c28492cac7a9
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31107644"
---
# <a name="idebugdisassemblystream2getcodelocationid"></a>IDebugDisassemblyStream2::GetCodeLocationId
Vrátí identifikátor umístění kódu pro konkrétní kód kontext.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetCodeLocationId(   
   IDebugCodeContext2* pCodeContext,  
   UINT64*             puCodeLocationId  
);  
```  
  
```csharp  
int GetCodeLocationId(   
   IDebugCodeContext2 pCodeContext,  
   out ulong          puCodeLocationId  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pCodeContext`  
 [v] [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) objekt, který chcete převést na identifikátor.  
  
 `puCodeLocationId`  
 [out] Vrátí identifikátor umístění kódu. V části poznámky.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby. Vrátí `E_CODE_CONTEXT_OUT_OF_SCOPE` Pokud kontext kód je platný, ale mimo obor.  
  
## <a name="remarks"></a>Poznámky  
 Identifikátor umístění kódu je specifická pro ladění modulu (DE), podpora zpětný překlad. Tento identifikátor umístění se používá interně pomocí DE sledovat pozice v kódu a je obvykle adresy nebo posun určitého druhu. Jediným požadavkem je, že pokud kód kontextu jedno umístění je menší než kód kontextu jiného umístění, menší než identifikátor kód umístění druhý kontextu kód musí být také odpovídající kód umístění identifikátor první kontext kódu.  
  
 Chcete-li načíst kód kontextu identifikátor umístění kódu, volejte [GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md) metoda.  
  
## <a name="see-also"></a>Viz také  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md)