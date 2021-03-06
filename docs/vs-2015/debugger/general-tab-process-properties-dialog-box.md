---
title: Karta Obecné, dialogové okno vlastností procesů | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: 86f4d61d-a594-4aac-8960-c5279b4a10fd
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5043d5250c6ce26807379d6cef25077480dbc344
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42676262"
---
# <a name="general-tab-process-properties-dialog-box"></a>Karta Obecné, dialogové okno vlastností procesu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [karta Obecné, dialogové okno vlastností procesu](https://docs.microsoft.com/visualstudio/debugger/general-tab-process-properties-dialog-box).  
  
Použití **Obecné** karta Další informace o konkrétní proces. Pro zobrazení [dialogové okno vlastností procesu](../debugger/process-properties-dialog-box.md), přesunout fokus [zobrazení procesů](../debugger/processes-view.md) okno. Vyberte libovolný uzel procesu ve stromové struktuře a pak zvolte **vlastnosti** z **zobrazení** nabídky.  
  
 Následující nastavení jsou k dispozici na **Obecné** kartu:  
  
|Položka|Popis|  
|-----------|-----------------|  
|**Název modulu**|Název modulu.|  
|**ID procesu**|Jedinečný Identifikátor tohoto procesu. Čísla ID procesu jsou opakovaně využívána, takže identifikují proces pouze po dobu životnosti procesu. Typ objektu procesu se vytvoří při spuštění programu. Všechna vlákna v procesu sdílet stejnou adresní prostor a mají přístup ke stejným datům.|  
|**Základní priorita**|Aktuální základní priorita tohoto procesu. Vlákna v rámci procesu můžete zvýšit a snížit své vlastní základní priorita relativní k základní priorita procesu.|  
|**Vlákna**|Počet vláken, které jsou aktuálně aktivní v tomto procesu.|  
|**Čas procesoru**|Celkový Procesorový čas strávený na tento proces a jeho vlákna. Rovno uživatelský čas plus privilegovaného času.|  
|**Čas uživatele**|Kumulativní uplynulý čas, který tento proces vláken mít stráví prováděním kódu v uživatelském režimu v jiných než nečinných vláken. Aplikace jsou spouštěny v uživatelském režimu, stejně jako podsystémy, jako je například Správce oken a stroj grafiky.|  
|**Privilegovaného času**|Celkový uplynulý čas tento proces běžel v privilegovaném režimu v jiných než nečinných vláken. Vrstva služby, rutin výkonný a jádro spustit v privilegovaném režimu. Ovladače zařízení u většiny zařízení než grafických adaptérů a tiskárny také spustit v privilegovaném režimu. Nějakou práci, která provádí Windows pro vaši aplikaci může objevit v jiných procesech subsystému kromě privilegovaného času.|  
|**Uplynulý čas**|Celkový uplynulý čas, který tento proces běžel.|



