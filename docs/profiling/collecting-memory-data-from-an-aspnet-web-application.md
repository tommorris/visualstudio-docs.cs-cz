---
title: Shromažďování dat paměti z webové aplikace ASP.NET pomocí příkazového řádku profileru | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- profiling tools,.NET memory method
ms.assetid: 57acf2b0-327a-4c0e-8078-ac2f6d99457d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- aspnet
ms.openlocfilehash: 161f96c38a12de1f29a0f4ebd5d3779f31cf8f23
ms.sourcegitcommit: 046a9adc5fa6d6d05157204f5fd1a291d89760b7
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2018
---
# <a name="collecting-memory-data-from-an-aspnet-web-application-by-using-the-profiler-command-line"></a>Shromažďování dat paměti z webové aplikace ASP.NET pomocí příkazového řádku profileru
Tato část popisuje postupy a možnosti pro shromažďování paměti přidělení a objekt dat doba platnosti pro webovou aplikaci ASP.NET pomocí **VSPerfCmd** nástroj příkazového řádku.  
  
> [!NOTE]
>  **VSPerfCmd** nástroj vám poskytne úplný přístup k nástrojích pro profilaci funkcí, včetně pozastavení a obnovení profilování a získání dalších dat z procesoru a čítačů výkonu systému Windows. Můžete také **VSPerfASPNETCmd** nástroj příkazového řádku, pokud není nutné tuto funkci. Ve srovnání s [VSPerfCmd](../profiling/vsperfcmd.md) žádné proměnné prostředí je nutné nastavit nástroj pro příkazový řádek, a není vyžadováno restartování počítače. Další informace najdete v tématu [rychlé profilace webu pomocí VSPerfASPNETCmd](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md).  
  
## <a name="common-tasks"></a>Obecné úlohy  
  
|Úloha|Související obsah|  
|----------|---------------------|  
|**Připojení profileru k spuštěné aplikace ASP.NET**|-   [Postupy: připojení profileru k webové aplikaci ASP.NET ke shromažďování dat paměti](../profiling/how-to-attach-the-profiler-to-an-aspnet-web-application-to-collect-memory-data-by-using-the-command-line.md)|  
|**Binární soubory nástroje staticky kompilované**|-   [Postupy: instrumentace staticky kompilované aplikace ASP.NET a shromažďování dat paměti](../profiling/how-to-instrument-a-statically-compiled-aspnet-web-application-and-collect-memory-data-by-using-the-profiler-command-line.md)|  
|**Binární soubory nástroje dynamicky kompilovat**|-   [Postupy: instrumentace dynamicky kompilované aplikace ASP.NET a shromažďování dat paměti](../profiling/how-to-instrument-a-dynamically-compiled-aspnet-web-application-and-collect-memory-data.md)|  
  
## <a name="related-tasks"></a>Související úlohy  
  
### <a name="profiling-aspnet-web-applications"></a>Profilace webových aplikací ASP.NET  
  
|Úloha|Související obsah|  
|----------|---------------------|  
|**Profilu pomocí metody vzorkování**|-   [Shromažďování statistik aplikace pomocí vzorkování](../profiling/collecting-application-statistics-for-aspnet-using-the-profiler-sampling-method.md)|  
|**Profilu pomocí metody instrumentace**|-   [Shromažďování podrobných dat časování pomocí instrumentace](../profiling/collecting-detailed-timing-data-aspnet-profiler-instrumentation-method.md)|  
|**Profil aktivita prostředku kolizí a přístup z více vláken**|-   [Shromažďování dat souběžnosti](../profiling/collecting-concurrency-data-for-an-aspnet-web-application.md)|  
  
### <a name="profiling-net-framework-memory-data"></a>Profilace dat paměti .NET Framework  
  
|Úloha|Související obsah|  
|----------|---------------------|  
|**Profil aplikace samostatné (klient)**|-   [Shromažďování dat paměti .NET Framework](../profiling/collecting-dotnet-framework-memory-data-for-stand-alone-applications.md)|  
|**Profil služby**|-   [Shromažďování dat paměti .NET](../profiling/collecting-memory-data-from-dotnet-framework-services-by-using-the-profiler-command-line.md)|  
  
### <a name="analyzing-net-memory-data-views-and-reports"></a>Analýza dat paměti .NET zobrazeních a sestavách  
 [Zobrazení dat paměti .NET](../profiling/dotnet-memory-data-views.md)  
  
## <a name="reference"></a>Odkaz  
 [Profilování nástroje pro příkazový řádek](../profiling/command-line-profiling-tools-reference.md)