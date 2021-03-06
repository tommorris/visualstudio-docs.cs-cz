---
title: IDebugEnumField | Dokumentace Microsoftu
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
- IDebugEnumField
helpviewer_keywords:
- IDebugEnumField interface
ms.assetid: 42f685bf-0f39-47f4-98b0-6022efe2bf97
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1a4429329e4a17cb0e0e5ffdc3cbe81b25910e74
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668208"
---
# <a name="idebugenumfield"></a>IDebugEnumField
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugEnumField](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugenumfield).  
  
Toto rozhraní představuje typ výčtu.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugEnumField : IDebugContainerField  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Poskytovatel symbolů implementuje toto rozhraní představující výčet.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Použití [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) získat z tohoto rozhraní [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) rozhraní, pokud [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) vrátí `FIELD_TYPE_ENUM`.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce VTable pořadí  
 Kromě metod na `IDebugField` a `IDebugContainerField` rozhraní, toto rozhraní implementuje následujících metod:  
  
|Metoda|Popis|  
|------------|-----------------|  
|[GetUnderlyingSymbol](../../../extensibility/debugger/reference/idebugenumfield-getunderlyingsymbol.md)|Vrátí [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) popisující název pro tento typ výčtu.|  
|[GetStringFromValue](../../../extensibility/debugger/reference/idebugenumfield-getstringfromvalue.md)|Vrátí název spojeného s danou hodnotou konstanty výčtu.|  
|[GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)|Vrátí hodnotu přidruženou k názvu konstantní daný výčet|  
|[GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)|Vrátí hodnotu přidruženou k dané výčtu konstant názvem, ale bez rozlišování případů.|  
  
## <a name="remarks"></a>Poznámky  
 Je základní symbol, který je ve skutečnosti vázané na umístění s [svázat](../../../extensibility/debugger/reference/idebugbinder-bind.md).  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní poskytovatele symbolů](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [Vytvoření vazby](../../../extensibility/debugger/reference/idebugbinder-bind.md)

