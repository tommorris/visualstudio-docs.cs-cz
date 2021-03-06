---
title: IDebugPointerObject | Dokumentace Microsoftu
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
- IDebugPointerObject
helpviewer_keywords:
- IDebugPointerObject interface
ms.assetid: 257fa167-b46e-4ffb-9a12-272efbf26702
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 217136135c7fec71065f6a18e156ff2e5e956499
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675126"
---
# <a name="idebugpointerobject"></a>IDebugPointerObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugPointerObject](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugpointerobject).  
  
> [!IMPORTANT]
>  V sadě Visual Studio 2015 je zastaralý tímto způsobem implementace vyhodnocovače výrazů. Informace o implementace vyhodnocovače výrazů modulu CLR najdete v tématu [vyhodnocovače výrazů modulu CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) a [spravované ukázka Chyba při vyhodnocování výrazu](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Toto rozhraní představuje ukazatel objektu.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugPointerObject : IDebugObject  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Chyba při vyhodnocování výrazu implementuje toto rozhraní k reprezentaci ukazatele objektu.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) rozhraní můžete získat pomocí tohoto rozhraní [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) Pokud `IDebugObject` představuje ukazatel.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Kromě metod zděděných z [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md), `IDebugPointerObject` rozhraní poskytuje následující metody.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Přístup přes ukazatel](../../../extensibility/debugger/reference/idebugpointerobject-dereference.md)|Získá objekt, na kterou ukazuje rozhraní.|  
|[Provedení metody GetBytes](../../../extensibility/debugger/reference/idebugpointerobject-getbytes.md)|Získá hodnotu, na kterou ukazuje rozhraní jako řadu bajtů po sobě jdoucích.|  
|[SetBytes](../../../extensibility/debugger/reference/idebugpointerobject-setbytes.md)|Nastaví hodnotu, na kterou ukazuje rozhraní v řadě po sobě jdoucích bajtů.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní vyhodnocovače výrazů používá k zastoupení ukazatele v strom analýzy.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní pro vyhodnocení výrazu](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)

