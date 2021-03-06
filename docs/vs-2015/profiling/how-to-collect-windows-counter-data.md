---
title: 'Postupy: shromažďování dat čítačů Windows | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.property.syscounter
- vs.performance.property.wincounter
helpviewer_keywords:
- windows counters
- performance tools, using windows counters
- profiling tools, using windows counters
ms.assetid: db4fbac2-bea5-4558-aa8b-160fcccf4b33
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7f0ace1d920cdd4f2c503c608a1695b04c1251f2
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42671672"
---
# <a name="how-to-collect-windows-counter-data"></a>Postupy: Shromažďování dat čítačů Windows
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: shromažďování dat čítačů Windows](https://docs.microsoft.com/visualstudio/profiling/how-to-collect-windows-counter-data).  
  
Čítače Windows jsou systémové čítače výkonu, které mohou být shromážděných během profilace v nastavených intervalech. V zobrazení sestav nástrojů pro profilaci sady značek je označen řádek **AutoMark** pro každý interval shromažďování. Tento řádek obsahuje sloupce, které popisují hodnoty čítače výkonu v tomto intervalu. Chcete-li omezit analýzu na určitou dobu mezi dvěma konkrétními značkami, vyberte značky, klikněte pravým tlačítkem a pak vyberte **filtrovat podle** ->  **značky** z místní nabídky.  
  
 **Požadavky**  
  
-   [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
> [!NOTE]
>  Rozšířené funkce zabezpečení v systému Windows 8 a Windows Server 2012 vyžadují významné změny ve způsobu, jakým profiler systému Visual Studio na těchto platformách shromažďuje data. Aplikace Windows Store také vyžadují nové techniky kolekce. Zobrazit [nástroje pro výkon v aplikacích Windows 8 a Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
### <a name="to-collect-windows-counter-data"></a>Ke shromažďování dat čítačů Windows  
  
1.  V prohlížeči výkonu, klikněte pravým tlačítkem na relaci, pro kterou chcete konfigurovat čítače Windows a vyberte **vlastnosti**.  
  
2.  V **stránky vlastností**, klikněte na tlačítko **čítače Windows**.  
  
3.  Vyberte **shromáždit čítače Windows** zaškrtávací políčko.  
  
4.  V **intervalem sběru hodnot (MS)** textové pole, zadejte časový interval.  
  
5.  Vybrat kategorii z **kategorie čítače** rozevíracího seznamu.  
  
6.  Vyberte instanci, ze **Instance** rozevíracího seznamu.  
  
7.  Vyberte čítače, které chcete použít při profilování aplikace.  
  
8.  Klikněte na tlačítko **použít.**  
  
## <a name="see-also"></a>Viz také  
 [Konfigurace výkonnostních relací](../profiling/configuring-performance-sessions.md)   
 [Vlastnosti výkonnostní relace](../profiling/performance-session-properties.md)   
 [Využití procesoru a čítače Windows](../profiling/cpu-and-windows-counters.md)



