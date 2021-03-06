---
title: IDebugClassField | Dokumentace Microsoftu
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
- IDebugClassField
helpviewer_keywords:
- IDebugClassField interface
ms.assetid: 49358cbc-8973-4862-9dcc-79b1248e6712
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f549d72a3c6af9e6e7393ace4f30d06558d9af80
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42679471"
---
# <a name="idebugclassfield"></a>IDebugClassField
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugClassField](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugclassfield).  
  
Toto rozhraní představuje třídu jako typ.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDebugClassField : IDebugContainerField  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Poskytovatel symbolů implementuje na stejný objekt, který implementuje toto rozhraní [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) rozhraní. Toto rozhraní je specializací, který představuje typ třídy.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Počet rozhraní mají metody, které můžou vrátit, včetně rozhraní [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md), [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md), a [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md). Můžete také použít [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) získat z tohoto rozhraní [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) rozhraní, pokud [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) metoda vrátí příznak `FIELD_TYPE_CLASS`.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Kromě metod na [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) a [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) rozhraní, toto rozhraní implementuje následující:  
  
|Metoda|Popis|  
|------------|-----------------|  
|[EnumBaseClasses](../../../extensibility/debugger/reference/idebugclassfield-enumbaseclasses.md)|Vytvoří čítač pro základní třídy této třídy.|  
|[DoesInterfaceExist](../../../extensibility/debugger/reference/idebugclassfield-doesinterfaceexist.md)|Určuje, zda určité rozhraní je definována v třídě.|  
|[EnumNestedClasses](../../../extensibility/debugger/reference/idebugclassfield-enumnestedclasses.md)|Vytvoří čítač pro vnořené třídy této třídy.|  
|[GetEnclosingClass](../../../extensibility/debugger/reference/idebugclassfield-getenclosingclass.md)|Získá třídu, která obklopuje této třídy.|  
|[EnumInterfacesImplemented](../../../extensibility/debugger/reference/idebugclassfield-enuminterfacesimplemented.md)|Vytvoří čítač pro rozhraní implementována touto třídou.|  
|[EnumConstructors](../../../extensibility/debugger/reference/idebugclassfield-enumconstructors.md)|Vytvoří čítač pro konstruktory této třídy.|  
|[GetDefaultIndexer](../../../extensibility/debugger/reference/idebugclassfield-getdefaultindexer.md)|Získá název výchozímu indexeru.|  
|[EnumNestedEnums](../../../extensibility/debugger/reference/idebugclassfield-enumnestedenums.md)|Vytvoří čítač pro vnořené čítačů této třídy.|  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní poskytovatele symbolů](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)

