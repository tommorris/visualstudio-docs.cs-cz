---
title: IDebugPortNotify2 | Dokumentace Microsoftu
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
- IDebugPortNotify2
helpviewer_keywords:
- IDebugPortNotify2 interface
ms.assetid: 43278b79-bf16-4c08-bcf1-6f7f7a17feab
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 703e42c0b0717761816ed8ca11f42e7f22650517
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629729"
---
# <a name="idebugportnotify2"></a>IDebugPortNotify2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugPortNotify2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugportnotify2).  
  
Toto rozhraní zaregistruje nebo zruší registraci program, který lze ladit s portem, který je spuštěn na.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugPortNotify2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Dodavatel port. Tento vlastní port implementuje toto rozhraní pro podporu přidávání a odebírání programů z portu. Obvykle je implementované na stejný objekt, který implementuje [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) rozhraní.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Volání [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) na `IDebugPort2` rozhraní vrátí toto rozhraní. Kromě toho volání [GetPortNotify](../../../extensibility/debugger/reference/idebugdefaultport2-getportnotify.md) vrátí toto rozhraní. Ladicí stroj můžete zobrazit toto rozhraní jako parametr [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md).  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 V následující tabulce jsou uvedeny metody objektu `IDebugPortNotify2`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[AddProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)|Zaregistruje port, který je spuštěn na program, který lze ladit.|  
|[RemoveProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md)|Zruší registraci program, který lze ladit z portu, který je spuštěn na.|  
  
## <a name="remarks"></a>Poznámky  
 Pokud není port pro ladění je způsob, jak zjistit, když programy jsou načteny nebo uvolněny, dodavatel port. Tento vlastní port musí implementovat toto rozhraní. Všechny programy, které jsou načteny pro ladění přes konkrétní port jsou sledovány v tomto rozhraní.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)

