---
title: Karta Obecné, dialogové okno Vlastnosti okna | Dokumentace Microsoftu
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
- Window Properties dialog box, General Tab
ms.assetid: 19142c60-9b32-46ba-a556-b62fd77568c1
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d699bda033a01e622925261bfa8455cae6f0f73a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666809"
---
# <a name="general-tab-window-properties-dialog-box"></a>Karta Obecné, dialogové okno vlastnosti okna
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [karta Obecné, dialogové okno Vlastnosti okna](https://docs.microsoft.com/visualstudio/debugger/general-tab-window-properties-dialog-box).  
  
Použití **Obecné** zobrazte informace o vybrané okno. Zobrazíte [dialogové okno Vlastnosti okna](../debugger/window-properties-dialog-box.md), přesuňte fokus [zobrazení Windows](../debugger/windows-view.md) okna. Vyberte jakékoli okno uzel ve stromu a pak zvolte **vlastnosti** z **zobrazení** nabídky.  
  
 Následující nastavení jsou k dispozici na **Obecné** kartu:  
  
|Položka|Popis|  
|-----------|-----------------|  
|**Titulek okna**|Text v záhlaví okna, nebo text obsažen v okně, pokud je ovládací prvek.|  
|**Popisovač okna**|Jedinečné ID tohoto okna. Jsou opakovaně využívána popisovač okna; okno identifikují pouze po dobu platnosti tohoto okna.|  
|**Proces okna**|Virtuální adresa funkce procedury okna pro toto okno. Toto pole také určuje, zda toto okno je okno Unicode, a určuje, zda je rozčleněných do podtříd.|  
|**Obdélník**|Ohraničující obdélník okna. Zobrazí se také velikost pravoúhelníku. Jednotky jsou pixelů v souřadnicovém systému obrazovky.|  
|**Obnovený Rect**|Ohraničující obdélník obnovené okna. Zobrazí se také velikost pravoúhelníku. Obnovený Rect budou lišit od obdélník pouze v případě, že je okno maximalizované ani minimalizováno. Jednotky jsou pixelů v souřadnicovém systému obrazovky.|  
|**Rect klienta**|Ohraničující rámeček pro klientské oblasti okna. Zobrazí se také velikost pravoúhelníku. Jednotky jsou relativní k levé horní části klientské oblasti okna pixelů.|  
|**Popisovač instance**|Popisovač instance aplikace. Instance popisovače nejsou jedinečné.|  
|**ID ovládacího prvku nebo popisovač nabídky**|Pokud okno zobrazení je podřízené okno, zobrazí se ID ovládacího prvku popisku. ID ovládacího prvku je celé číslo, které identifikuje ID této podřízené okno ovládacího prvku. Pokud není okno se zobrazí podřízené okno, zobrazí se popisek nabídky zpracování. Popisovač nabídky je celé číslo, které identifikuje popisovač nabídky spojené s tímto oknem.|  
|**Uživatelská Data**|Specifické pro aplikaci data, která je přiřazena tato struktura okna.|  
|**Bajty okna**|Počet bajtů navíc spojený s tímto oknem. Význam těchto bajtů se určuje podle aplikace. Rozbalte položku seznamu zobrazíte bajtové hodnoty ve formátu DWORD.|



