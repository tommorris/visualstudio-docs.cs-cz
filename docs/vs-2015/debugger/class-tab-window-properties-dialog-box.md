---
title: Karta třída, dialogové okno Vlastnosti okna | Dokumentace Microsoftu
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
- Window Properties dialog box, Class Tab
ms.assetid: eaec9f07-d580-436d-934d-76c4e59439aa
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8a4be66a2eb725f2c81032b18414a2d6d624a0cf
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668191"
---
# <a name="class-tab-window-properties-dialog-box"></a>Karta Třída, dialogové okno vlastnosti okna
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [karta třída, dialogové okno Vlastnosti okna](https://docs.microsoft.com/visualstudio/debugger/class-tab-window-properties-dialog-box).  
  
Použití **třídy** karta zobrazuje informace ve třídě vybrané okno. Zobrazíte [dialogové okno Vlastnosti okna](../debugger/window-properties-dialog-box.md), přesuňte fokus [zobrazení Windows](../debugger/windows-view.md) okna. Vyberte jakékoli okno uzel ve stromu a pak zvolte **vlastnosti** z **zobrazení** nabídky.  
  
 Následující nastavení jsou k dispozici na **třídy** kartu:  
  
|Položka|Popis|  
|-----------|-----------------|  
|**Název třídy**|Název (nebo ordinální číslo) této třídy okna.|  
|**Styly třídy**|Kombinace stylu kódů třídy.|  
|**Bajty třídy**|Specifické pro aplikaci data přidružená k této třídy okna.|  
|**Formát Atom třídy**|Atom pro třídu vrácené **RegisterClass** volání.|  
|**Popisovač instance**|Popisovač instance modulu, který registrované třídy. Instance popisovače nejsou jedinečné.|  
|**Bajty okna**|Počet bajtů navíc spojené s každou okno této třídy. Význam těchto bajtů se určuje podle aplikace. Rozbalte položku seznamu zobrazíte bajtové hodnoty ve formátu DWORD.|  
|**Proces okna**|Aktuální adresu **WndProc** funkce pro windows z této třídy. Tím se liší od **proces okna** na **Obecné** kartě Pokud rozčlenění okna.|  
|**Název nabídky**|Název hlavní nabídky, která souvisí s windows z této třídy ("none" Pokud neexistuje žádná nabídka).|  
|**Popisovač ikony**|Popisovač ikony, která souvisí s windows z této třídy ("none" Pokud neexistuje žádná ikona).|  
|**Popisovač ukazatele**|Popisovač pro kurzor, který je přidružený k windows této třídy ("none" Pokud neexistuje žádný kurzor).|  
|**Štětec pozadí**|Popisovač pro štětec pozadí, která souvisí s windows z této třídy, nebo jednu z předdefinovaných COLOR_ * barev pro vykreslování pozadí okna ("none" Pokud neexistuje žádný štětec).|



