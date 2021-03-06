---
title: 'Postupy: Změna možností krokování při ladění (starší verze) | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- branch stepping
- debugging, stepping options
- debugging workflows, stepping options
- stepping, changing options
- instance stepping
ms.assetid: aedc06af-d58a-44d6-aee4-f397f1f923a0
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 1fbe4ef5feeff7201a5c8772c1e754402db9ffd5
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675433"
---
# <a name="how-to-change-the-debug-stepping-option-legacy"></a>Postupy: Změna možností krokování při ladění (starší verze)
Toto téma popisuje, jak změnit krokování možnosti ladění pro [!INCLUDE[wf](../includes/wf-md.md)] aplikací ve starší [!INCLUDE[wfd1](../includes/wfd1-md.md)] , které mají souběžných akce. Použijte starší [!INCLUDE[wfd2](../includes/wfd2-md.md)] potřeba cílit na platformu [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] nebo [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Když ladíte starší aktivity, které mají souběžné spouštění, jako například **aktivitě typu ParallelActivity** nebo **aktivitou skupiny ConditionedActivityGroup**, můžete použít jednu ze dvou možností pro jednotlivé kroky v kódu.  
  
 Použijte následující postup změna ladění krokování projektu starších verzí pracovních postupů.  
  
## <a name="procedures"></a>Procedury  
  
#### <a name="to-change-the-debug-stepping-option"></a>Chcete-li změnit možnosti krokování ladění  
  
1.  Spusťte sadu Visual Studio.  
  
2.  Otevřete existující projekt starších verzí pracovních postupů nebo vytvořte nový projekt, který využívá souběžných aktivit a, který cílí na buď [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] nebo [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
3.  Na **pracovního postupu** nabídky v starší [!INCLUDE[wfd2](../includes/wfd2-md.md)], přejděte na **ladění**a pak na **možnosti krokování**.  
  
4.  Vyberte buď **Instance** nebo **větev**.  
  
## <a name="see-also"></a>Viz také  
 [Ladění starších verzí pracovních postupů](../workflow-designer/debugging-legacy-workflows.md)   
 [Možnosti krokování při ladění (starší verze)](../workflow-designer/debug-stepping-options-legacy.md)