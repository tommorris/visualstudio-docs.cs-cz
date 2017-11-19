---
title: IEEDataStorage | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IEEDataStorage
helpviewer_keywords: IEEDataStorage interface
ms.assetid: 704e932d-2325-410e-89c4-ce88c6ec19da
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: daf5f3e7547ee32b641ccf4c1448eaa9a80b72fa
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="ieedatastorage"></a>IEEDataStorage
Toto rozhraní představuje pole bajtů.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IEEDataStorage : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Poznámky pro implementátory  
 Vyhodnocení výrazu (EE) implementuje toto rozhraní představují pole bajtů (používá typ vizualizérech k načtení a změnit data prostřednictvím [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) rozhraní). EE obvykle implementuje toto rozhraní pro podporu vizualizérech externího typu.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Metody na `IPropertyProxyEESide` rozhraní všechny vrátit toto rozhraní. Volání [GetPropertyProxy](../../../extensibility/debugger/reference/ipropertyproxyprovider-getpropertyproxy.md) získat [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) rozhraní. Volání [QueryInterface](/cpp/atl/queryinterface) na [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) rozhraní získat [IPropertyProxyProvider](../../../extensibility/debugger/reference/ipropertyproxyprovider.md) rozhraní.  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 `IEEDataStorage` Rozhraní implementuje následujících metod:  
  
|Metoda|Popis|  
|------------|-----------------|  
|[GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)|Načte zadaný počet bajtů dat, které mají poskytnutá vyrovnávací paměť.|  
|[Getsize –](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)|Získá počet bajtů dat, které jsou k dispozici.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní se používá podle typu vizualizér pro přístup k data ukládaná společností určitý objekt. Data, je zpracovaná jako pole bajtů, což vizualizér typ k manipulaci s ním v jakémkoli způsob, jak je potřeba ho k dispozici pro uživatele.  
  
 Vlastní prohlížeč můžete také použít toto rozhraní, v případě potřeby, i když více obvykle vlastní prohlížeč využije vlastní rozhraní [GetMemoryBytes](../../../extensibility/debugger/reference/idebugproperty2-getmemorybytes.md) nebo [GetStringChars](../../../extensibility/debugger/reference/idebugproperty3-getstringchars.md) (pro data orientovaná na řetězec).  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Sestavení: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Základní rozhraní](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [Typ vizualizér a vlastní prohlížeč](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)