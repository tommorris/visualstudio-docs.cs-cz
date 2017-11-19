---
title: "Karta prostor, dialogové okno Vlastnosti procesu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Process properties for Windows NT
ms.assetid: c4de1866-7447-48f7-aa88-28ad92c0b930
caps.latest.revision: "4"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a70f9805f0868c7afec70fdda26ff97766281d9a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="space-tab-process-properties-dialog-box"></a>Karta Prostor, dialogové okno vlastností procesu
Použití **místo** kartě prozkoumat adresní prostor procesu. Chcete-li zobrazit [dialogové okno Vlastnosti procesu](../debugger/process-properties-dialog-box.md), přesunout fokus na [zobrazení procesů](../debugger/processes-view.md) okno. Vyberte libovolný uzel procesu ve stromové struktuře, a potom vyberte **vlastnosti** z **zobrazení** nabídky.  
  
 Následující nastavení jsou k dispozici na **místo** karta:  
  
|Položka|Popis|  
|-----------|-----------------|  
|**Zobrazit místo označen jako**|Pomocí tohoto rozevíracího seznamu vyberte kategorii místa (bitové kopie, namapovaný, vyhrazena nebo nepřiřazené).|  
|**Spustitelný soubor bajtů**|Pro vybranou kategorii součet všech adresního prostoru, který tento proces používá. Spustitelný soubor paměti je paměť, která mohou být provedeny programy, ale nemusí číst nebo zapisovat.|  
|**Exec – jen pro čtení bajtů**|Pro vybranou kategorii součet všech adresní prostor, používá se jen pro čtení vlastnosti, které tento proces používá. Exec – jen pro čtení paměti je paměť, která může být proveden, stejně jako číst.|  
|**Exec – pro čtení a zápis bajtů**|Pro vybranou kategorii součet všech adresní prostor používán s vlastnostmi pro čtení a zápis, které tento proces používá. Exec – pro čtení a zápis paměť je paměti, který lze programy a také lze číst a upravovat.|  
|**Exec zápisu kopírování bajtů**|Pro vybranou kategorii součet všech adresního prostoru, který může programy a také lze číst a zapisovat. Tento typ ochrany se používá, když paměti musí být sdílen mezi procesy. Pokud sdílení procesy pouze pro čtení paměti, pak budou používat stejnou paměť. Pokud sdílející proces vyžaduje přístup pro zápis, budou pro proces provedené kopie tuto paměť.|  
|**Žádný přístup bajtů**|Pro vybranou kategorii součet všech adresního prostoru, který brání jeho použití procesu. Narušení přístupu se generuje, pokud je zápis nebo dojde k pokusu o čtení.|  
|**Jen pro čtení bajtů**|Pro vybranou kategorii součet všech adresního prostoru, který může být proveden, stejně jako číst.|  
|**Bajty čtení a zápis**|Pro vybranou kategorii součet všech adresní prostor, který umožňuje čtení a zápis.|  
|**Kopie zápis bajtů**|Pro vybranou kategorii součet všech adresní prostor, který umožňuje sdílení paměti pro čtení, ale ne pro zápis. Pokud procesy čtou tuto paměť, můžou sdílet stejnou paměť. Ale při sdílení proces chce mít přístup pro čtení a zápis do této sdílené paměti, je vytvořena kopii tohoto paměti pro zápis.|