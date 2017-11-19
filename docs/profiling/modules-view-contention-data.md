---
title: "Zobrazení modulů – Data kolizí | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Modules view
ms.assetid: 1a9aa122-2d8f-4a09-b503-92975aa6b648
caps.latest.revision: "12"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fae0bd48af8c9fbaaaf8c38f50a2fe8233f15cb3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="modules-view---contention-data"></a>Zobrazení modulů – Data kolizí
Moduly zobrazení dat kolizí zobrazí seskupené podle moduly, které byly v data profilování vzorků dat souběžnosti. Každý modul je kořenem hierarchickou stromovou strukturu. Funkce modulu došlo k kolizní události jsou uvedené pod uzlem modulu.  
  
 Pokud funkce byla spuštěna vlastní kód, při kolizní událostí došlo k chybě, to znamená, funkce se v horní části zásobníku volání, původní řádky a instrukce, adresy, které byly provádění jsou uvedeny pod uzlem funkce. Protože je prováděna řádek nebo instrukce je řádku zdroje nebo ukazatele instrukce shromažďovat data, včetně a výhradní hodnoty jsou vždy stejné pro řádek data a instrukce data.  
  
 Následující tabulka popisuje hodnoty ve sloupcích v moduly zobrazení dat kolizí.  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**Výhradní blokované čas**|-Pro funkce, čas, který tuto funkci byl zablokován spuštěním kódu v těle funkce. Blokované čas v funkce, které byly volá funkci není součástí.<br />-Pro modul, součet výhradní blokované čas funkce v modulu.<br />-Pro řádek nebo instrukce, čas, které tento řádek nebo byl zablokován spouštění instrukcí.|  
|**Výhradní blokované čas: %**|-Pro modul nebo funkci procento všech blokovaných času v profilaci spuštění, který byl výhradní blokované době tento modul nebo funkce.<br />-Pro řádek nebo instrukce, procento všech blokovaných čas v profilaci spustit ve které tento řádek nebo instrukce byl zablokován provádění.|  
|**Výhradní kolizí**|-Pro funkce, počet pokusů, které tuto funkci byl zablokován spuštěním kódu v těle funkce. Kolizí ve funkcích, které byly volá funkci nejsou zahrnuty.<br />-Pro modul, součet výhradní kolizí funkcí v modulu.<br />-Pro řádek nebo instrukce, kolikrát že tento řádek nebo instrukce byl zablokován provádění.|  
|**% Výhradní kolizí**|-Pro modul nebo funkci procento všech kolizí v profilaci spuštění, které byly výhradní kolizí této funkce nebo modul.<br />-Pro řádek nebo instrukce procento všech kolizí v profilaci spuštění, které byly kolizí zablokované tento řádek nebo instrukce spuštění.|  
|**Blokované čas (včetně).**|-Pro funkce, čas, který tuto funkci nebo funkci, která byla volána pomocí této funkce byl zablokován provádění.<br />-Pro modul součet blokované čas v funkce, jejíž alespoň jeden z tento modul byl v zásobníku.<br />-Pro řádek nebo instrukce, čas, které tento řádek nebo byl zablokován spouštění instrukcí.|  
|**Včetně blokované čas: %**|-Pro modul nebo funkci byl procento všech blokovaných času v profilaci spustit, včetně blokované čas tento modul nebo funkce.<br />-Pro řádek nebo instrukce procento všech blokovaných času v profilaci spustit ve které tento řádek nebo instrukce provádění.|  
|**Kolizí (včetně).**|-Pro funkce, počet pokusů, které tuto funkci nebo funkci, která byla volána pomocí této funkce byl zablokován provádění.<br />-Pro modul Počet kolizí v funkce, jejíž alespoň jeden z tento modul byl v zásobníku.<br />-Pro řádek nebo instrukce, kolikrát že tento řádek nebo instrukce byl zablokován provádění.|  
|**% Kolizí (včetně).**|-Pro modul nebo funkci procento všech kolizí v profilaci spuštění, které byly včetně kolizí této funkce nebo modul.<br />-Pro řádek nebo instrukce procento všech blokovaných času v profilaci spustit ve které tento řádek nebo instrukce provádění.|  
|**Číslo řádku – funkce**|Číslo řádku spuštění této funkce ve zdrojovém souboru.|  
|**Název modulu**|Název modul, který obsahuje funkce, čáry nebo instrukce ukazatele.|  
|**Cesta modulu**|Cesta modul, který obsahuje ukazatele modulu, funkce, čáry nebo instrukcí.|  
|**Jméno**|Název modulu nebo funkce.|  
|**ID procesu**|ID procesu (PID) z profilace spustit.|  
|**Název procesu**|Název procesu.|  
|**Zdrojový soubor**|Zdrojový soubor, který obsahuje definici pro tuto funkci.|  
  
## <a name="see-also"></a>Viz také  
 [Postupy: přizpůsobení sloupců zobrazení sestavy](../profiling/how-to-customize-report-view-columns.md)   
 [Zobrazení modulů](../profiling/modules-view.md)   
 [Zobrazení modulů – instrumentace](../profiling/modules-view-dotnet-memory-instrumentation-data.md)   
 [Moduly zobrazení – vzorkování](../profiling/modules-view-dotnet-memory-sampling-data.md)   
 [Zobrazení modulů](../profiling/modules-view-instrumentation-data.md)   
 [Zobrazení modulů](../profiling/modules-view-sampling-data.md)