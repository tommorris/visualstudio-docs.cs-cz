---
title: IDebugGenericFieldDefinition::ConstructInstantiation | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- ConstructInstantiation
- IDebugGenericFieldDefinition::ConstructInstantiation
ms.assetid: ef8ae261-a98b-4dc2-93b3-7c5191818ba2
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a3c11eb3578cd547265a6d0f14727c931364dc0c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebuggenericfielddefinitionconstructinstantiation"></a>IDebugGenericFieldDefinition::ConstructInstantiation
Vytvoří instanci pole zadané pole typu argumentů.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT ConstructInstantiation(  
   ULONG32       cArgs,  
   IDebugField** ppArgs,  
   IDebugField** ppConstructedField  
);  
```  
  
```csharp  
int ConstructInstantiation(  
   uint            cArgs,  
   IDebugField[]   ppArgs,  
   out IDebugField ppConstructedField  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `cArgs`  
 [v] Počet argumentů `ppArgs` pole.  
  
 `ppArgs`  
 [v] Pole, které obsahuje argumenty typu. Argumenty typu musí být uzavřený typy (neobecnou nebo zcela vytvořenou instanci obecné).  
  
 `ppConstructedField`  
 [out] Vrátí [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) rozhraní, které představuje nové pole.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Omezení nejsou zaškrtnutí.  
  
## <a name="see-also"></a>Viz také  
 [IDebugGenericFieldDefinition](../../../extensibility/debugger/reference/idebuggenericfielddefinition.md)