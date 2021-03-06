---
title: 'Postupy: přepnutí na jiné vlákno během ladění | Microsoft Docs'
ms.custom: ''
ms.date: 04/27/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- threads, switching [debugging]
ms.assetid: 5cd76c52-76fa-4fcc-b37e-e9f0ecac0e9e
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e7e5e3b127dd397a32b54915f95827ebe5649f5f
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2018
ms.locfileid: "31475678"
---
# <a name="how-to-switch-to-another-thread-while-debugging-in-visual-studio"></a>Postupy: přepnutí na jiné vlákno během ladění v sadě Visual Studio
Při ladění vícevláknové aplikace, můžete přejít z vlákno, které pracujete s na jiné vlákno jedné z několika metod.

> [!NOTE]
> Pokud chcete určit pořadí, ve kterém vláken spuštění, budete muset [ukotvení a odblokování vláken](../debugger/get-started-debugging-multithreaded-apps.md).

Při kontrole vláken v editoru kódu a jiné vícevláknové ladění windows žlutá šipka označuje aktuální vlákno. Zelenou šipku s složené tail znamená, že má jiný aktuální vlákno aktuálního kontextu ladicího programu.
  
### <a name="to-switch-to-any-thread-that-appears"></a>Přejděte na všechny vlákno, které se zobrazí 
  
-   V **vláken** nebo **paralelního sledování** okna, klikněte dvakrát na vlákno.  
  
### <a name="to-switch-to-a-thread-in-a-source-window"></a>Chcete-li přepnout na vlákno v okně zdroje  
  
-   V levém oddělovací mezery, klikněte pravým tlačítkem myši ikonu značky vlákno ![vlákno značky](../debugger/media/dbg-thread-marker.png "ThreadMarker"), přejděte na příkaz **přepnout**a pak klikněte na název daném vláknu, ke kterému chcete přejít . Místní nabídky zobrazuje pouze vláken v tomto konkrétní umístění.  
  
     Pokud žádný přístup z více vláken značky se zobrazí, klikněte pravým tlačítkem myši **vláken** okna a ověřte, že **zobrazit vláken ve zdroji** je vybrána.  
  
### <a name="to-switch-to-a-thread-in-the-debug-location-toolbar"></a>Chcete-li přepnout na vlákno v panelu nástrojů ladění umístění  
  
1.  Na **ladění umístění** nástrojů, klikněte na tlačítko **vláken** seznamu.  
  
2.  V seznamu klikněte na vlákno, ke kterému chcete přejít.  
  
## <a name="see-also"></a>Viz také  
 [Ladění vícevláknových aplikací](../debugger/debug-multithreaded-applications-in-visual-studio.md)
