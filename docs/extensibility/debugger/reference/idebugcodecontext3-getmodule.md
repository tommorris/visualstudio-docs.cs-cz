---
title: IDebugCodeContext3::GetModule | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- IDebugCodeContext3::GetModule
ms.assetid: 8e4317b8-8255-486c-a896-a68ed94f8aa1
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3a3dd353e3b329208ca71553ea7f441a054feb4a
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31103978"
---
# <a name="idebugcodecontext3getmodule"></a>IDebugCodeContext3::GetModule
Získá odkaz na rozhraní modulu ladění.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetModule(   
   IDebugModule2 **ppModule  
);  
```  
  
```csharp  
public int GetModule(   
   out IDebugModule2 ppModule  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppModule`  
 [out] Referenční informace k rozhraní ladění modulu.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje, jak pro tuto metodu implementovat **CDebugCodeContext** objekt, který zveřejňuje [IDebugBeforeSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugbeforesymbolsearchevent2.md) rozhraní.  
  
```cpp  
HRESULT CDebugCodeContext::GetModule(IDebugModule2** ppModule)  
{  
    HRESULT hr = S_OK;  
    CComPtr<CModule> pModule;  
  
    IfFalseGo( ppModule, E_INVALIDARG );  
    *ppModule = NULL;  
  
    IfFailGo( this->GetModule(&pModule) );  
    IfFailGo( pModule->QueryInterface(IID_IDebugModule2, (void**) ppModule) );  
  
Error:  
  
    return hr;  
}  
```  
  
## <a name="see-also"></a>Viz také  
 [IDebugCodeContext3](../../../extensibility/debugger/reference/idebugcodecontext3.md)