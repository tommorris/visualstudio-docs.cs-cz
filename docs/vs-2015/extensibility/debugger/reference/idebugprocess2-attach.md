---
title: IDebugProcess2::Attach | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugProcess2::Attach
helpviewer_keywords:
- IDebugProcess2::Attach
ms.assetid: 40d78417-fde2-45c3-96c9-16e06bd9008d
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 90ff2520a64ca338cb703c5e22f8a0c021b52540
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666588"
---
# <a name="idebugprocess2attach"></a>IDebugProcess2::Attach
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugProcess2::Attach](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprocess2-attach).  
  
Správce ladění relace (SDM) se připojí k procesu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback,  
   GUID*                 rgguidSpecificEngines,  
   DWORD                 celtSpecificEngines,  
   HRESULT*              rghrEngineAttach  
);  
```  
  
```csharp  
int Attach(   
   IDebugEventCallback2 pCallback,  
   Guid[]               rgguidSpecificEngines,  
   uint                 celtSpecificEngines,  
   int[]                rghrEngineAttach  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pCallback`  
 [in] [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) objekt, který se používá pro oznámení události ladění.  
  
 `rgguidSpecificEngines`  
 [in] Pole identifikátory GUID ladicími stroji, který se má použít pro ladění programů spuštěných v rámci procesu. Tento parametr může být hodnota null. Podrobnosti najdete v části poznámky.  
  
 `celtSpecificEngines`  
 [in] Počet ladicí stroje v `rgguidSpecificEngines` pole a velikost `rghrEngineAttach` pole.  
  
 `rghrEngineAttach`  
 [out v] Pole vrácené ladicími stroji kódy HRESULT. Velikost tohoto pole se zadává v `celtSpecificEngines` parametru. Každý z kódů je obvykle buď `S_OK` nebo `S_ATTACH_DEFERRED`. Ten označuje, že DE je v současnosti připojená k žádné programy.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí kód chyby. V následující tabulce jsou uvedeny další možné hodnoty.  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|`E_ATTACH_DEBUGGER_ALREADY_ATTACHED`|Zadaný proces je již připojen k ladicímu programu.|  
|`E_ATTACH_DEBUGGEE_PROCESS_SECURITY_VIOLATION`|Během procesu připojení došlo k porušení zabezpečení.|  
|`E_ATTACH_CANNOT_ATTACH_TO_DESKTOP`|Klasické pracovní plochy proces nelze připojit k ladicímu programu.|  
  
## <a name="remarks"></a>Poznámky  
 Připojení k procesu, na položku Všechny programy spuštěné v tomto procesu, který lze ladit pomocí ladicí stroj (DE) zadaný v připojí SDM `rgguidSpecificEngines` pole. Nastavte `rgguidSpecificEngines` parametr s hodnotou null hodnotu, nebo zahrnout `GUID_NULL` v poli se připojit k všechny programy v procesu.  
  
 Všechny ladění události, ke kterým dochází v procesu se posílají daného [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) objektu. To `IDebugEventCallback2` objekt víceklientského modelu SDM volá tuto metodu.  
  
## <a name="see-also"></a>Viz také  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)

