---
title: IDebugExpressionEvaluator2::SetCallback | Dokumentace Microsoftu
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
- IDebugExpressionEvaluator2::SetCallback
- SetCallback
ms.assetid: 31e3a99e-e784-44a3-8b19-cc5ef31ed546
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 44761820b510f87a8ac007dba4a45837c7915afd
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673012"
---
# <a name="idebugexpressionevaluator2setcallback"></a>IDebugExpressionEvaluator2::SetCallback
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugExpressionEvaluator2::SetCallback](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugexpressionevaluator2-setcallback).  
  
Umožňuje vyhodnocovací filtr výrazů (EE) k určení rozhraní zpětného volání, které modul ladicího programu (DE) bude používat ke čtení nastavení metriky.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT SetCallback (  
   IDebugSettingsCallback2* pCallback  
);  
```  
  
```csharp  
int SetCallback (  
   IDebugSettingsCallback2 pCallback  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pCallback`  
 [in] Rozhraní pro nastavení zpětného volání.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda poskytuje rozhraní pro správce ladění relace, vyhodnocovače výrazů můžete použít ke čtení nastavení metriky. To je užitečné ve vzdálené ladění číst metriky na [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] počítače.  
  
## <a name="example"></a>Příklad  
 Následující příklady ukazují postup implementace této metody pro **CEE** objekt, který zveřejňuje [IDebugSettingsCallback2](../../../extensibility/debugger/reference/idebugsettingscallback2.md) rozhraní.  
  
```cpp#  
HRESULT CEE::SetCallback(IDebugSettingsCallback2* in_pCallback)  
{  
    // precondition  
    INVARIANT( this );  
  
    // function body  
    if (NULL != this->m_LanguageSpecificUseCases.pfSetCallback)  
    {  
        EEDomain::fSetCallback DomainVal =  
        {  
            in_pCallback  
        };  
  
        BOOL bSuccess = (*this->m_LanguageSpecificUseCases.pfSetCallback)(DomainVal);  
        ENSURE( bSuccess );  
    }  
  
    // postcondition  
    INVARIANT( this );  
  
    return S_OK;  
}  
```  
  
## <a name="see-also"></a>Viz také  
 [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)

