---
title: "Ladění pracovních starší | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- workflows, debugging
- debugging, workflows
- debugging workflows
ms.assetid: e6097b47-760a-4b30-a92c-ae70cdbda49f
caps.latest.revision: "8"
author: ErikRe
ms.author: erikre
manager: erikre
ms.openlocfilehash: 2253eb414e58d5168cf6e1d2f4c22880d18d1bd6
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="debugging-legacy-workflows"></a>Ladění pracovních starší verze
Pokud používáte starší verze [!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)] v [!INCLUDE[vs_current_long](../misc/includes/vs_current_long_md.md)] k sestavení [!INCLUDE[wf](../workflow-designer/includes/wf_md.md)] aplikace, aby target.NET Framework 3.0 nebo 3.5, můžete ladit vaše pracovní postupy jako libovolné jiné programy nastavení zarážek, připojení k procesům a prozkoumání vláken a Zásobník volání. Máte také možnost ladění vzdáleně.  
  
> [!NOTE]
>  Pokud bylo nainstalovat a odinstalovat na váš počítač více verzí sady Visual Studio, WF3 ladění neúspěšně s jedním z existují následující dvě možnosti:  
>   
>  -   Nejsou vaše zarážky.  
> -   Zobrazí se následující zpráva:  
>   
>  **Nelze spustit ladění na webovém serveru. Ladicí program není správně nainstalován.  Nelze ladění na požadovaný typ kódu.  Spusťte instalační program a nainstalujte nebo opravte ladicího programu.**  
>   
>  Pokud některý z těchto scénářů dojde při ladění v rozhraní .NET Framework 3.0 nebo 3.5 pracovní postupy, provádění a opravit instalaci sady Visual Studio.  
  
 [!INCLUDE[wf2](../workflow-designer/includes/wf2_md.md)]se integruje s následující standard [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ladění windows:  
  
-   **Breakpoint –**: funguje podle očekávání, můžete však zadat aktivitu pro název funkce.  
  
-   **Zásobník volání**: změněné zajistit přehled aktivit, které mají spustit v instanci pracovního postupu. Položky v **zásobníkem volání** okna jsou nejprve v úrovni hledání provádění aktivity. Dvakrát klikněte na položku pro přesunout zaměření na vybranou aktivitou.  
  
-   **Vlákna**: poskytuje ID instance k instanci pracovního postupu, který je právě laděn.  
  
 Visual Studio pro Windows Workflow Foundation nepodporuje následující funkce ladění:  
  
-   Podmíněné zarážky na plochu návrháře.  
  
-   QuickWatch.  
  
-   Nastavit další příkaz.  
  
-   Spusťte ke kurzoru.  
  
-   Upravit a pokračovat.  
  
-   Ladění za běhu.  
  
-   Ladění ve smíšeném režimu.  
  
## <a name="in-this-section"></a>V tomto oddílu  
 [Vyvolání ladicího programu sady Visual Studio pro Windows Workflow Foundation (zastaralé)](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [Zakázání ladicího programu sady Visual Studio pro Windows Workflow Foundation (zastaralé)](../workflow-designer/disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [Postupy: ladění pracovních založený na technologii ASP.NET (zastaralé)](../workflow-designer/how-to-debug-aspnet-based-workflows-legacy.md)  
  
 [Postupy: Nastavte zarážky v pracovních postupech (zastaralé)](../workflow-designer/how-to-set-breakpoints-in-workflows-legacy.md)  
  
 [Ladění pracovních ze vzdáleného počítače (zastaralé)](../workflow-designer/debugging-workflows-from-a-remote-computer-legacy.md)  
  
 [Ladění taktování možnosti (zastaralé)](../workflow-designer/debug-stepping-options-legacy.md)  
  
 [Postupy: Změna možnost ladění krokování (zastaralé)](../workflow-designer/how-to-change-the-debug-stepping-option-legacy.md)