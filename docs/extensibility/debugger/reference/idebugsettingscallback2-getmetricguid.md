---
title: IDebugSettingsCallback2::GetMetricGuid | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: IDebugSettingsCallback2::GetMetricGuid
ms.assetid: 91092763-3362-4857-adf0-231bc1254206
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d43bb839b1c8c4be3d9c56a20d6e9e17eb79cd1b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugsettingscallback2getmetricguid"></a>IDebugSettingsCallback2::GetMetricGuid
Načte jedinečný identifikátor metriky její název.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetMetricGuid(  
   LPCWSTR pszType,  
   REFGUID guidSection,  
   LPCWSTR pszMetric,  
   GUID*   pguidValue  
);  
```  
  
```csharp  
private int GetMetricGuid(  
   string   pszType,  
   ref Guid guidSection,  
   string   pszMetric,  
   out Guid pguidValue  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pszType`  
 [v] Typ metriky.  
  
 `guidSection`  
 [v] Jedinečný identifikátor oddílu.  
  
 `pszMetric`  
 [v] Název metriky.  
  
 `pguidValue`  
 [out] Vrací jedinečný identifikátor metriky.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="see-also"></a>Viz také  
 [IDebugSettingsCallback2](../../../extensibility/debugger/reference/idebugsettingscallback2.md)