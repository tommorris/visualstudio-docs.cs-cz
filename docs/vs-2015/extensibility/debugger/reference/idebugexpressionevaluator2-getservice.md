---
title: IDebugExpressionEvaluator2::GetService | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IDebugExpressionEvaluator2::GetService
- GetService
ms.assetid: f8988a9e-9d18-42af-84a7-55f41e9adf63
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7e8ef02bee0f716194f1d37d619f070e00ecadbe
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670413"
---
# <a name="idebugexpressionevaluator2getservice"></a>IDebugExpressionEvaluator2::GetService
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugExpressionEvaluator2::GetService](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugexpressionevaluator2-getservice).  
  
Načte službu objekt dle jejich jedinečného identifikátoru.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT GetService (  
   GUID        uid,  
   IUnknown ** ppService  
);  
```  
  
```csharp  
int GetService (  
   Guid       uid,  
   out object ppService  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `uid`  
 [in] Jedinečný identifikátor služby k načtení.  
  
 `ppService`  
 [out] Vrátí objekt, který představuje službu.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 To mohou být spotřebovány vyhodnocení výrazu třetích stran získat services z jiného vyhodnocovací filtr výrazů. Například tato metoda může získat rozhraní pro služby visualizéru z výchozí vyhodnocovací filtr výrazů. Je nepravděpodobné, že je nutné implementovat toto rozhraní vyhodnocovače výrazů třetích stran.  
  
## <a name="see-also"></a>Viz také  
 [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)

