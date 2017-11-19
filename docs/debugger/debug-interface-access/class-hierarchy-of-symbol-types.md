---
title: "Třídy hierarchie typů symbolů | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: symbols [DIA SDK], class hierarchies
ms.assetid: 0ccd6990-4654-44cd-a6f3-bdd82fe90f6c
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a89cc0342ed5b9d4e1fcb85cbc84e124588d9c9b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="class-hierarchy-of-symbol-types"></a>Hierarchie tříd typů symbolů
Následující tabulka popisuje typy symbol v hierarchii tříd.  
  
## <a name="symbol-types"></a>Symbol typy  
  
|Typ symbolu|Popis|  
|-----------------|-----------------|  
|[UDT](../../debugger/debug-interface-access/udt.md)|Symbol používají k vyjádření každé třídy, struktury a sjednocení|  
|[Výčet (přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/enum-debug-interface-access-sdk.md)|Symbol pro výčtové typy.|  
|[Pointertype –](../../debugger/debug-interface-access/pointertype.md)|Symbol pro typy ukazatelů.|  
|[ArrayType](../../debugger/debug-interface-access/arraytype.md)|Symbol pro typy polí.|  
|[Základní typ BaseType](../../debugger/debug-interface-access/basetype.md)|Symbol pro základní typy|  
|[TypeDef (přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/typedef-debug-interface-access-sdk.md)|Symbol, který představuje názvy pro ostatní typy.|  
|[Baseclass –](../../debugger/debug-interface-access/baseclass.md)|Symbolu používanou pro každou základní třídu uživatelem definovaný typ (UDT).|  
|[Přítel (přístup k rozhraní ladění SDK)](../../debugger/debug-interface-access/friend-debug-interface-access-sdk.md)|Symbol pro friend – třídy a funkce, přítele.|  
|[Functiontype –](../../debugger/debug-interface-access/functiontype.md)|Symbol pro každý podpis jedinečné funkce.|  
|[Functionargtype –](../../debugger/debug-interface-access/functionargtype.md)|Symbol pro každý parametr funkci.|  
|[Vtableshape –](../../debugger/debug-interface-access/vtableshape.md)|Symbol pro velikost virtuální tabulky.|  
|[VTable](../../debugger/debug-interface-access/vtable.md)|Symbol pro virtuální tabulku.|  
|[CustomType](../../debugger/debug-interface-access/customtype.md)|Symbol pro typ definované dodavatelem.|  
|[Spravovaného typu](../../debugger/debug-interface-access/managedtype.md)|Symbol pro typ definované v metadatech.|  
|[Dimenze](../../debugger/debug-interface-access/dimension.md)|Symbol pro rozměry pole.|  
  
> [!NOTE]
>  Každý symbol může mít vlastnosti, které obsahují informace o symbol, jakož i odkazy na další symboly. Tyto vlastnosti jsou uvedeny v tématech jednotlivých symbol.  
  
## <a name="see-also"></a>Viz také  
 [CV_access_e – výčet](../../debugger/debug-interface-access/cv-access-e.md)   
 [Lexikální hierarchie typů symbolů](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [Symboly a značky symbolů](../../debugger/debug-interface-access/symbols-and-symbol-tags.md)