---
title: IDebugProgram3::ExecuteOnThread | Dokumentace Microsoftu
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
- IDebugProgram3::ExecuteOnThread
ms.assetid: 2f5211e3-7a3f-47bf-9595-dfc8b4895d0d
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8ad46418897f4cdd2521209dd6643362e81bfcb6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672284"
---
# <a name="idebugprogram3executeonthread"></a>IDebugProgram3::ExecuteOnThread
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugProgram3::ExecuteOnThread](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprogram3-executeonthread).  
  
Spustí ladicí program. Vlákno se vrátí do poskytnout informace o ladicího programu, ve které vlákno je uživatel zobrazení při provádění programu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT ExecuteOnThread(  
   [in] IDebugThread2* pThread)  
```  
  
```csharp  
int ExecuteOnThread(  
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pThread`  
 [in] [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) objektu.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Existují tři způsoby, že ladicí program může pokračovat v provádění po zastavení:  
  
-   Spusťte: Zrušit všechny předchozí krok a spusťte až k další zarážce a tak dále.  
  
-   Krok: Zrušit všechny původní kroku a spustit, dokud se nedokončí nový krok.  
  
-   Pokračovat: Spusťte znovu a ponechání aktivní žádné staré kroku.  
  
 Vlákno předán `ExecuteOnThread` je užitečné, když se budete rozhodovat, ve kterém kroku zrušit. Pokud si nejste jisti vlákno, spusťte zruší všechny kroky. Se znalostí vlákna stačí zrušit kroku na aktivní vlákno.  
  
## <a name="see-also"></a>Viz také  
 [Spuštění](../../../extensibility/debugger/reference/idebugprogram2-execute.md)   
 [IDebugProgram3](../../../extensibility/debugger/reference/idebugprogram3.md)

