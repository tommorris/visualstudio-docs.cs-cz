---
title: Diaaddressmapentry – | Dokumentace Microsoftu
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
- DiaAddressMapEntry enumeration
ms.assetid: 5d0ae226-981d-4541-a801-fc4993fe663b
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0a6d5075917c49be66d030846cdc186b0fa5e50a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669672"
---
# <a name="diaaddressmapentry"></a>DiaAddressMapEntry
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [diaaddressmapentry –](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/diaaddressmapentry).  
  
Popisuje položky v mapování adres.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
struct DiaAddressMapEntry {   
   DWORD rva,  
   DWORD rvaTo  
};  
```  
  
## <a name="elements"></a>Elementy  
 `rva`  
 Relativní virtuální adresu (RVA) v bitové kopii A.  
  
 `rvaTo`  
 Relativní virtuální adresu `rva` je namapována na obrázku B.  
  
## <a name="remarks"></a>Poznámky  
 Mapování adresy zajišťuje překlad z jedné image rozložení (A) do jiného (B). Pole `DiaAddressMapEntry` struktury seřazené podle `rva` definuje mapu adresu.  
  
 Přeložit adresy, `addrA`, obrázku A na adresu, `addrB`, obrázku B, proveďte následující kroky:  
  
1.  Hledat na mapě položce, `e`, s největší `rva` menší než nebo rovno `addrA`.  
  
2.  Nastavte `delta = addrA – e.rva`.  
  
3.  Nastavte `addrB = e.rvaTo + delta`.  
  
 Pole `DiaAddressMapEntry` struktury je předán [idiaaddressmap::set_addressmap –](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) metody.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: dia2.h  
  
## <a name="see-also"></a>Viz také  
 [Výčty a struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)



