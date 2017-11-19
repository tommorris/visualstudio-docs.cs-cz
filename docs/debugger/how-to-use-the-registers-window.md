---
title: "Zobrazení hodnot registru v ladicím programu sady Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.registers
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- registers, debugging
- register contents
- flags, Registers window
- register groups
- debugging [Visual Studio], Registers window
- Registers window
ms.assetid: 2918ffa2-562f-40d6-9053-ef321bbeb767
caps.latest.revision: "37"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1cff6db85b29b4db6006d37fd21e2d9b109b099e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="view-register-values-and-use-the-registers-window-in-the-visual-studio-debugger"></a>Zobrazení hodnoty zaregistrovat a použití okna zaregistruje v ladicím programu Visual Studio
Okna registry je k dispozici pouze v případě, že je povoleno ladění úrovni adresu v **možnosti** dialogové okno, **ladění** uzlu **Obecné** kategorie.  
  
 **Zaregistruje** zobrazí okno obsah registru. Pokud necháte **zaregistruje** okno otevřít v průběhu vašeho programu, můžete zobrazit registrace změní hodnoty jako kód spustí. Hodnoty, které se změnily nedávno se zobrazí červeně. Můžete upravit hodnot registru. Další informace najdete v tématu [postupy: Úprava hodnoty zaregistrovat](../debugger/how-to-edit-a-register-value.md).  
  
 Pro lepší přehlednost, **zaregistruje** okno uspořádá zaregistruje do skupin, které se liší podle platformy a procesoru typu. Můžete zobrazit nebo skrýt skupiny tak, jak chcete. Další informace najdete v tématu [postupy: zobrazení a skrytí registrovat skupiny](../debugger/how-to-display-and-hide-register-groups.md).  
  
 Podrobný úvod do koncepty za registry a okno registrů, najdete v části [základní informace o ladění: okno zaregistruje](../debugger/debugging-basics-registers-window.md).  
  
> [!NOTE]
>  Dialogová okna a příkazy nabídek, které vidíte, se mohou lišit od těch popsaných v nápovědě v závislosti na aktivních nastaveních nebo edici. Chcete-li změnit nastavení, zvolte **nastavení importu a exportu** na **nástroje** nabídky. Další informace najdete v tématu [přizpůsobení prostředí Visual Studio IDE](../ide/personalizing-the-visual-studio-ide.md).  
  
### <a name="to-display-the-registers-window"></a>Pro zobrazení okna registry  
  
-   Na **ladění** nabídce zvolte **Windows**a potom zvolte **zaregistruje**.  
  
     Ladicí program musí být spuštěna, nebo v režimu pozastavení.  
  
    > [!NOTE]
    >  Informace o registraci není k dispozici pro skript nebo aplikace SQL.  
  
## <a name="see-also"></a>Viz také  
 [Základní informace k ladění: Okno registrů](../debugger/debugging-basics-registers-window.md)   
 [Zobrazení dat v ladicím programu](../debugger/viewing-data-in-the-debugger.md)   
 [Základní informace k ladění: Okno registrů](../debugger/debugging-basics-registers-window.md)