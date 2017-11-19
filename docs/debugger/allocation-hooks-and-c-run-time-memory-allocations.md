---
title: "Háky přidělení a přidělení běhové paměti jazyka C | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], hook functions
- memory allocation, troubleshooting allocation hooks
- allocation hooks
- hooks, allocation
ms.assetid: cc34ee96-3d91-41bd-a019-aa3759139e7e
caps.latest.revision: "14"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62a8be3b1a1c98a330efeb26d9a84e74f2334423
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="allocation-hooks-and-c-run-time-memory-allocations"></a>Háky přidělení a přidělení běhové paměti jazyka C
Velmi důležité omezení na funkce háku přidělení je, že se musí explicitně Ignorovat `_CRT_BLOCK` bloky (přidělení paměti interně provedené funkce běhové knihovny jazyka C) Pokud udělají jakékoli volání funkce běhové knihovny jazyka C, které přidělují interní paměť. `_CRT_BLOCK` Bloky můžete ignorovat zahrnutím kódu, například následující na začátku vaší přidělení napojit funkce:  
  
```  
if ( nBlockUse == _CRT_BLOCK )  
    return( TRUE );  
```  
  
 Pokud vaše háku přidělení neignoruje `_CRT_BLOCK` blokuje, pak všechny funkce běhové knihovny jazyka C volal v vaší háku můžete depeše programu v nekonečné smyčce. Například `printf` díky interní přidělení. Pokud váš kód háku volá `printf`, pak výsledné přidělení způsobí háku říkalo akci, která bude volat **printf** znovu, a tak dále dokud přetečení zásobníku. Pokud potřebujete sestavy `_CRT_BLOCK` přidělení operace, je možné toto omezení obejít používat funkce rozhraní API systému Windows, nikoli C běhové funkce, pro formátování a výstup. Protože rozhraní API systému Windows nepoužívejte haldě běhové knihovny jazyka C, se nebude depeše vaší háku přidělení v nekonečné smyčce.  
  
 Pokud si projdete běhové knihovny zdrojové soubory, zobrazí se, že výchozí přidělení napojit funkce, **CrtDefaultAllocHook** (která vrací jednoduše **TRUE**), se nachází v samostatném souboru své vlastní, DBGHOOK. C. Pokud chcete, aby vaše háku přidělení, která se má volat i pro přidělení provedené spuštění běhu kód, který se spustí před vaší aplikace **hlavní** funkce, můžete nahradit výchozí funkci s vlastním, místo pomocí [_crtsetallochook –](/cpp/c-runtime-library/reference/crtsetallochook).  
  
## <a name="see-also"></a>Viz také  
 [Zápis funkce háku ladění](../debugger/debug-hook-function-writing.md)   
 [Ukázka crt_dbg2](http://msdn.microsoft.com/en-us/21e1346a-6a17-4f57-b275-c76813089167)