---
title: "Vsperfmon – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- VSPerfMon tool
- command line, tools
- command-line tools, VSPerfMon tool
- data [Visual Studio ALM], VSPerfMon tool
- performance data, VSPerfMon tool
- performance tools, VSPerfMon tool
- profilng tools,VSPerfCmd
ms.assetid: 37052afb-7a58-441f-bb17-f1587cc57068
caps.latest.revision: "30"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8fe5e6b129fd8c5f1e8ce20bb902b977a66f1035
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="vsperfmon"></a>VSPerfMon
Vsperfmon – nástroj můžete použít ke shromažďování dat výkonu pro aplikace. Tento nástroj se obvykle spustit VSPerfCmd.exe. Vsperfmon – zobrazí informace o procesu připojení nebo odpojení, která není k dispozici pomocí vsperfcmd – nástroj. Chcete-li tyto informace zobrazit, spusťte vsperfmon – v samostatném okně. Vsperfmon – k vyvolání použijte následující syntaxi:  
  
```  
VSPerfMon [/U] </TRACE [/COUNTER:cfg] | /SAMPLE | /COVERAGE> /CROSSSESSION /OUTPUT <file name> [/WINCOUNTER:cfg] [/USER [DOMAIN\]username]  
```  
  
 Následující tabulka popisuje možnosti vsperfmon – nástroj:  
  
|Možnosti|Popis|  
|-------------|-----------------|  
|**U**|Výstup konzoly přesměrovaného je zapsána jako kódování Unicode.  Toto musí být první možnost zadat.|  
|**VÝSTUP:** `<` *název souboru*`>`|Provede přesměrování výstupu pro zadaný název souboru.|  
|**TRASOVÁNÍ**|Spustí monitorování výkonu pro instrumentovaného profilace.|  
|**UKÁZKA**|Spustí monitorování výkonu pro profilace vzorkování.|  
|**POKRYTÍ**|Spustí monitorování výkonu pro shromažďování pokrytí kódu.|  
|**SOUBĚŽNOSTI**|Spustí monitorování výkonu pro profilace kolizí prostředku.|  
|**UŽIVATEL:** `[` *domény* `\]` *uživatelské jméno*|Umožňuje přístup klienta k monitorování výkonu ze zadaného účtu.|  
|**CROSSSESSION**|Umožňuje profilace mezi relace.|  
|**ČÍTAČ**`:cfg`|Pokud se používá metoda profilování instrumentace (trasování), určuje čítačů procesoru, které se mají shromažďovat u každého bodu instrumentace. Můžete shromáždit více dat čítačů zadáním více možností čítače.<br /><br /> Použijte následující syntax k určení čítač (*cfg*) data:<br /><br /> **Název_čítače** [**, načtěte**[,**FriendlyName**]]<br /><br /> -   **Název_čítače** je název čítače vrácené příkazem /QueryCounters VSPerfCmd.<br />-   **Načtěte** je interval vzorkování událostí čítače. Nepoužívejte *opětovného načtení* pomocí metody instrumentace.<br />-Li zadána, **FriendlyName** nahrazuje **název_čítače** v nástrojích pro profilaci sestavy názvy sloupců.|  
|**WINCOUNTER**`:path`|Určuje čítačů výkonu systému Windows mají být součástí značky data. `path`je řetězec čítače výkonu systému Windows v formát cesty PDH čítače. Příklad:<br /><br /> \Processor(0)\\% času procesoru<br /><br /> Přepnutí \System\Context za sekundu|  
|**PRO AUTOMATICKÉ OZNAČOVÁNÍ**`:n`|Určuje časový interval (v milisekundách) mezi automatické značky, pokud používáte /WINCOUNTER. Zaokrouhlená na nejbližší 500ms.<br /><br /> Použijte hodnotu 0, chcete-li zakázat automatické značky. (výchozí = 500ms-li tento parametr)|  
  
## <a name="see-also"></a>Viz také  
 [Vsinstr –](../profiling/vsinstr.md)   
 [Vsperfcmd –](../profiling/vsperfcmd.md)   
 [Vsperfreport –](../profiling/vsperfreport.md)   
 [Zobrazení sestav výkonu](../profiling/performance-report-views.md)