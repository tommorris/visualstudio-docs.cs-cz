---
title: dwTYPE_KIND | Dokumentace Microsoftu
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
- dwTYPE_KIND
helpviewer_keywords:
- dwTYPE_KIND enumeration
ms.assetid: 6ff56b0f-c502-4e6c-9829-bfa05361b783
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 026cf5e3f26cc6faeb8e8829295c0875203d88d1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42679411"
---
# <a name="dwtypekind"></a>dwTYPE_KIND
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [dwTYPE_KIND](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/dwtype-kind).  
  
Určuje, jak interpretovat typ [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) objektu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
  
typedef DWORD dwTYPE_KIND;  
```  
  
```csharp  
public enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
```  
  
#### <a name="parameters"></a>Parametry  
 TYPE_KIND_METADATA  
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) sjednocení by měl být interpretován jako [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md) struktury.  
  
 TYPE_KIND_PDB  
 `TYPE_INFO` Sjednocení by měl být interpretován jako [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md) struktury.  
  
 TYPE_KIND_BUILT  
 `TYPE_INFO` Sjednocení by měl být interpretován jako [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md) struktury.  
  
## <a name="remarks"></a>Poznámky  
 Joinkind hodnoty tento výčet `dwKind` pole [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) struktury a slouží k určení, jak interpretovat `type` člen sjednocení. `TYPE_INFO` Struktura je vrácený voláním [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md) metody.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)   
 [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)   
 [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)   
 [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)

