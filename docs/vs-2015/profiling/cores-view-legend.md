---
title: Legenda zobrazení jader | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.cores.legend
helpviewer_keywords:
- Concurrency Visualizer, Cores View Legend
ms.assetid: e160384c-fcfe-49b3-86b7-229adb736c51
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6416b9bf96b3a23fce72df56190df9dfd5847531
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42679500"
---
# <a name="cores-view-legend"></a>Legenda zobrazení jader
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [Legenda zobrazení jader](https://docs.microsoft.com/visualstudio/profiling/cores-view-legend).  
  
Legenda zobrazení jader identifikuje každý podproces, barvu a název. Obsahuje sloupce, které zobrazují počty pro přepnutí kontextu mezi jádry a celkem přepnutí kontextu, procento přepínačů kontextů napříč jádry. Řádky v legendě jsou seřazené podle počtu přepínače kontextu mezi jádry v sestupném pořadí.  
  
 Výběr řádků v legendě pro filtrování vláken, která se zobrazí na časové ose. Na časové ose se zobrazí jen vybraná vlákna. Pokud nejsou vybrány žádné řádky, zobrazí se všechny řádky na časové ose.  
  
 Kontextu mezi jádry přepne náklady na další režii a výkonu než přepínače, které zůstávají ve stejné logické jádro. Při přepnutí kontextu registrech procesoru jsou uložený a obnovený, spuštění kódu jádra operačního systému, jsou znovu načíst položky překladu Page Table Entry vyrovnávací paměti a procesoru kanál vyprazdňuje. Přepnutí kontextu mezi jádry může být i dražší než jiné přepnutí kontextu, protože není platný pro toto vlákno na jiné základní data v mezipaměti. Naproti tomu Pokud vlákno přepnout kontext na jádro, které dříve spuštěno na, je pravděpodobné, že je užitečná data stále v mezipaměti. Při přepnutí kontextu mezi jádry zvýšily pokoušejí spravovat vlákno má snížený výkon a vztahů, zvažte, jestli chcete tento problém vyřešit. Začněte tím, že odstranění spřažení vláken a poté můžete sledovat výsledné chování napříč jádry.  
  
 Následující tabulka popisuje prvky legendy.  
  
|Prvek|Definice|  
|-------------|----------------|  
|Název vlákna|V předchozí časová osa jader a název tohoto vlákna se zobrazuje barva vlákna.|  
|Přepnutí kontextu mezi jádry|Počet přepnutí kontextu pro vlákno, které také přepnout z jednoho logického jádra do jiného. Se nerozlišují varianty jádro přepínačů kontextů napříč z kostka jeden procesor do jiného a ty, které zůstat na stejném kostka.|  
|Celkem přepnutí kontextu|Celkový počet přepnutí kontextu pro dané vlákno během intervalu získávání vzorků. Pokaždé, když vlákno změní jeden přepnutí kontextu kontextu (například ze spuštění synchronizace) se počítá.|  
|Procento přepínačů kontextů napříč jádry|Vypočítaná jako procento aplikací jako podíl počtu kontextu mezi jádry přepínače podle počtu celkem přepnutí kontextu. Čím vyšší toto procento, tím větší celkového efektu režii kontextu mezi jádry přepne na výkon toto konkrétní vlákno.|  
  
## <a name="see-also"></a>Viz také  
 [Zobrazení jader](../profiling/cores-view.md)



