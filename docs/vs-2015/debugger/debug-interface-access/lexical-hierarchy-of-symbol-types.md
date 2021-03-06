---
title: Lexikální hierarchie typů symbolů | Dokumentace Microsoftu
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
- symbols [DIA SDK], type hierarchies
ms.assetid: 912da653-ddfe-45a4-84aa-64281283739a
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2d807841429a722f31f3aecdc08f1a0972b05378
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633856"
---
# <a name="lexical-hierarchy-of-symbol-types"></a>Lexikální hierarchie typů symbolů
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [lexikální hierarchie typů symbolů](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/lexical-hierarchy-of-symbol-types).  
  
Následující tabulka uvádí v lexikální hierarchie typů symbolů.  
  
## <a name="symbol-types"></a>Typů symbolů  
  
|Typ symbolu|Popis|  
|-----------------|-----------------|  
|[Poznámka](../../debugger/debug-interface-access/annotation.md)|Určuje umístění služby s poznámkami v kódu programu.|  
|[Blok](../../debugger/debug-interface-access/block.md)|Určuje vnořené obory ve funkcích.|  
|`Compiland`|Určuje `compiland` propojený soubor .exe.|  
|[CompilandDetails](../../debugger/debug-interface-access/compilanddetails.md)|Určuje kompilantu data, která může vyžadovat načítání podrobností o další kompilace a proto se vám účtovat za běhu režie pro načtení.|  
|[CompilandEnv](../../debugger/debug-interface-access/compilandenv.md)|Určuje libovolné proměnné prostředí důležité pro kompilaci souboru pro kompilaci.|  
|[Vlastní (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/custom-debug-interface-access-sdk.md)|Určuje symbol definovaný uživatelem.|  
|[Data (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/data-debug-interface-access-sdk.md)|Určuje tyto proměnné jako parametry, místní proměnné, globální proměnné a členy třídy.|  
|[Exe](../../debugger/debug-interface-access/exe.md)|Určuje globální rozsah dat; odpovídá celý soubor .exe nebo .dll.|  
|[FuncDebugEnd](../../debugger/debug-interface-access/funcdebugend.md)|Určuje funkci, která obsahuje bod definovaný v ladění, které se do konce.|  
|[FuncDebugStart](../../debugger/debug-interface-access/funcdebugstart.md)|Určuje funkci, která obsahuje bod definovaný v ladění, která má začít.|  
|[Funkce (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/function-debug-interface-access-sdk.md)|Určuje funkci, která.|  
|[Popisek (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/label-debug-interface-access-sdk.md)|Určuje umístění v kódu programu.|  
|[PublicSymbol](../../debugger/debug-interface-access/publicsymbol.md)|Určuje externí symbol, který se zobrazí při vytváření spustitelného souboru.|  
|[Převod](../../debugger/debug-interface-access/thunk.md)|Určuje `thunk`.|  
|[UsingNameSpace](../../debugger/debug-interface-access/usingnamespace.md)|Určuje `namespace`identifikátor.|  
  
> [!NOTE]
>  Další symbol vlastnosti mohou být k dispozici v závislosti na typu symbol. Tyto vlastnosti jsou uvedeny v tématech pro jednotlivé symbol.  
  
## <a name="see-also"></a>Viz také  
 [Hierarchie tříd typů symbolů](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [Idiasymbol::get_symtag –](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)   
 [Symboly a značky symbolů](../../debugger/debug-interface-access/symbols-and-symbol-tags.md)   
 [Symtagenum – výčet](../../debugger/debug-interface-access/symtagenum.md)



