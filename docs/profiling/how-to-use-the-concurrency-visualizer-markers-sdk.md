---
title: "Postupy: Použití SDK značek Vizualizéru souběžnosti | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 19a45032-f8a7-4137-890e-2ceeec938b8d
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: eacea655fe24b497b6bf9caa699e03cac99103d8
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-use-the-concurrency-visualizer-markers-sdk"></a>Postupy: Použití SDK značek Vizualizéru souběžnosti
Toto téma ukazuje, jak se používat sadu SDK Vizualizéru souběžnosti vytvořit rozsahy a zapsat příznaky, zprávy a upozornění.  
  
### <a name="to-use-c"></a>Chcete-li použít C++  
  
1.  SDK Vizualizéru souběžnosti podporu přidáte do vaší aplikace. Další informace najdete v tématu [SDK Vizualizéru souběžnosti](../profiling/concurrency-visualizer-sdk.md).  
  
2.  Přidat `include` příkaz a `using` příkazu pro sadu SDK.  
  
    ```C++  
  
    #include <cvmarkersobj.h>  
    using namespace Concurrency::diagnostic;  
  
    ```  
  
3.  Přidejte kód k vytvoření tři rozsahy v řadě výchozí značky a zápis příznak, zprávu a výstrahu, jednu pro každý rozpětí. Metody k zápisu příznaky, zprávy a upozornění jsou členy [marker_series](../profiling/marker-series-class.md) třídy. V konstruktoru pro [span](../profiling/span-class.md) vyžaduje třídy `marker_series` objektu, tak, aby každý rozpětí je přidružen konkrétní značky řady. A `span` skončí, když je odstraněn.  
  
    ```C++  
  
    marker_series series;  
    span *flagSpan = new span(series, 1, _T("flag span"));  
    series.write_flag(_T("Here is the flag."));  
    delete flagSpan;  
  
    span *messageSpan = new span(series, 2, _T("message span"));  
    series.write_flag(_T("Here is the message."));  
    delete messageSpan;  
  
    span *alertSpan = new span(series, 3, _T("alert span"));  
    series.write_flag(_T("Here is the alert."));  
    delete alertSpan;  
  
    ```  
  
4.  Na řádku nabídek zvolte **analyzovat**, **vizualizér souběžnosti**, **začínat aktuálního projektu** spusťte aplikaci a zobrazte vizualizér souběžnosti. Následující obrázek znázorňuje tři rozsahy a tři značek v vizualizér souběžnosti.  
  
     ![Vizualizér souběžnosti se 3 značkami a výstrahy](../profiling/media/cvmarkersnative.png "CvMarkersNative")  
  
5.  Přidejte kód k vytvoření další, vlastní značky řady voláním v konstruktoru pro `marker_series` která přijímá řetězcový název řady, značky.  
  
    ```C++  
  
    marker_series flagSeries(_T("flag series"));  
    span *flagSeriesSpan = new span(flagSeries, 1, _T("flag span"));  
    flagSeries.write_flag(1, _T("flag"));  
    // Sleep to even out the display in the Concurrency Visualizer.  
    Sleep(50);  
    delete flagSeriesSpan;  
  
    marker_series messageSeries(_T("message series"));  
    span *messageSeriesSpan = new span(messageSeries, 1, _T("message span"));  
    messageSeries.write_message(1, _T("message"));  
    // Sleep to even out the display in the Concurrency Visualizer.  
    Sleep(50);  
    delete messageSeriesSpan;  
  
    ```  
  
6.  Spusťte v aktuálním projektu zobrazíte vizualizér souběžnosti. Řada dvě značky se zobrazí v vlastní dráhy v zobrazení vláken. Následující obrázek znázorňuje dva nové rozsahy.  
  
     ![Vizualizér souběžnosti 3 řady vlastní značky](../profiling/media/cvmarkerseriesnative.png "CvMarkerSeriesNative")  
  
### <a name="to-use-visual-basic-or-c"></a>Chcete-li použít Visual Basic a C# #
  
1.  SDK Vizualizéru souběžnosti podporu přidáte do vaší aplikace. Další informace najdete v tématu [SDK Vizualizéru souběžnosti](../profiling/concurrency-visualizer-sdk.md).  
  
2.  Přidat `using` nebo `Imports` příkazu pro sadu SDK.  
  
    ```VB  
    Imports Microsoft.ConcurrencyVisualizer.Instrumentation  
  
    ```  
  
    ```CSharp  
    using Microsoft.ConcurrencyVisualizer.Instrumentation;  
    ```  
  
3.  Přidejte kód a vytvořte tři rozsahy na výchozí značky řadu, zápis příznak, zprávu a výstrahu, jednu pro každý rozpětí. Vytváření <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.Span> objekt voláním statické `EnterSpan` metoda. Zapsat do výchozí řadu, používáte metody statické zápisu <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.Markers> třídy.  
  
    ```VB  
  
    Dim flagSpan As Span = Markers.EnterSpan("flag span")  
    Markers.WriteFlag("Here is the flag.")  
    flagSpan.Leave()  
  
    Dim messageSpan As Span = Markers.EnterSpan("message span")  
    ' Sleep for a millisecond to even out the display in the Concurrency Visualizer.  
    System.Threading.Thread.Sleep(1)  
    Markers.WriteMessage("Here is a message")  
    messageSpan.Leave()  
  
    Dim alertSpan As Span = Markers.EnterSpan("alert span")  
    ' Sleep for a millisecond to even out the display in the Concurrency Visualizer.  
    System.Threading.Thread.Sleep(1)  
    Markers.WriteAlert("Here is an alert")  
    alertSpan.Leave()  
  
    ```  
  
    ```CSharp  
  
    Span flagSpan = Markers.EnterSpan("flag span");  
    Markers.WriteFlag("Here is the flag.");  
    flagSpan.Leave();  
  
    Span messageSpan = Markers.EnterSpan("message span");  
    // Sleep for a millisecond to even out the display in the Concurrency Visualizer.  
    System.Threading.Thread.Sleep(1);  
    Markers.WriteMessage("Here is a message");  
    messageSpan.Leave();  
  
    Span alertSpan = Markers.EnterSpan("alert span");  
    // Sleep for a millisecond to even out the display in the Concurrency Visualizer.  
    System.Threading.Thread.Sleep(1);  
    Markers.WriteAlert("Here is an alert");  
    alertSpan.Leave();  
    ```  
  
4.  Na řádku nabídek zvolte **analyzovat**, **vizualizér souběžnosti**, **začínat aktuálního projektu** spusťte aplikaci a zobrazte vizualizér souběžnosti. Následující obrázek znázorňuje tři rozsahy a tři značek v zobrazení vláken vizualizér souběžnosti.  
  
     ![Vizualizér souběžnosti se značkami a výstrahy](../profiling/media/cvmarkersmanaged.png "CvMarkersManaged")  
  
5.  Přidejte kód k vytvoření značky řadu zákazníků pomocí statické <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.Markers.CreateMarkerSeries%2A> metoda. <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.MarkerSeries> Třída obsahuje metody pro vytváření rozsahy a zápis příznaky, zprávy a upozornění.  
  
    ```VB  
  
    Dim flagSeries As MarkerSeries = Markers.DefaultWriter.CreateMarkerSeries("flag series")  
    Dim flagSeriesSpan As Span = flagSeries.EnterSpan("flag span")  
    System.Threading.Thread.Sleep(1)  
    flagSeries.WriteFlag(1, "flag")  
    System.Threading.Thread.Sleep(1)  
    flagSeriesSpan.Leave()  
  
    Dim messageSeries As MarkerSeries = Markers.DefaultWriter.CreateMarkerSeries("message series")  
    Dim messageSeriesSpan As Span = messageSeries.EnterSpan("message span")  
    messageSeries.WriteMessage("message")  
    System.Threading.Thread.Sleep(1)  
    messageSeriesSpan.Leave()  
    ```  
  
    ```CSharp  
  
    MarkerSeries flagSeries = Markers.DefaultWriter.CreateMarkerSeries("flag series");  
    Span flagSeriesSpan = flagSeries.EnterSpan("flag span");  
    System.Threading.Thread.Sleep(1);  
    flagSeries.WriteFlag(1, "flag");  
    System.Threading.Thread.Sleep(1);  
    flagSeriesSpan.Leave();  
  
    MarkerSeries messageSeries = Markers.DefaultWriter.CreateMarkerSeries("message series");  
    Span messageSeriesSpan = messageSeries.EnterSpan("message span");  
    messageSeries.WriteMessage("message");  
    System.Threading.Thread.Sleep(1);  
    messageSeriesSpan.Leave();  
    ```  
  
6.  Spusťte v aktuálním projektu zobrazíte vizualizér souběžnosti. Řada tři značky se zobrazí v vlastní dráhy v zobrazení vláken. Následující obrázek znázorňuje tři nové rozpětí.  
  
     ![Vizualizér souběžnosti 3 řady vlastní značky](../profiling/media/cvmarkerseriesmanaged.png "CvMarkerSeriesManaged")  
  
## <a name="see-also"></a>Viz také  
 [SDK Vizualizéru souběžnosti](../profiling/concurrency-visualizer-sdk.md)