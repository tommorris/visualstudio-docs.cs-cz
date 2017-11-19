---
title: IDebugMethodField::EnumStaticLocals | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugMethodField::EnumStaticLocals
helpviewer_keywords: IDebugMethodField::EnumStaticLocals method
ms.assetid: e0c522c4-f759-4c32-ae87-7abcb573e77d
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 49de63c81c46f379630f5d5cb328a670472ddcee
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugmethodfieldenumstaticlocals"></a>IDebugMethodField::EnumStaticLocals
Vytvoří enumerátor pro statické místní proměnné metody.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT EnumStaticLocals(   
   IEnumDebugFields** ppLocals  
);  
```  
  
```csharp  
int EnumStaticLocals(  
   out IEnumDebugFields ppLocals  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppLocals`  
 [out] Vrátí [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) objektu, který představuje seznam místní statické hodnoty. Pokud neexistují žádné místní statické hodnoty, vrátí hodnotu null.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí S_OK nebo vrátí S_FALSE, pokud nejsou žádné místní statické hodnoty. Jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Každý prvek je [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) objektu, který představuje různé typy místní statické hodnoty. Volání [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) metoda na každém objektu k určení přesně jaký druh statické místní objekt představuje.  
  
## <a name="see-also"></a>Viz také  
 [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)