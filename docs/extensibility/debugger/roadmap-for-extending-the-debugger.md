---
title: "Plán pro rozšíření ladicího programu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], roadmap
- Debugging SDK, roadmap
ms.assetid: 1f4096a8-f7aa-4dfa-84e1-6d59263e70bb
caps.latest.revision: "16"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: af86f2b8daeffeb700b619c4ba0d9cbb00700dd8
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="roadmap-for-extending-the-debugger"></a>Plán pro rozšíření ladicí program
Tato dokumentace poskytuje průvodce a referenční informace pro rozšíření [!INCLUDE[vs_current_short](../../code-quality/includes/vs_current_short_md.md)] ladicího programu s [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)].  
  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]ladění dokumentace obsahuje ukázky, komplexní odkaz a několik reprezentativní scénáře, které ukazují typické způsoby, jak přizpůsobit ladicího programu.  
  
 Vaše kompilátoru a její výstup zjistit, co je potřeba provést k implementaci ladění ve vašem produkt. Pokud vaše kompilátoru:  
  
-   Cílem nativní operační systém Windows a zapisuje. Soubor PDB, můžete ladit programy s modulem ladění nativního kódu (DE), která je integrována do [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Není nutné k implementaci vyhodnocování DE nebo výraz. Vyhodnocení výrazu je napsán pro syntaxi programovacího jazyka C++.  
  
-   Vytvoří výstup (MSIL intermediate language), můžete ladit programy s modulem ladění spravovaného kódu DE, což je také součástí Microsoft [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Proto musí implementovat pouze vyhodnocení výrazu. Vyhodnocovací filtr výrazů ukázkové zajišťuje za vás. Další informace naleznete v následujících tématech:  
  
     [Vyhodnocení výrazu](../../extensibility/debugger/expression-evaluation-visual-studio-debugging-sdk.md)  
  
     [Vyhodnocení výrazů](../../extensibility/debugger/evaluating-expressions.md)  
  
     [Kontext vyhodnocení výrazu](../../extensibility/debugger/expression-evaluation-context.md)  
  
     [Vyhodnocení výrazu v režimu pozastavení](../../extensibility/debugger/expression-evaluation-in-break-mode.md)  
  
     [Zápis běžné vyhodnocení výrazu Runtime jazyka](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)  
  
-   Cíle a chráněné operačního systému nebo jiných běhové prostředí, budete muset napsat vlastní DE. Kurz, který vytvoří jednoduchý DE pomocí knihovny ATL COM je k dispozici. Další informace naleznete v následujících tématech:  
  
     [Vytváření vlastních ladění modulu](../../extensibility/debugger/creating-a-custom-debug-engine.md)  
  
     [Kurz: Vytvoření modul ladění pomocí knihovny ATL COM](http://msdn.microsoft.com/en-us/9097b71e-1fe7-48f7-bc00-009e25940c24)  
  
     [Implementace Port dodavatele](../../extensibility/debugger/implementing-a-port-supplier.md)  
  
     [Ukázky](../../extensibility/debugger/visual-studio-debugging-samples.md)  
  
## <a name="see-also"></a>Viz také  
 [Začínáme](../../extensibility/debugger/getting-started-with-debugger-extensibility.md)