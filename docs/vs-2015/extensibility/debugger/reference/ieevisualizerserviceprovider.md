---
title: IEEVisualizerServiceProvider | Dokumentace Microsoftu
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
- IEEVisualizerServiceProvider
helpviewer_keywords:
- IEEVisualizerServiceProvider interface
ms.assetid: 859d1a51-1c65-4c8b-ae74-3b74b181ebcd
caps.latest.revision: 18
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e27eab6c3547790ca1f66181c04bba085e463c5e
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633572"
---
# <a name="ieevisualizerserviceprovider"></a>IEEVisualizerServiceProvider
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IEEVisualizerServiceProvider](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ieevisualizerserviceprovider).  
  
> [!IMPORTANT]
>  V sadě Visual Studio 2015 je zastaralý tímto způsobem implementace vyhodnocovače výrazů. Informace o implementace vyhodnocovače výrazů modulu CLR najdete v tématu [vyhodnocovače výrazů modulu CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) a [spravované ukázka Chyba při vyhodnocování výrazu](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Toto rozhraní poskytuje přístup k metodě, která můžete vytvořit služby vizualizátoru, která se používá ke zpracování typu vizualizéru úkoly pro rozhraní IDE.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IEEVisualizerServiceProvider : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Visual Studio implementuje toto rozhraní k vytvoření objektu služby vizualizátoru, který se pak použije k poskytování ID tříd (`CLSID`s) z vizualizérů typů do integrovaného vývojového prostředí sady Visual Studio.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Chyba při vyhodnocování výrazu (EE) volá [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md) získat toto rozhraní.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
  
|Metoda|Popis|  
|------------|-----------------|  
|[CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)|Vytvoří službu vizualizéru|  
  
## <a name="remarks"></a>Poznámky  
 `IEEVisualizerServiceProvider` Rozhraní zadaný během provádění [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md). Služby visualizéru, který vytvoří toto rozhraní se používá k poskytování funkce, které [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) rozhraní, který EE je zodpovědný za implementace. EE zodpovídá také za implementace [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md) rozhraní, které umožňuje vizualizérů typů zobrazit a změnit hodnoty vlastnosti.  
  
 Zobrazit [Visualizing a zobrazení dat](../../../extensibility/debugger/visualizing-and-viewing-data.md) podrobné informace o interakci těchto rozhraní.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní pro vyhodnocení výrazu](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)   
 [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)   
 [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [Vizualizace a zobrazení dat](../../../extensibility/debugger/visualizing-and-viewing-data.md)

