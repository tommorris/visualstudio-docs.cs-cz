---
title: IRemoteDebugApplicationThreadEx:EnumGlobalContexts | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationThreadEx:EnumGlobalContexts
apilocation:
- scrobj.dll
helpviewer_keywords:
- IRemoteDebugApplicationThreadEx:EnumGlobalContexts
ms.assetid: a6c0bc3f-4afc-41e1-b734-06e252c5b171
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c57dc014e9f448e58db5fe6509536db5023b22dd
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
ms.locfileid: "24794820"
---
# <a name="iremotedebugapplicationthreadexenumglobalcontexts"></a>IRemoteDebugApplicationThreadEx:EnumGlobalContexts
Vytvoří výčet kontexty globálním výrazu pro všechny jazyky, které jsou spuštěné v této přístup z více vláken.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumGlobalExpressionContexts(  
   IEnumDebugExpressionContexts**  ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnum`  
 [out] Enumerátor, který uvádí kontexty globálním výrazu pro všechny jazyky, které jsou spuštěné v této přístup z více vláken.  
  
## <a name="return-value"></a>Návratová hodnota  
 Vrátí metodu `HRESULT`. Možné hodnoty zahrnují hodnoty v následující tabulce, ale nejsou na ně omezeny.  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|`S_OK`|Metoda byla úspěšná.|  
  
## <a name="remarks"></a>Poznámky