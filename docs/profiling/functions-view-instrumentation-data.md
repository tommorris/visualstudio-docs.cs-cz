---
title: "Zobrazení funkcí – Data instrumentace | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Function view
ms.assetid: 595d91c8-a42b-4644-85b8-39e8140a5dfe
caps.latest.revision: "11"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 582ec23192001b262938a82b9867ae82805e0cab
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="functions-view---instrumentation-data"></a>Zobrazení funkcí – Data instrumentace
Zobrazení sestavy funkce uvádí data profilování podle názvu funkce.  
  
## <a name="general"></a>Obecné  
 Obecné sloupce rozpoznat funkci v řádku zobrazení.  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**Název funkce**|Název funkce.|  
|**Adresa funkce**|Adresa funkce.|  
|**Číslo řádku – funkce**|Číslo řádku spuštění této funkce ve zdrojovém souboru.|  
|**Počet volání**|Celkový počet volání této funkce.|  
|**Zdrojový soubor**|Zdrojový soubor, který obsahuje definici pro tuto funkci.|  
|**Název modulu**|Název modulu, který obsahuje funkci.|  
|**Cesta modulu**|Cesta modul, který obsahuje funkce.|  
|**ID procesu**|ID procesu (PID) z profilace spustit.|  
|**Název procesu**|Název procesu.|  
|**Režijní náklady na čas výhradní testu**|Čas režie pro tuto funkci, která je způsobeno tím instrumentace. Funkce, které byly volá funkci neobsahoval režijní náklady. Režijní náklady na test odečtení od sebe výhradní.|  
|**Režijní náklady na čas včetně testu**|Čas režie pro tuto funkci a jeho podřízené funkce způsobený instrumentace. Režijní náklady na ji zahrnout do funkce, které byly volá funkci. Test režie odečtení od sebe (včetně).|  
  
## <a name="elapsed-inclusive-values"></a>Uplynulá (včetně) hodnot  
 Uplynulá (včetně) hodnot označuje datum a čas, který byl funkce v zásobníku volání. Čas zahrnout času stráveného funkce, které byly volat funkce a času stráveného v volání operačního systému, jako jsou přepínače kontextu a vstupně výstupní operace.  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**Uplynulý čas (včetně).**|Celkový počet uplynulý čas včetně všechna volání této funkce.|  
|**% Uplynulá doba (včetně).**|Procento celkového počtu uplynulý čas včetně čas spuštění profilování stráveného při uplynulá doba včetně této funkce.|  
|**Průměr uplynulý čas včetně čas**|Průměr uplynulý čas včetně volání této funkce.|  
|**Maximální uplynulá doba (včetně).**|Maximální uplynulý čas včetně volání této funkce.|  
|**Min uplynulý čas včetně čas**|Minimální uplynulý čas včetně volání této funkce.|  
  
## <a name="elapsed-exclusive-values"></a>Uplynulá výhradní hodnoty  
 Uplynulá výhradní hodnoty označuje datum a čas, že funkce byla spuštěna kódu v těle funkce, tedy při funkce byla v horní části zásobníku volání. Čas zahrnovat času stráveného v volání operačního systému, jako jsou přepínače kontextu a vstupně-výstupních operací, ale nezahrnuje času stráveného v funkce, které byly volá funkci.  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**Uplynulá doba výhradní**|Celkový počet uplynulý čas výhradní všechna volání této funkce.|  
|**Uplynulý čas výhradní %**|Procento celkového počtu uplynul výhradní času stráveného při celková doba uplynulá výhradní této funkce spuštění profilování.|  
|**Průměr uplynulý exkluzivní čas**|Průměr uplynulý čas výhradní volání této funkce.|  
|**Maximální uplynulá doba výhradní**|Maximální uplynulý čas výhradní volání této funkce.|  
|**Min uplynulý exkluzivní čas**|Minimální uplynulý čas výhradní volání této funkce.|  
  
## <a name="application-inclusive-values"></a>Aplikace (včetně) hodnot  
 Aplikace (včetně) hodnot označuje datum a čas, který byl funkce v zásobníku volání. Čas nezahrnuje času stráveného v volání operačního systému, jako jsou přepínače kontextu a vstupně-výstupních operací, ale nezahrnuje času stráveného v funkce, které byly volá funkci.  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**Doba aplikace (včetně).**|Celkový počet aplikací čas včetně všechna volání této funkce.|  
|**Aplikace % času (včetně).**|Procento celkového počtu uplynulý čas včetně čas spuštění profilování stráveného v čase (včetně). Celkový počet aplikací této funkce.|  
|**Prům. čas včetně aplikace**|Průměrná aplikace čas včetně volání této funkce.|  
|**Maximální doba včetně aplikace**|Čas (včetně). maximální aplikace volání této funkce.|  
|**Doba včetně aplikace min.**|Čas včetně minimální aplikace volání této funkce.|  
  
## <a name="application-exclusive-values"></a>Výhradní hodnoty aplikace  
 Aplikace hodnot, které označuje datum a čas, která funkce byla spuštěna přímo v horní části zásobníku volání. Čas nezahrnuje času stráveného v volání operačního systému, jako jsou přepínače kontextu a vstupně-výstupních operací, a nezahrnuje času stráveného v funkce, které byly volá funkci.  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**Výhradní doba aplikace**|Celkový počet aplikací čas výhradní všechna volání této funkce.|  
|**Aplikace % výhradní čas**|Procento celkového počtu uplynul výhradní času stráveného při výhradní doba celkový aplikace této funkce spuštění profilování.|  
|**Prům. čas výhradní aplikace**|Průměrná aplikace čas výhradní volání této funkce.|  
|**Maximální doba výhradní aplikace**|Čas výhradní maximální aplikace volání této funkce.|  
|**Doba výhradní aplikace min.**|Čas výhradní minimální aplikace volání této funkce.|  
  
## <a name="see-also"></a>Viz také  
 [Postupy: přizpůsobení sloupců zobrazení sestavy](../profiling/how-to-customize-report-view-columns.md)   
 [Zobrazení funkcí](../profiling/functions-view-sampling-data.md)   
 [Zobrazení funkcí – vzorkování](../profiling/functions-view-dotnet-memory-sampling-data.md)   
 [Zobrazení funkcí – instrumentace](../profiling/functions-view-dotnet-memory-instrumentation-data.md)