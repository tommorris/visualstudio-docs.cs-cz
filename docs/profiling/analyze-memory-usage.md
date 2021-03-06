---
title: Analýza využití paměti v aplikaci Visual Studio | Dokumentace Microsoftu
ms.custom: ''
ms.date: 01/02/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3cee40dd1dab8c3a9d9b57b84e6e299651bc5fc8
ms.sourcegitcommit: db94ca7a621879f98d4c6aeefd5e27da1091a742
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2018
ms.locfileid: "42624387"
---
# <a name="analyze-memory-usage"></a>Analýza využití paměti
Použijte integrovaný ladicí program **využití paměti** diagnostický nástroj k vyhledání nevrácené paměti a využití paměti neefektivní. Umožňuje nástroj využití paměti, můžete provést jeden nebo více *snímky* spravovaný a nativní paměti haldy. Můžete shromažďovat snímky technologie .NET, nativní nebo smíšený režim (.NET a nativní) aplikace.  
  
-   Jeden snímek pochopit jeho relativní dopad typů objektů na využití paměti a vyhledání kódu vaší aplikace, která používá paměť neefektivně, můžete analyzovat.  
  
-   Můžete také porovnat (rozdíl) dvěma snímky vyhledejte oblasti v kódu aplikace, které způsobují využití paměti časem zvětšuje.  

Podrobné pokyny najdete v tématu [analýza využití paměti](../profiling/memory-usage.md) kurzu. Analýza využití paměti bez připojení ladicího programu, najdete v článku [využití paměti bez ladicího programu](memory-usage-without-debugging2.md).

Můžete použít profilovací nástroje bez ladicího programu s Windows 7 a novější. Windows 8 a novější se vyžaduje pro spuštění nástrojů pro profilaci s ladicím programem (**diagnostické nástroje** okno).
  
## <a name="blogs-and-videos"></a>Blogy a videa  

|         |         |
|---------|---------|
|  ![Ikona filmové kamery pro video](../install/media/video-icon.png "Sledovat video")  |    [Podívejte se na video](https://mva.microsoft.com/en-US/training-courses-embed/getting-started-with-visual-studio-2017-17798/Profiling-with-Diagnostics-Tools-in-Visual-Studio-2017-daHnzMD6D_9211787171) pomocí diagnostických nástrojů, které ukazuje, jak analyzovat využití paměti a využití procesoru v sadě Visual Studio 2017. |

 [Analýza využití procesoru a paměti během ladění](https://blogs.msdn.microsoft.com/visualstudio/2016/02/15/analyze-cpu-memory-while-debugging/)  
  
 [Visual C++ blog: profilace paměti v aplikaci Visual C++ 2015](https://blogs.msdn.microsoft.com/vcblog/2015/10/21/memory-profiling-in-visual-c-2015/)  

## <a name="see-also"></a>Viz také:
 [Profilace v sadě Visual Studio](../profiling/index.md)  
 [Nejdřív se podívejte na nástroje pro profilaci](../profiling/profiling-feature-tour.md)