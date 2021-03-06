---
title: Basictype – | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- BasicType enumeration
ms.assetid: 19ae53ba-cd6e-47b6-9f94-27ae663ce955
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6a518c3cb800493fdf6c2677a0f09957e2768b0e
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673101"
---
# <a name="basictype"></a>BasicType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [basictype –](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/basictype).  
  
Určuje základní typ symbolu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum BasicType {   
   btNoType   = 0,  
   btVoid     = 1,  
   btChar     = 2,  
   btWChar    = 3,  
   btInt      = 6,  
   btUInt     = 7,  
   btFloat    = 8,  
   btBCD      = 9,  
   btBool     = 10,  
   btLong     = 13,  
   btULong    = 14,  
   btCurrency = 25,  
   btDate     = 26,  
   btVariant  = 27,  
   btComplex  = 28,  
   btBit      = 29,  
   btBSTR     = 30,  
   btHresult  = 31  
};  
```  
  
## <a name="elements"></a>Elementy  
 btNoType  
 Není zadán žádný základní typ.  
  
 btVoid  
 Základní typ je `void`.  
  
 btChar  
 Základní typ je `char` (C/C++ typ).  
  
 btWChar  
 Základní typ je širokého znaku (Unicode) (`WCHAR`).  
  
 btInt  
 Základní typ je `signed int` (C/C++ typ).  
  
 btUInt  
 Základní typ je `unsigned int` (C/C++ typ).  
  
 btFloat  
 Základní typ je číslo s plovoucí desetinnou čárkou (`FLOAT`).  
  
 btBCD  
 Základní typ je binární soubor pevně zakódované desetinné číslo (`BCD`).  
  
 btBool  
 Základní typ je logická hodnota (`BOOL`).  
  
 btLong  
 Základní typ je `long int` (C/C++ typ).  
  
 btULong  
 Základní typ je `unsigned long int` (C/C++ typ).  
  
 btCurrency  
 Základní typ je měna.  
  
 btDate  
 Základní typ je datum a čas (`DATE`).  
  
 btVariant  
 Základní typ je typ proměnné struktury (`VARIANT`).  
  
 btComplex  
 Základní typ je komplexní čísla.  
  
 btBit  
 Základní typ je tento bit.  
  
 btBSTR  
 Základní typ je řetězec základní nebo binární (`BSTR`).  
  
 btHresult  
 Základní typ je `HRESULT`.  
  
## <a name="remarks"></a>Poznámky  
 Jsou vrácené hodnoty v tento výčet [idiasymbol::get_basetype –](../../debugger/debug-interface-access/idiasymbol-get-basetype.md) metody.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: cvconst.h  
  
## <a name="see-also"></a>Viz také  
 [Výčty a struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [Idiasymbol::get_basetype –](../../debugger/debug-interface-access/idiasymbol-get-basetype.md)   
 [IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol-get-length.md)



