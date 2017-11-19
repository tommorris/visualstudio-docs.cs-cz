---
title: IDebugProgram2::GetProcess | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugProgram2::GetProcess
helpviewer_keywords: IDebugProgram2::GetProcess
ms.assetid: 1d602485-ebaf-451c-9165-f2e226f20a90
caps.latest.revision: "13"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6d085c149c72393f0179ad6b6b50334426777d9c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugprogram2getprocess"></a>IDebugProgram2::GetProcess
Získáte proces, který tento program je spuštěn v.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetProcess(  
   IDebugProcess2** ppProcess  
);  
```  
  
```csharp  
int GetProcess(  
   out IDebugProcess2 ppProcess  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppProcess`  
 [out] Vrátí [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) rozhraní, které představuje proces.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Pokud modul ladění (DE) implementuje [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md) rozhraní, je DE implementace této metody by měla vždy vrátit `E_NOTIMPL` protože Zavedenými nemůže určit, které proces běží v a proto nelze splňovat implementace této metody.  
  
 Implementace `IDebugEngineLaunch2` rozhraní znamená, že je DE musí vědět, jak vytvořit proces; proto je DE implementace [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) rozhraní je možné vědět, co proces je spuštěna v.  
  
## <a name="see-also"></a>Viz také  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)