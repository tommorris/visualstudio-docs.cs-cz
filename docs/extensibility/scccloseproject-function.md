---
title: Scccloseproject – funkce | Dokumentace Microsoftu
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- SccCloseProject
helpviewer_keywords:
- SccCloseProject function
ms.assetid: 259c2069-d349-4814-810f-1c3151b7fb84
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 49d3196fbe2eb6c3bafa1ec234e27072e50a4b7d
ms.sourcegitcommit: 06db1892fff22572f0b0a11994dc547c2b7e2a48
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/08/2018
ms.locfileid: "39636022"
---
# <a name="scccloseproject-function"></a>Scccloseproject – funkce
Tato funkce se zavře projekt knec konkrétní relace.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
SCCRTN SccCloseProject (  
   LPVOID pvContext  
);  
```  
  
### <a name="parameters"></a>Parametry  
 pvContext  
 Struktura kontext modulu plug-in zdroje ovládacího prvku.  
  
## <a name="return-value"></a>Návratová hodnota  
 Modul plug-in implementaci ovládacího prvku zdroje této funkce má vracet instanci jednoho z následujících hodnot:  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|SCC_OK|Projekt byl úspěšně uzavřen.|  
|SCC_E_PROJNOTOPEN|Žádný projekt není otevřen.|  
|SCC_E_NOTAUTHORIZED|Uživatel nemůže k provedení této operace.|  
|SCC_E_NONSPECIFICERROR|K nespecifikované chybě.|  
  
## <a name="remarks"></a>Poznámky  
 [Sccopenproject –](../extensibility/sccopenproject-function.md) je vždy volána před provedením této funkce. Voláním této funkce je následována volání na buď `SccOpenProject` funkce nebo [sccuninitialize –](../extensibility/sccuninitialize-function.md), které zcela ukončí připojení k systému správy zdrojového kódu.  
  
## <a name="see-also"></a>Viz také:  
 [Funkce modulu plug-in API zdrojového ovládacího prvku](../extensibility/source-control-plug-in-api-functions.md)   
 [Sccopenproject –](../extensibility/sccopenproject-function.md)   
 [Sccinitialize –](../extensibility/sccinitialize-function.md)