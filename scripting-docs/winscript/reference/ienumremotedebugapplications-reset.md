---
title: IEnumRemoteDebugApplications::Reset | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumRemoteDebugApplications.Reset
apilocation:
- scrobj.dll
helpviewer_keywords:
- IEnumRemoteDebugApplications::Reset
ms.assetid: a2c03728-999f-400c-bf40-4ced6cd88410
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 657822ed1fed8cd9fb129a17469820b368f86244
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
ms.locfileid: "24794382"
---
# <a name="ienumremotedebugapplicationsreset"></a>IEnumRemoteDebugApplications::Reset
Návrat na začátek v sekvenci výčtu.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Reset();  
```  
  
#### <a name="parameters"></a>Parametry  
 Tato metoda nepřijímá žádné parametry.  
  
## <a name="return-value"></a>Návratová hodnota  
 Vrátí metodu `HRESULT`. Možné hodnoty zahrnují hodnoty v následující tabulce, ale nejsou na ně omezeny.  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|`S_OK`|Metoda byla úspěšná.|  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda obnoví v sekvenci výčet na začátku.  
  
## <a name="see-also"></a>Viz také  
 [Ienumremotedebugapplications – rozhraní](../../winscript/reference/ienumremotedebugapplications-interface.md)