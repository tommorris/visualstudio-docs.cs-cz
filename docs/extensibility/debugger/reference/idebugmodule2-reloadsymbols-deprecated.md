---
title: IDebugModule2::ReloadSymbols_Deprecated | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugModule2::ReloadSymbols
helpviewer_keywords:
- IDebugModule2::ReloadSymbols method
ms.assetid: 0f9f0133-7d58-4cd9-a6ca-1141e095749d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: dcd383130c1af1765014adfa438482543c336ede
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31118857"
---
# <a name="idebugmodule2reloadsymbolsdeprecated"></a>IDebugModule2::ReloadSymbols_Deprecated
ZASTARALÉ. NEPOUŽÍVEJTE. Znovu načte symboly pro tento modul.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT ReloadSymbols(   
   LPCOLESTR pszUrlToSymbols,  
   BSTR*     pbstrDebugMessage  
);  
```  
  
```csharp  
int ReloadSymbols(   
   string     pszUrlToSymbols,  
   out string pbstrDebugMessage  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pszUrlToSymbols`  
 [v] Cesta k úložišti symbol.  
  
 `pbstrDebugMessage`  
 [out] Vrátí informační zpráva, jako je například stav nebo chybovou zprávu, která se zobrazí vpravo od názvu modulu v okně moduly.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby. Modul ladění musí vracet vždycky `E_FAIL`.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda není podporován. Implementace [LoadSymbols](../../../extensibility/debugger/reference/idebugmodule3-loadsymbols.md) metoda místo.  
  
## <a name="see-also"></a>Viz také  
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)   
 [LoadSymbols](../../../extensibility/debugger/reference/idebugmodule3-loadsymbols.md)