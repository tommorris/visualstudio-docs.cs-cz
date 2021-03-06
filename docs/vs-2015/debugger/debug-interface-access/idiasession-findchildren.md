---
title: Idiasession::findchildren – | Dokumentace Microsoftu
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
- IDiaSession::findChildren method
ms.assetid: 5d19046f-f668-4aa9-8788-95cda9a98997
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 97fed0f8ce7ff0712054b2aa3408217efe39f706
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629446"
---
# <a name="idiasessionfindchildren"></a>IDiaSession::findChildren
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [idiasession::findchildren –](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/idiasession-findchildren).  
  
Načte všechny podřízené objekty zadaný nadřazený identifikátor odpovídající název a značka typu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT findChildren (   
   IDiaSymbol*       parent,  
   SymTagEnum        symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `parent`  
 [in] [Idiasymbol –](../../debugger/debug-interface-access/idiasymbol.md) představující nadřazeného objektu. Pokud je tento symbol nadřazené funkce, modul nebo blok a pak jeho lexikální podřízené položky jsou vráceny v `ppResult`. Pokud je symbol nadřazeného typu, budou vráceny podřízené třídy. Pokud je tento parametr `NULL`, pak `symtag` musí být nastaveno na `SymTagExe` nebo `SymTagNull`, která vrací globální obor (soubor .exe).  
  
 `symtag`  
 [in] Určuje symbol značky podřízené položky, který se má načíst. Hodnoty pocházejí ze [symtagenum – výčet](../../debugger/debug-interface-access/symtagenum.md) výčtu. Nastavte na `SymTagNull` načíst všechny podřízené objekty.  
  
 `name`  
 [in] Určuje název podřízenou položku, která se má načíst. Nastavte na `NULL` pro všechny podřízené objekty, které se mají načíst.  
  
 `compareFlags`  
 [in] Určení možností porovnání využije na odpovídající název. Hodnoty z [namesearchoptions – výčet](../../debugger/debug-interface-access/namesearchoptions.md) výčtu lze použít samostatně nebo v kombinaci.  
  
 `ppResult`  
 [out] Vrátí [idiaenumsymbols –](../../debugger/debug-interface-access/idiaenumsymbols.md) načíst objekt, který obsahuje seznam podřízenými symboly.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí kód chyby.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje, jak najít místní proměnné, funkce `pFunc` nejmenuje shoda `szVarName`.  
  
```cpp#  
IDiaEnumSymbols* pEnum;  
pSession->findChildren( pFunc, SymTagData, szVarName, nsCaseSensitive, &pEnum );  
```  
  
## <a name="see-also"></a>Viz také  
 [Přehled](../../debugger/debug-interface-access/overview-debug-interface-access-sdk.md)   
 [Idiaenumsymbols –](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [Idiasession –](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol –](../../debugger/debug-interface-access/idiasymbol.md)   
 [Namesearchoptions – výčet](../../debugger/debug-interface-access/namesearchoptions.md)   
 [Symtagenum – výčet](../../debugger/debug-interface-access/symtagenum.md)



