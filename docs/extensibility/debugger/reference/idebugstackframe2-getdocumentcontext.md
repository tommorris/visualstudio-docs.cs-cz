---
title: IDebugStackFrame2::GetDocumentContext | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugStackFrame2::GetDocumentContext
helpviewer_keywords: IDebugStackFrame2::GetDocumentContext
ms.assetid: 69e81439-1238-4f18-9028-6fd1c1ba5e4a
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4c015d2b5839ee979b88eced74b3a51efa5bd42f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugstackframe2getdocumentcontext"></a>IDebugStackFrame2::GetDocumentContext
Získá kontext dokumentu pro tento rámce zásobníku.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetDocumentContext (   
   IDebugDocumentContext2** ppCxt  
);  
```  
  
```csharp  
int GetDocumentContext (   
   out IDebugDocumentContext2 ppCxt  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppCxt`  
 [out] Vrátí [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) objekt, který představuje aktuální pozici ve zdrojovém dokumentu.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda je rychlejší než při volání [GetCodeContext](../../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md) metoda a pak volání [GetDocumentContext](../../../extensibility/debugger/reference/idebugcodecontext2-getdocumentcontext.md) metoda v kontextu kódu. Však není zaručeno, že bude tuto metodu implementovat každý motor ladění (DE).  
  
## <a name="see-also"></a>Viz také  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [GetDocumentContext](../../../extensibility/debugger/reference/idebugcodecontext2-getdocumentcontext.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugstackframe2-getcodecontext.md)