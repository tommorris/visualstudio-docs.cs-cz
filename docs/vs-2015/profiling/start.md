---
title: Spuštění | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: b85d0fe9-f67a-4b7c-8d48-7eecf3f2dfe9
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 14a68592a350c7c5604f6d7af3037eecf6c9d3e9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42683206"
---
# <a name="start"></a>Spustit
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [Start](https://docs.microsoft.com/visualstudio/profiling/start).  
  
**Start** je možnost možností VSPerfCmd.exe, která inicializuje profiler k zadané metodě profilování.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
VSPerfCmd.exe /Start:Method /Output:FileName [Options]  
```  
  
#### <a name="parameters"></a>Parametry  
 `Method`  
 Musí být jedna z následujících klíčových slov:  
  
-   **TRASOVÁNÍ** -určuje metody instrumentace.  
  
-   **Ukázka** -určuje metody vzorkování.  
  
-   **POKRYTÍ** -určuje pokrytí kódu.  
  
-   **SOUBĚŽNOST** -určuje metodu kolize prostředků.  
  
## <a name="required-options"></a>Požadované možnosti  
 **Výstup** možnost musí být zadán při **Start** je zadán v příkazovém řádku.  
  
 **Výstup:** `filename`  
 Určuje název výstupního souboru.  
  
## <a name="exclusive-options"></a>Výhradní možnosti  
 Tyto možnosti lze použít pouze s **Start** možnost příkazového řádku.  
  
 **CrossSession**&#124;**CS**  
 Umožňuje procesy profilace. Názvy možností **CrossSession** a **CS** jsou podporovány.  
  
 **Uživatel:**[`domain\`]`username`  
 Umožňuje přístup klienta k monitoru ze zadaného účtu.  
  
 **WinCounter:** `Path` [**Automark**:`n`]  
 **WinCounter** určuje čítač výkonu Windows zahrnout jako značky v souboru dat profilování. **AutoMark** Určuje interval v milisekundách mezi kolekcemi datového souboru.  
  
## <a name="invalid-options"></a>Neplatné možnosti  
 Tyto možnosti nelze použít s **Start** možnost příkazového řádku.  
  
 **Status**  
 **Stav** se vztahuje na tyto procesy, které jsou profilovány. Vypíše procesy a vlákna a jejich aktuální stavy profilu (zapnuto/vypnuto). Například, pokud proces zastavená **stav** nebude to znamenat v sestavě. **Stav** se zobrazí, že je buď profilována procesu nebo ne.  
  
 **Vypnutí**[**:**`Timeout`]  
 Vypne profilování.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje způsob použití VSPerfCmd.exe **Start** možnost pro inicializaci profileru.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
```  
  
## <a name="see-also"></a>Viz také  
 [Nástroj VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profilace samostatných aplikací](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profilace webových aplikací ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profilace služeb](../profiling/command-line-profiling-of-services.md)



