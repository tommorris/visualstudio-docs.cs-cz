---
title: "Idialoadcallback2 – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaLoadCallback2 interface
ms.assetid: 9a44277d-cbed-4811-9bad-5a2aa0f09323
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 474b6efeecc13b197f3189804682265beeba907e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idialoadcallback2"></a>IDiaLoadCallback2
Zpětná volání obdrží z symbol DIA postup vyhledání, která umožňují omezení uložená vyhledáním proces.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDiaLoadCallback2 : IDiaLoadCallback  
```  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Kromě metod v [idialoadcallback –](../../debugger/debug-interface-access/idialoadcallback.md) rozhraní, toto rozhraní poskytuje následující metody:  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Idialoadcallback2::restrictoriginalpathaccess –](../../debugger/debug-interface-access/idialoadcallback2-restrictoriginalpathaccess.md)|Určuje, zda hledá soubor .pdb v adresáři původní ladění.|  
|[Idialoadcallback2::restrictreferencepathaccess –](../../debugger/debug-interface-access/idialoadcallback2-restrictreferencepathaccess.md)|Určuje, jestli je povolené hledá soubor .pdb v cestě, kde je umístěn soubor .exe.|  
|[Idialoadcallback2::restrictdbgaccess –](../../debugger/debug-interface-access/idialoadcallback2-restrictdbgaccess.md)|Určuje, jestli hledáte informace o ladění je povolené z soubory dbg.|  
|[Idialoadcallback2::restrictsystemrootaccess –](../../debugger/debug-interface-access/idialoadcallback2-restrictsystemrootaccess.md)|Určuje, jestli hledání soubory PDB povolený v kořenovém adresáři systému.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní implementuje klientskou aplikaci a poskytuje odkaz na jeho ve volání [idiadatasource::loaddataforexe –](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) metoda. Mějte na paměti, pro všechny metody v implementaci [idialoadcallback –](../../debugger/debug-interface-access/idialoadcallback.md) také rozhraní.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: Dia2.h  
  
 Knihovna: diaguids.lib  
  
 Knihovny DLL: msdia80.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní (přístup k rozhraní SDK ladění)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiadatasource::loaddataforexe –](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)   
 [Idiareadexeatoffsetcallback –](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)   
 [Idiareadexeatrvacallback –](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)   
 [Idialoadcallback –](../../debugger/debug-interface-access/idialoadcallback.md)