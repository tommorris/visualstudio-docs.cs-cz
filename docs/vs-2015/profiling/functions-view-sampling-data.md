---
title: Zobrazení funkcí – vzorkování dat | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- sampling profiling method,Functions View
- Functions view
ms.assetid: 029d5ebb-e551-46b0-b64e-2c553d9dbb8e
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3813c306c2240e7b9db0e8e3d5cbf5929cf0cf91
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629653"
---
# <a name="functions-view---sampling-data"></a>Zobrazení funkcí – vzorkování dat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [zobrazení funkcí – Data vzorkování](https://docs.microsoft.com/visualstudio/profiling/functions-view-sampling-data).  
  
Zobrazení sestav funkce pro požadovanou metodu profilu odběru vzorků jsou uvedeny funkce, které byly vzorkovány během spuštění profilování.  
  
> [!NOTE]
>  Rozšířené funkce zabezpečení v systému Windows 8 a Windows Server 2012 vyžadují významné změny ve způsobu, jakým profiler systému Visual Studio na těchto platformách shromažďuje data. Aplikace Windows Store také vyžadují nové techniky kolekce. Zobrazit [nástroje pro výkon v aplikacích Windows 8 a Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**ID procesu**|ID procesu (PID) běhu profilování.|  
|**Název procesu**|Název procesu.|  
|**Název modulu**|Název modulu, který obsahuje funkci.|  
|**Cesta modulu**|Cesta k napadenému modulu, který obsahuje funkci.|  
|**Zdrojový soubor**|Zdrojový soubor, který obsahuje definici pro tuto funkci.|  
|**Název funkce**|Plně kvalifikovaný název funkce.|  
|**Číslo řádku funkce**|Číslo řádku začátku této funkce ve zdrojovém souboru.|  
|**Adresa funkce**|Adresa funkce.|  
|**Celkových vzorků**|Celkový počet vzorků, které byly shromážděny při provádění této funkce; To znamená, počet vzorků, které byly shromážděny při této funkce v zásobníku volání. Počet obsahuje ukázky, které byly shromážděny při byly provádění funkcí, které byly volány touto funkcí.|  
|**% Celkových vzorků**|Procento všechny ukázky v profilování, které byly celkových vzorků této funkce.|  
|**Výhradní vzorky**|Celkový počet vzorků, které byly shromážděny při provádění kódu v těle této funkce; To znamená, když tato funkce byla vrcholu zásobníku volání. Ukázky, které byly shromážděny ve funkcích, které byly volány touto funkcí nejsou zahrnuty.|  
|**% Výhradních vzorků**|Procento všechny ukázky v profilování, které byly výhradních vzorků této funkce.|  
  
## <a name="see-also"></a>Viz také  
 [Postupy: přizpůsobení sloupců zobrazení sestavy](../profiling/how-to-customize-report-view-columns.md)   
 [Zobrazení funkcí – instrumentace](../profiling/functions-view-dotnet-memory-instrumentation-data.md)   
 [Zobrazení funkcí – vzorkování](../profiling/functions-view-dotnet-memory-sampling-data.md)   
 [Zobrazení funkcí](../profiling/functions-view-instrumentation-data.md)



