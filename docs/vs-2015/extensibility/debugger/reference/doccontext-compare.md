---
title: DOCCONTEXT_COMPARE | Dokumentace Microsoftu
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
- DOCCONTEXT_COMPARE
helpviewer_keywords:
- DOCCONTEXT_COMPARE enumeration
ms.assetid: ed947c34-b07e-4b69-8381-b6e7cb842862
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1a4643a525e5a97f7c8af3be2e86eba9ac161936
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673837"
---
# <a name="doccontextcompare"></a>DOCCONTEXT_COMPARE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [DOCCONTEXT_COMPARE](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/doccontext-compare).  
  
Určuje kritéria pro porovnání dvou kontextů dokumentu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum enum_DOCCONTEXT_COMPARE {   
   DOCCONTEXT_EQUAL         = 0x0001,  
   DOCCONTEXT_LESS_THAN     = 0x0002,  
   DOCCONTEXT_GREATER_THAN  = 0x0003,  
   DOCCONTEXT_SAME_DOCUMENT = 0x0004  
};  
typedef DWORD DOCCONTEXT_COMPARE;  
```  
  
```csharp  
enum enum_DOCCONTEXT_COMPARE {   
   DOCCONTEXT_EQUAL         = 0x0001,  
   DOCCONTEXT_LESS_THAN     = 0x0002,  
   DOCCONTEXT_GREATER_THAN  = 0x0003,  
   DOCCONTEXT_SAME_DOCUMENT = 0x0004  
};  
```  
  
## <a name="members"></a>Členové  
 DOCCONTEXT_EQUAL  
 Vyhledá první kontext dokumentu v seznamu, který je roven cílový kontext dokumentu.  
  
 DOCCONTEXT_LESS_THAN  
 Vyhledá první kontext dokumentu v seznamu, která je menší než cílový kontext dokumentu.  
  
 DOCCONTEXT_GREATER_THAN  
 Vyhledá první kontext dokumentu v seznamu, který je větší než cílový kontext dokumentu.  
  
 DOCCONTEXT_SAME_DOCUMENT  
 Vyhledá první kontext dokumentu v seznamu, který je ve stejném dokumentu jako cílový kontext dokumentu.  
  
## <a name="remarks"></a>Poznámky  
 Předán jako argument [porovnání](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md) metody.  
  
 Tyto hodnoty se používají k určení porovnání kritérií pro hledání v seznamu první kontext dokumentu. Kontext dokumentu je uveden seznam kontexty dokumentu se porovnat proti prostřednictvím `IDebugDocumentContext2::Compare` metody. První kontext dokumentu v seznamu, pro který je operátor porovnání `true` je poté vrácen.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Porovnání](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md)

