---
title: 'Postupy: použití hledání v Návrháři pracovních postupů | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f42d3115-2ed2-4941-8f1e-92dac41c30fa
caps.latest.revision: 3
author: steved0x
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 5c66286aa8647644bf32e0d805c2ff8d0f574991
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633772"
---
# <a name="how-to-use-search-in-the-workflow-designer"></a>Postupy: použití hledání v Návrháři postupu provádění
Pro usnadnění vytváření rozsáhlejších, složitějších pracovních postupů, hledání můžete využívat v Návrháři pracovních postupů pro vyhledání položek – klíčové slovo. Všimněte si, že návrhář nepodporuje nahrazení. Hledání v Návrháři najdete následující:  
  
## <a name="quick-find"></a>Rychlé hledání  
 Rychlé vyhledání v Návrháři najdete následující:  
  
-   Vlastnosti <xref:System.Activities.Activity> objekty, <xref:System.Activities.Statements.FlowNode> objekty, <xref:System.Activities.Statements.State> objekty, přechodů a další položky vlastní řízení toku.  
  
-   Proměnné  
  
-   Arguments  
  
-   Výrazy  
  
#### <a name="using-quick-find"></a>Použití rychlého hledání  
  
1.  Otevřít Návrhář pracovního postupu, stiskněte **Ctrl + F**, nebo vyberte **upravit**, **najít a nahradit**, **rychlé hledání**.  
  
2.  Zadejte hledaný termín do **najít** textového pole a klikněte na tlačítko **najít další**.  
  
3.  Hledaný termín se bude nacházet v aktuálním pracovním postupu. Následující snímek obrazovky ukazuje zobrazovaný název aktivity se nachází v návrháři.  
  
     ![Výsledek vyhledávání v Návrháři postupu provádění](../workflow-designer/media/designersearch.png "DesignerSearch")  
  
## <a name="find-in-files"></a>Najít v souborech  
 Použití hledání v souborech bude vyhledávat řetězce soubory pracovního postupu, včetně souborů XAML.  
  
#### <a name="using-find-in-files"></a>Použití hledání v souborech  
  
1.  V sadě Visual Studio, stiskněte klávesu **Ctrl + Shift + F**, nebo vyberte **upravit**, **najít a nahradit**, **najít v souborech**  
  
2.  Zadejte hledaný termín do **najít** textového pole a klikněte na tlačítko **najít vše**  
  
3.  Zobrazí se výsledek hledání v [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)] **najít výsledek** zobrazení. Položka výsledků dvakrát klikněte na aktivitu, která obsahuje shodu v Návrháři pracovních postupů.