---
title: IEnumDebugThreads2::Next | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IEnumDebugThreads2::Next
helpviewer_keywords: IEnumDebugThreads2::Next
ms.assetid: bcffd954-3c67-4867-96f3-041ddb3e34d4
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a12c6232f135e8bf4569b6de90a7191548e28746
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="ienumdebugthreads2next"></a>IEnumDebugThreads2::Next
Vrací další sadu elementů z výčtu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT Next(  
   ULONG           celt,  
   IDebugThread2** rgelt,  
   ULONG*          pceltFetched  
);  
```  
  
```csharp  
int Next(  
   uint            celt,  
   IDebugThread2[] rgelt,  
   ref uint        pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `celt`  
 [v] Počet elementů k načtení. Také určuje maximální velikost `rgelt` pole.  
  
 `rgelt`  
 [ve out] Pole [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) elementy k vyplnění.  
  
 `pceltFetched`  
 [out] Vrátí počet elementů ve skutečnosti, vrátí se v `rgelt`.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`. Vrátí `S_FALSE` Pokud méně než požadovaný počet elementů nemohl být vrácen; jinak vrátí kód chyby.  
  
## <a name="see-also"></a>Viz také  
 [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)