---
title: IEnumDebugFrameInfo2 | Dokumentace Microsoftu
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
- IEnumDebugFrameInfo2
helpviewer_keywords:
- IEnumDebugFrameInfo2
ms.assetid: 994e30ad-435a-4f9e-9272-d96d9e01099c
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7e343b8caabe2a09943ccc4cd068a62598dea548
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674647"
---
# <a name="ienumdebugframeinfo2"></a>IEnumDebugFrameInfo2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IEnumDebugFrameInfo2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ienumdebugframeinfo2).  
  
Vytvoří výčet toto rozhraní [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) struktury.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IEnumDebugFrameInfo2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Ladicí stroj (DE) implementuje toto rozhraní uvést seznam struktur, která popisuje aktuální zásobník volání.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Visual Studio volání [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) získat toto rozhraní pokaždé, když zarážku, výjimka nebo zastavení dochází v programu, který se právě ladí.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 V následující tabulce jsou uvedeny metody objektu `IEnumDebugFrameInfo2`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugframeinfo2-next.md)|Načte zadaný počet [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) struktury v sekvenci výčtu.|  
|[Přeskočit](../../../extensibility/debugger/reference/ienumdebugframeinfo2-skip.md)|Vynechá zadaný počet [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) struktury v sekvenci výčtu.|  
|[Resetovat](../../../extensibility/debugger/reference/ienumdebugframeinfo2-reset.md)|Návrat na začátek sekvence výčtu.|  
|[Klonování](../../../extensibility/debugger/reference/ienumdebugframeinfo2-clone.md)|Vytvoří čítač, který obsahuje stejného stavu jako aktuální enumerátor výčtu.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugframeinfo2-getcount.md)|Získá počet [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) struktury v enumerátor.|  
  
## <a name="remarks"></a>Poznámky  
 Visual Studio obdrží toto rozhraní jako první krok zpracovávání zarážky, výjimka nebo uživatelem generovaný pozastavení na program, který se právě ladí. Seznam [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) struktury představuje aktuální zásobník volání, s aktuálním volání funkce na začátku seznamu a nejstarší funkce volání na konci seznamu. Každý `FRAMEINFO` představuje rámec zásobníku, kontext, ve kterém můžete vyhodnotit výrazy a prohlédli jste si místní proměnné.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)   
 [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)

