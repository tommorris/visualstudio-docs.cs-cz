---
title: IDebugPortSupplier2::GetPort | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugPortSupplier2::GetPort
helpviewer_keywords: IDebugPortSupplier2::GetPort
ms.assetid: d55d5055-7386-4037-bf22-4c3e434a99ca
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0d322cfe7486d0353c1eabad9f9c7bb40ee73477
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugportsupplier2getport"></a>IDebugPortSupplier2::GetPort
Získá port od jiného dodavatele portu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetPort(   
   REFGUID       guidPort,  
   IDebugPort2** ppPort  
);  
```  
  
```csharp  
int GetPort(   
   ref Guid        guidPort,  
   out IDebugPort2 ppPort  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `guidPort`  
 [v] Globálně jedinečný identifikátor (GUID) portu.  
  
 `ppPort`  
 [out] Vrátí [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) objekt, který reprezentuje port.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby. Vrátí `E_PORTSUPPLIER_NO_PORT` Pokud není port existuje s daným identifikátorem.  
  
## <a name="see-also"></a>Viz také  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)