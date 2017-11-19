---
title: "Zobrazení (IP) ukazatele na instrukce – vzorkování dat | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Instruction Pointers view
ms.assetid: c7f647bb-c5a3-4708-9f9d-33c0fd6e2e96
caps.latest.revision: "11"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b328a12e2b82f6aa688180d9ac57066552e808c9
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2017
---
# <a name="instruction-pointers-ips-view---sampling-data"></a>Zobrazení (IP) ukazatele na instrukce – vzorkování dat
Zobrazení IP adres vzorkování dat výkonu datového seznamy pokyny sestavení, které byly prováděny přímo, kdy ukázky byly shromážděny v profilaci spustit.  
  
> [!NOTE]
>  Funkce Rozšířené zabezpečení v systému Windows 8 a Windows Server 2012 vyžaduje významné změny ve způsobu, jakým Visual Studio profiler shromažďuje data na těchto platformách. Aplikace UWP také vyžadují nové techniky kolekce. V tématu [nástroje pro sledování výkonu v aplikacích pro Windows 8 a Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
|Sloupec|Popis|  
|------------|-----------------|  
|**ID procesu**|ID procesu (PID) z profilace spustit.|  
|**Název procesu**|Název procesu.|  
|**Název modulu**|Název modul, který obsahuje pokyn.|  
|**Cesta modulu**|Cesta modul, který obsahuje pokyn.|  
|**Zdrojový soubor**|Zdrojový soubor, který obsahuje pokyn.|  
|**Název funkce**|Název funkce, která obsahuje pokyn.|  
|**Číslo řádku – funkce**|Číslo řádku spuštění této funkce ve zdrojovém souboru.|  
|**Adresa funkce**|Počáteční adresa paměti funkce v načíst binárního souboru.|  
|**Začátek řádku zdroje**|Počáteční řádek číslo ve zdrojovém souboru, kdy byl shromážděn této ukázce.|  
|**End řádku zdroje**|Koncová číslo řádku ve zdrojovém souboru, kdy byl shromážděn této ukázce.|  
|**Začátek znaku zdroje**|Posun počáteční znak v řádku souboru původního, kdy byl shromážděn této ukázce.|  
|**End znaku zdroje**|Posun ukončovací znak v řádku souboru zdroje, kdy byl shromážděn této ukázce.|  
|**Adresa instrukce**|Adresa instrukce v načíst binárního souboru.|  
|**Výhradní ukázky**|Celkový počet vzorků, které byly shromážděny při provádění pokynů.|  
|**% Výhradní ukázky**|Procento všechny ukázky v profilaci spuštění, které byly shromážděny při provádění pokynů.|  
  
## <a name="see-also"></a>Viz také  
 [Ukazatele na instrukce (IP) zobrazení – vzorkování](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)