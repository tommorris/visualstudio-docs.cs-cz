---
title: "Čas synchronizace | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.cv.threads.timeline.synchronization
helpviewer_keywords: Concurrency Visualizer, Synchronization Time
ms.assetid: affa04cc-8bba-4848-9301-b19846d3c2cb
caps.latest.revision: "6"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c6f792e58a2c98219d15e889846921f537d74140
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="synchronization-time"></a>Čas synchronizace
Tyto segmenty v časové ose jsou přidruženy k blokování pokusů, které jsou klasifikovány jako synchronizace. Když vlákno je označený jako blokované při synchronizaci, je implicitní jednu z těchto věcí:  
  
-   Spuštění podprocesu bylo pravděpodobně způsobeno v volání synchronizace dobře známé vláken rozhraní API, jako `EnterCriticalSection()` nebo `WaitForSingleObject()`.  
  
-   Algoritmus odpovídající rozhraní API nemůže být zcela komplexní, a proto některé rozhraní API, který může být namapovaný na ostatních kategorií může také zobrazit jako synchronizace, protože rámce ve volání zásobníku nakonec dosažen základní jádra blokování primitivní, který byl mapovat na tuto kategorii.  
  
 Abyste pochopili základní příčinu události blokující přístup z více vláken, pečlivě zkontrolujte blokování zásobníky volání a profilu, sestavy.  
  
## <a name="see-also"></a>Viz také  
 [Zobrazení vláken](../profiling/threads-view-parallel-performance.md)