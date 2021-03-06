---
title: Hierarchie typů symbolů třídy | Dokumentace Microsoftu
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
- symbols [DIA SDK], class hierarchies
ms.assetid: 0ccd6990-4654-44cd-a6f3-bdd82fe90f6c
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 35db9ca51285e10310a7fcee0c6db32dd9dff4a4
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668671"
---
# <a name="class-hierarchy-of-symbol-types"></a>Hierarchie tříd typů symbolů
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [hierarchie typů symbolů tříd](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/class-hierarchy-of-symbol-types).  
  
Následující tabulka popisuje typy symbolu v hierarchii tříd.  
  
## <a name="symbol-types"></a>Typů symbolů  
  
|Typ symbolu|Popis|  
|-----------------|-----------------|  
|[UDT](../../debugger/debug-interface-access/udt.md)|Symbol použitý k reprezentaci jednotlivých třídy, struktury a sjednocení.|  
|[Výčet (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/enum-debug-interface-access-sdk.md)|Symbol pro výčtové typy.|  
|[PointerType](../../debugger/debug-interface-access/pointertype.md)|Symbol pro typy ukazatelů.|  
|[ArrayType](../../debugger/debug-interface-access/arraytype.md)|Symbol pro typy polí.|  
|[BaseType](../../debugger/debug-interface-access/basetype.md)|Symbol pro základní typy|  
|[Typedef (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/typedef-debug-interface-access-sdk.md)|Symbol, který představuje názvy pro ostatní typy.|  
|[BaseClass](../../debugger/debug-interface-access/baseclass.md)|Symbolu používanou pro každou základní třídu uživatelem definovaný typ (UDT).|  
|[Friend (Přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/friend-debug-interface-access-sdk.md)|Symbol spřátelené třídy a funkce friend.|  
|[FunctionType](../../debugger/debug-interface-access/functiontype.md)|Symbol pro každou jedinečnou funkci podpis.|  
|[FunctionArgType](../../debugger/debug-interface-access/functionargtype.md)|Symbol pro každý parametr funkce.|  
|[VTableShape](../../debugger/debug-interface-access/vtableshape.md)|Symbol pro velikost virtuální tabulky.|  
|[VTable](../../debugger/debug-interface-access/vtable.md)|Symbol pro virtuální tabulky.|  
|[CustomType](../../debugger/debug-interface-access/customtype.md)|Symbol pro typ definované dodavatelem.|  
|[ManagedType](../../debugger/debug-interface-access/managedtype.md)|Symbol pro typ definovaný v metadatech.|  
|[Rozměr](../../debugger/debug-interface-access/dimension.md)|Symbol rozměry pole.|  
  
> [!NOTE]
>  Každý symbol může mít vlastnosti, které obsahují informace o symbolu, jakož i odkazy na jiné symboly. Tyto vlastnosti jsou uvedeny v tématech pro jednotlivé symbol.  
  
## <a name="see-also"></a>Viz také  
 [Cv_access_e – výčet](../../debugger/debug-interface-access/cv-access-e.md)   
 [Lexikální hierarchie typů symbolů](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [Symboly a značky symbolů](../../debugger/debug-interface-access/symbols-and-symbol-tags.md)



