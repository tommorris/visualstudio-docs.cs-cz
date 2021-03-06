---
title: IDebugClassField::GetDefaultIndexer | Dokumentace Microsoftu
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
- IDebugClassField::GetDefaultIndexer
helpviewer_keywords:
- IDebugClassField::GetDefaultIndexer method
ms.assetid: 47ce4f45-3816-4b40-909c-5032d0692d75
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b632103d30dddb178ad0d2866f72e6f864d9f197
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673480"
---
# <a name="idebugclassfieldgetdefaultindexer"></a>IDebugClassField::GetDefaultIndexer
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugClassField::GetDefaultIndexer](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugclassfield-getdefaultindexer).  
  
Získá název výchozímu indexeru.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT GetDefaultIndexer(   
   BSTR* pbstrIndexer  
);  
```  
  
```csharp  
int GetDefaultIndexer(  
   out string pbstrIndexer  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pbstrIndexer`  
 [out] Vrátí řetězec obsahující název výchozí indexeru.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí hodnotu S_OK nebo vrátí S_FALSE v případě, že neexistuje žádný výchozí indexer. V opačném případě vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Indexer výchozí třídy je vlastnost, která je označena jako `Default` vlastnost pro pole přístupy. To je specifické pro [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]. Tady je příklad výchozímu indexeru deklarované v [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)] a způsobu jejich použití.  
  
```vb  
Imports System.Collections;  
  
Public Class Class1  
    Private myList as Hashtable  
  
    Default Public Property Item(ByVal Index As Integer) As Integer  
        Get  
            Return CType(List(Index), Integer)  
        End Get  
        Set(ByVal Value As Integer)  
            List(Index) = Value  
        End Set  
    End Property  
End Class  
  
Function GetItem(Index as Integer) as Integer  
    Dim classList as Class1 = new Class1  
    Dim value as Integer  
  
    ' Access array through default indexer  
    value = classList(2)  
  
    ' Access array through explicit property  
    value = classList.Item(2)  
  
    Return value  
End Function  
```  
  
## <a name="see-also"></a>Viz také  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)

