---
title: Sys (VSPerfCmd) | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 294a6f9e-b49f-4c83-b322-5ac5411b66fb
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fb87886e4b40643a23e661294c6fcf0a2a74332b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669828"
---
# <a name="sys-vsperfcmd"></a>Sys (VSPerfCmd)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [Sys (VSPerfCmd)](https://docs.microsoft.com/visualstudio/profiling/sys-vsperfcmd).  
  
VSPerfCmd.exe **Sys** možnost nastaví profilování události, ke které se definuje tak do systémových volání událostí (volání funkcí v profilované aplikace v operačním systému) a volitelně změny číslo systému volá v vzorkování Interval z výchozí hodnoty 10.  
  
 **Sys** jde použít jenom v příkazovém řádku, který také obsahuje **spuštění** nebo **připojit** možnost.  
  
 Ve výchozím nastavení událost odběru vzorků profiler je nastavena na hodinových cyklů procesoru a interval vzorkování je nastavený na 10 000 000. **Časovače**, **PF**, **Sys**, a **čítač** možnosti umožňují nastavit událost odběru vzorků a interval odběru vzorků. **GC** možnost shromažďuje data paměti .NET v každé události přidělování a uvolňování paměti kolekce. Na příkazovém řádku lze zadat pouze jeden z těchto možností.  
  
 Událost odběru vzorků a interval vzorkování je možné nastavit pouze v první příkazového řádku, který obsahuje **spuštění** nebo **připojit** možnost.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
VSPerfCmd.exe {/Launch:AppName|Attach:PID} /Sys[:Events] [Options]  
```  
  
#### <a name="parameters"></a>Parametry  
 `Events`  
 Celočíselná hodnota, která určuje počet systému volání události v intervalu vzorkování. Pokud `Events` není zadán, je nastavit interval na 10.  
  
## <a name="required-options"></a>Požadované možnosti  
 **Sys** vyžaduje jednu z následujících možností.  
  
 **Spuštění:** `AppName`  
 Spuštění profileru a aplikace určené `AppName`.  
  
 **Připojení:** `PID`  
 Připojí profiler k procesu určené `PID`.  
  
## <a name="invalid-options"></a>Neplatné možnosti  
 Tyto možnosti nelze zadat na stejném příkazovém řádku jako **Sys**.  
  
 **PF**[**:**`Events`]  
 Nastaví událost odběru vzorků na chyby stránek a volitelně nastaví interval vzorkování na `Events`. Výchozí interval PF je 10.  
  
 **Časovač**[**:**`Cycles`]  
 Nastaví událost odběru vzorků na hodin procesoru cykly a volitelně nastaví interval vzorkování na `Cycles`. Výchozí interval časovače je 10 000 000.  
  
 **Čítač:** `Name`[`,Reload`[`,FriendlyName`]]  
 Nastaví událost odběru vzorků na výkon procesoru čítač určené `Name` a nastaví interval vzorkování na `Reload`.  
  
 **Uvolňování paměti**[**:**{**přidělení**&#124;**životnost**}]  
 Shromažďuje data paměti .NET. Ve výchozím nastavení (**přidělení**), data se shromažďují v každé události přidělení paměti. Když **životnost** parametr zadán, data se shromažďují také na všechny události uvolňování paměti kolekce.  
  
## <a name="example"></a>Příklad  
 Tento příklad ukazuje, jak nastavit profiler událost odběru vzorků na volání systému a jak nastavit interval vzorkování na 20 volání na vzorek.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /Sys:20  
```  
  
## <a name="see-also"></a>Viz také  
 [Nástroj VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profilace samostatných aplikací](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profilace webových aplikací ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profilace služeb](../profiling/command-line-profiling-of-services.md)



