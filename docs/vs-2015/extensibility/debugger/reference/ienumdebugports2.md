---
title: IEnumDebugPorts2 | Dokumentace Microsoftu
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
- IEnumDebugPorts2
helpviewer_keywords:
- IEnumDebugPorts2
ms.assetid: 1754eef3-cf62-42e0-b218-1911acba77d4
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9ff7eac1da5cba43bf93a352e571c7a1f912932b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42679513"
---
# <a name="ienumdebugports2"></a>IEnumDebugPorts2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IEnumDebugPorts2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ienumdebugports2).  
  
Toto rozhraní uvádí porty počítači nebo port dodavatele.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IEnumDebugPorts2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Dodavatel port. Tento vlastní port implementuje toto rozhraní představující seznam portů vytvořili dodavatelem. Visual Studio implementuje toto rozhraní podporu vlastní dodavatele portu.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Volání [EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md) získat toto rozhraní představující seznam portů, které jsou vytvořené dodavatele portu. Volání [EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md) získat toto rozhraní představující seznam portů, které byly uloženy na disk.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 V následující tabulce jsou uvedeny metody objektu `IEnumDebugPorts2`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugports2-next.md)|Načte zadaný počet portů v sekvenci výčtu.|  
|[Přeskočit](../../../extensibility/debugger/reference/ienumdebugports2-skip.md)|Vynechá zadaný počet portů v sekvenci výčtu.|  
|[Resetovat](../../../extensibility/debugger/reference/ienumdebugports2-reset.md)|Návrat na začátek sekvence výčtu.|  
|[Klonování](../../../extensibility/debugger/reference/ienumdebugports2-clone.md)|Vytvoří čítač, který obsahuje stejného stavu jako aktuální enumerátor výčtu.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugports2-getcount.md)|Získá počet portů v enumerátor.|  
  
## <a name="remarks"></a>Poznámky  
 Visual Studio používá toto rozhraní k naplnění seznamu porty používané pro připojení k procesům.  
  
 Ladicí stroj obvykle nepoužívá toto rozhraní.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumPorts](../../../extensibility/debugger/reference/idebugcoreserver2-enumports.md)   
 [EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md)

