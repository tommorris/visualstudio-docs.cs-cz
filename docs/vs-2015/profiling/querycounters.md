---
title: QueryCounters | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8059d4b2-af61-4a47-a6c2-8da5c0741c74
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ff5cd703a323c93c479d69bbe956855106d80d80
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633178"
---
# <a name="querycounters"></a>QueryCounters
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [QueryCounters](https://docs.microsoft.com/visualstudio/profiling/querycounters).  
  
**QueryCounters** Vypíše seznam čítačů výkonu procesoru (hardware), které jsou k dispozici v počítači.  
  
 **QueryCounters** musí být jedinou možností příkazového řádku.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
VSPerfCmd.exe /QueryCounters  
```  
  
#### <a name="parameters"></a>Parametry  
 Žádné  
  
## <a name="remarks"></a>Poznámky  
 Při použití metody instrumentace profileru můžete shromažďovat hodnoty jedné nebo více čítačů výkonu procesoru na každou událost shromažďování dat. Při použití metoda profilování vzorkování, můžete zadat jeden čítače událostí a počet výskytů události má být použit jako interval vzorkování.  
  
 Různé procesory zveřejnit různé čítače výkonu procesoru. Profiler definuje sadu obecný čítače, které jde použít na téměř všechny procesory. **QueryCounters** Vypíše seznam názvů obecného čítače i názvy čítačů, které jsou specifické pro procesor.  
  
## <a name="see-also"></a>Viz také  
 [Nástroj VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profilace samostatných aplikací](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profilace webových aplikací ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profilace služeb](../profiling/command-line-profiling-of-services.md)



