---
title: IDebugPortSupplier2::AddPort | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugPortSupplier2::AddPort
helpviewer_keywords:
- IDebugPortSupplier2::AddPort
ms.assetid: df491161-6bf3-4fcc-b478-b9ec88ec995f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ab6348739feba7006e5c18eee6f7dc5f301242d9
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31114427"
---
# <a name="idebugportsupplier2addport"></a>IDebugPortSupplier2::AddPort
Přidá port.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT AddPort(   
   IDebugPortRequest2* pRequest,  
   IDebugPort2**       ppPort  
);  
```  
  
```csharp  
int AddPort(   
   IDebugPortRequest2 pRequest,  
   out IDebugPort2    ppPort  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRequest`  
 [v] [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) objekt, který popisuje port, který chcete přidat.  
  
 `ppPort`  
 [out] Vrátí [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) objekt, který reprezentuje port.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda vytvoří ve skutečnosti požadovaném portu, jakož i přidáním do portu dodavatele interní seznam aktivních portů. [CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md) nelze volat metodu nejprve aby se zabránilo možné časově náročné zpožděním.  
  
## <a name="see-also"></a>Viz také  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)   
 [CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md)