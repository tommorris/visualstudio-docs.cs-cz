---
title: IDebugArrayObject | Dokumentace Microsoftu
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
- IDebugArrayObject
helpviewer_keywords:
- IDebugArrayObject method
ms.assetid: a1c8e77e-dee1-4748-a516-6ab032a8f54f
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 02d8c9758dc12a5f19f489d1221446bd4b855c96
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673646"
---
# <a name="idebugarrayobject"></a>IDebugArrayObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugArrayObject](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugarrayobject).  
  
> [!IMPORTANT]
>  V sadě Visual Studio 2015 je zastaralý tímto způsobem implementace vyhodnocovače výrazů. Informace o implementace vyhodnocovače výrazů modulu CLR najdete v tématu [vyhodnocovače výrazů modulu CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) a [spravované ukázka Chyba při vyhodnocování výrazu](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Toto rozhraní představuje objektu array.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugArrayObject : IDebugObject  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Chyba při vyhodnocování výrazu implementuje toto rozhraní k reprezentaci pole.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) rozhraní můžete získat pomocí tohoto rozhraní [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) Pokud objekt představuje pole.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Kromě metod na `IDebugObject` rozhraní, následující metody jsou implementovány ve `IDebugArrayObject` rozhraní.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[GetCount](../../../extensibility/debugger/reference/idebugarrayobject-getcount.md)|Získá počet elementů v poli.|  
|[GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md)|Získá prvek pole.|  
|[Metody GetElements](../../../extensibility/debugger/reference/idebugarrayobject-getelements.md)|Získá všechny prvky pole.|  
|[Getrank –](../../../extensibility/debugger/reference/idebugarrayobject-getrank.md)|Získá řád objektu array.|  
|[Getdimensions –](../../../extensibility/debugger/reference/idebugarrayobject-getdimensions.md)|Získá rozměry pole.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní vyhodnocovače výrazů používá představující pole v strom analýzy.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)

