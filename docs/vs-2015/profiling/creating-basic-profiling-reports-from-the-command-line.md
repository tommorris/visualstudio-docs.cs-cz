---
title: Vytváření sestav z příkazového řádku pro profilaci Basic | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6d73e21e-c04e-48ea-91cc-e517a5f2cd3f
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f237388f1e15a461bb61ee8862f0fe466180aaef
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666714"
---
# <a name="creating-basic-profiling-reports-from-the-command-line"></a>Vytváření základních sestav profilace z příkazového řádku
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [vytváření základní profilování sestavy, z příkazového řádku](https://docs.microsoft.com/visualstudio/profiling/creating-basic-profiling-reports-from-the-command-line).  
  
Toto téma popisuje základní příkazy VSPerfReport, které generují sestavy hodnot oddělených čárkami (.csv) z .vsp nebo .vsps souboru dat profilování. Popis všech možností sestavy naleznete v tématu [VSPerfReport](../profiling/vsperfreport.md).  
  
## <a name="report-commands"></a>Příkazy sestavy  
 Použijte jednu z následujících příkazů pro vytvoření sestavy pro zadaný soubor dat profilování.  
  
 **VSPerfReport** `VSPFile` **Summary**  
 Generuje všechny sestavy, které jsou k dispozici pro soubor .vsp nebo .vsps.  
  
 **VSPerfReport** `VSPFile` **/Summary:**`ReportType`[,`ReportType`...]  
 Generuje zadané typy sestavy.  
  
 **VSPerfReport** `VSPFile`   **/calltrace**  
 Generuje sestavu, která obsahuje každou událost shromažďování dat. Pouze instrumentace.  
  
## <a name="summary-report-type-parameters"></a>Parametry typu souhrnné sestavy  
 Následující tabulka popisuje sestavy, které se vygenerovaly zadanou možností typu sestavy. Sloupce sestavy závisí na metodu, která byla použita pro sběr dat profilace.  
  
|Souhrnný parametr|Popis sestavy|Referenční informace o sestavách|  
|-----------------------|------------------------|----------------------|  
|**CallerCallee**|Představuje nadřazené a podřízené vztahy mezi funkcemi.|-   [Vzorkování dat](../profiling/caller-callee-view-sampling-data.md)<br />-   [Data instrumentace](../profiling/caller-callee-view-instrumentation-data.md)<br />-   [Data vzorkování paměti .NET](../profiling/caller-callee-view-dotnet-memory-sampling-data.md)<br />-   [Data instrumentace paměti .NET](../profiling/caller-callee-view-net-memory-instrumentation-data.md)<br />-   [Data kolizí](../profiling/caller-callee-view-contention-data.md)|  
|**– funkce**|Uvádí data profilování dle funkce.|-   [Vzorkování dat](../profiling/functions-view-sampling-data.md)<br />-   [Data instrumentace](../profiling/functions-view-instrumentation-data.md)<br />-   [Data vzorkování paměti .NET](../profiling/functions-view-dotnet-memory-sampling-data.md)<br />-   [Data instrumentace paměti .NET](../profiling/functions-view-dotnet-memory-instrumentation-data.md)<br />-   [Data kolizí](../profiling/functions-view-contention-data.md)|  
|**Stromu volání**|Představuje cesty spuštění a data profilování funkcí během spuštění profilování.|-   [Data instrumentace](../profiling/call-tree-view-instrumentation-data.md)<br />-   [Vzorkování dat](../profiling/call-tree-view-sampling-data.md)<br />-   [Data vzorkování paměti .NET](../profiling/call-tree-view-dotnet-memory-sampling-data.md)<br />-   [Data instrumentace paměti .NET](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)<br />-   [Data kolizí](../profiling/call-tree-view-contention-data.md)|  
|**Counter**|Uvádí profilovací značky a hodnoty čítače výkonu Windows, které byly shromážděny během spuštění profilování.|-   [Zobrazení značek](../profiling/marks-view.md)|  
|**IP**|Uvádí data profilování podle instrukce.|-   [Vzorkování dat](../profiling/instruction-pointers-ips-view-sampling-data.md)<br />-   [Data vzorkování paměti .NET](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)<br />-   [Data kolizí](../profiling/instruction-pointers-ips-view-contention-data.md)|  
|**Životnost**|Uvádí dobu životnosti přidělených objektů.|-   [Zobrazení doby života objektu](../profiling/object-lifetime-view.md)|  
|**Řádek**|Uvádí data profilování pomocí řádku zdrojového kódu.|-   [Vzorkování dat](../profiling/lines-view-sampling-data.md)<br />-   [Data vzorkování paměti .NET](../profiling/lines-view-dotnet-memory-sampling-data.md)<br />-   [Data kolizí](../profiling/lines-view-contention-data.md)|  
|**Záhlaví**|Informace hlavičky souboru dat profilování.|Specifické pro soubor.|  
|**Mark**|Profilovací značky shromážděné při spuštění profilování.|-   [Zobrazení značek](../profiling/marks-view.md)|  
|**Modul**|Uvádí data profilování pro moduly.|-   [Vzorkování dat](../profiling/modules-view-sampling-data.md)<br />-   [Data instrumentace](../profiling/modules-view-instrumentation-data.md)<br />-   [Data vzorkování paměti .NET](../profiling/modules-view-dotnet-memory-sampling-data.md)<br />-   [Data instrumentace paměti .NET](../profiling/modules-view-dotnet-memory-instrumentation-data.md)<br />-   [Data kolizí](../profiling/modules-view-contention-data.md)|  
|**Proces**|Uvádí data profilování pro procesy.|-   [Zobrazení procesů](../profiling/process-view.md)<br />-   [Data kolizí](../profiling/process-view-contention-data.md)|  
|**vlákno**|Uvádí data profilování pro vlákna.|-   [Zobrazení procesů](../profiling/process-view.md)|  
|**Typ**|Uvádí data profilování přidělení podle typu.|-   [Přidělení – zobrazení](../profiling/dotnet-memory-allocations-view.md)|  
|**Kolize**|Sporty prostředků.|-   [Sporty prostředků](../profiling/resource-contentions-view-contention-data.md)|  
|**RuleWarnings**|Uvádí problémy pravidla výkonu.|-Uvádí CheckId, popis a umístění zdrojového kódu problému pravidla.|  
|**TRASOVÁNÍ UDÁLOSTÍ PRO WINDOWS**|Události trasování událostí pro Windows (ETW) shromážděné při spuštění profilování.|-   [Sestava trasování událostí pro Windows](../profiling/event-tracing-for-windows-etw-report.md)|



