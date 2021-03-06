---
title: Programy | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], programs
- programs, debugging
ms.assetid: e1f955d8-95da-493b-837e-e97741a26d7e
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2c6db9d45f9bb421738b71e630482cbbb8f6525c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42686747"
---
# <a name="programs"></a>Programy
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [programy](https://docs.microsoft.com/visualstudio/extensibility/debugger/programs).  
  
Z hlediska architektury ladicího programu **program**:  
  
-   Je kontejner pro sadu vláken a sady modulů. Program nemá žádné jeden přirovnání v operačním systému Windows.  
  
     Program je druh podproces. Například při ladění webu, skript se dají považovat za programu. Při spuštění skriptu v procesu skriptovací stroj nezávisle na jiné skripty také má svou vlastní sadu vláken. Ladicí stroj (DE) připojí k programu a nikoli do procesu nebo vlákna.  
  
-   Můžete identifikovat samostatně a proces je spuštěn v a lze připojit k být odpojen od a popisují DE, který byl vytvořen, pokud existuje. Program lze spustit, zastavit, pokračovat a být ukončena.  
  
-   Můžete zobrazit výčet všech podprocesů. Program lze také zadat vlastní datový proud zpětný překlad a můžete zobrazit výčet všech kontextech kód z daného dokumentu pozice.  
  
-   Je reprezentován [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) rozhraní vytvořené předtím, než je připojen program, nebo jako součást procesu připojení, v závislosti na implementaci. Při port vytvoří výčet programy, které proces, každý program je vytvořena v souladu s odpovídající [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md) rozhraní předán jako argument [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md). Ladicí stroj také vytvořit `IDebugProgram2` rozhraní k reprezentaci programy, tyto programy nejsou vytvářena v souladu s uzlem programu. `IDebugProgramNode2` Rozhraní vytvořené Zavedenými se používají pro skutečné ladění, zatímco vytvořených port se používá pouze pro zjištění, jaké programy jsou spuštěny v procesu.  
  
## <a name="see-also"></a>Viz také  
 [Procesy](../../extensibility/debugger/processes.md)   
 [Uzly programů](../../extensibility/debugger/program-nodes.md)   
 [Moduly](../../extensibility/debugger/modules.md)   
 [Koncepty ladicího programu](../../extensibility/debugger/debugger-concepts.md)   
 [Ladicí stroj](../../extensibility/debugger/debug-engine.md)   
 [Pozice dokumentu](../../extensibility/debugger/document-position.md)   
 [Kontext kódu](../../extensibility/debugger/code-context.md)   
 [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)

