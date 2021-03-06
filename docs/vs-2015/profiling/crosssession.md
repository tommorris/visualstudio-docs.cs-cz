---
title: CrossSession | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: b9fcb9c3-7903-478c-9b7c-dbd94092fcba
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4c4306f89b41639ba70e581ed6b3b4ce70089c01
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/05/2018
ms.locfileid: "43775920"
---
# <a name="crosssession"></a>CrossSession
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CrossSession](https://docs.microsoft.com/visualstudio/profiling/crosssession).  
  
VSPerfCmd.exe **CrossSession** možnost umožňuje profileru začnete shromažďovat data z všechny relace konzoly. **CrossSession** možnost musí být použita s **Start** možnost.  
  
 Můžete použít zkratku **CS** místo **CrossSession**.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
VSPerfCmd.exe /Start:Method /CrossSession [Options]  
```  
  
#### <a name="parameters"></a>Parametry  
 Žádné  
  
## <a name="valid-options"></a>Platné možnosti  
 Chcete-li povolit profilaci v jiné relaci **CrossSession** možnost musí být zadaný pomocí **Start** možnost. **CrossSession** musí být zadaná také v jakémkoli následné **připojit nástroj VSPerfCmd** a **odpojit** příkazy.  
  
 **Spusťte:** `Method`  
 **Start** možnost inicializuje profiler k zadané metodě profilování.  
  
 **Připojit:** _PID_[**,**_PID_]  
 Zahájení profilace konkrétních procesů.  
  
 **Odpojit**[**:**_PID_[,_PID_]]  
 Zastaví profilaci konkrétních procesů.  
  
## <a name="example"></a>Příklad  
 V tomto příkladu **CrossSession** možnost se používá k připojení k aplikaci, která byla spuštěna v jiné relaci konzoly.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /CrossSession  
VSPerfCmd.exe /Attach:12345 /CS  
```  
  
## <a name="see-also"></a>Viz také  
 [Nástroj VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profilace samostatných aplikací](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profilace webových aplikací ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profilace služeb](../profiling/command-line-profiling-of-services.md)



