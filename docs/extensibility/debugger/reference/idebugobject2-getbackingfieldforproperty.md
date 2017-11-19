---
title: IDebugObject2::GetBackingFieldForProperty | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugObject2::GetBackingFieldForProperty
helpviewer_keywords: IDebugObject2::GetBackingFieldForProperty method
ms.assetid: e72c6338-5573-4fad-8075-f3ade3435424
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2637ddf5d50953367de66cd2ca63d7774dbc3213
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugobject2getbackingfieldforproperty"></a>IDebugObject2::GetBackingFieldForProperty
Získá pole nebo proměnná (pokud existuje), může být zálohování vlastnost představuje tento objekt.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetBackingFieldForProperty(  
   IDebugObject2** ppObject  
);  
```  
  
```csharp  
int GetBackingFieldForProperty(  
   out IDebugObject2 ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppObject`  
 [out] [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md) objekt popisující pole zálohování.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí S_OK; jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md) objektů, představuje vlastnost třídy spravovaného kódu, který je metoda s get nebo nastavení přístupového objektu. Tyto vlastnosti obvykle vyžadují proměnnou, která bude obsahovat hodnotu manipulovat vlastnost. Tato proměnná se označuje jako pole zálohování. Pokud není k dispozici žádné pole zálohování pro objekt, zkontrolujte vrátit hodnotu null: některé volající nemusí věnovat pozornost návratovou hodnotu, ale místo toho bude vypadat Pokud chcete zobrazit, pokud byla vrácena hodnota null v `ppObject`.  
  
## <a name="see-also"></a>Viz také  
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)