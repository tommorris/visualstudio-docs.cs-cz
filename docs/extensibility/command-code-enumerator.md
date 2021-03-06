---
title: Enumerátor kódu příkazu | Dokumentace Microsoftu
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- command code enumerator
- source control plug-ins, command code enumeration
ms.assetid: 5d2c360c-59e4-4da8-bcb4-dd07c7441e40
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 67c133339f47a3f15822e4ff79587f9a09253a66
ms.sourcegitcommit: 25a62c2db771f938e3baa658df8b1ae54a960e4f
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/24/2018
ms.locfileid: "39231971"
---
# <a name="command-code-enumerator"></a>Enumerátor kódu příkazu
Tento výčet je používán možnosti [sccgetcommandoptions –](../extensibility/sccgetcommandoptions-function.md) a [sccpopulatelist –](../extensibility/sccpopulatelist-function.md)označíte, příkazu, pro který jsou zadány možnosti.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
enum SCCCOMMAND {  
   SCC_COMMAND_GET,  
   SCC_COMMAND_CHECKOUT,  
   SCC_COMMAND_CHECKIN,  
   SCC_COMMAND_UNCHECKOUT,  
   SCC_COMMAND_ADD,  
   SCC_COMMAND_REMOVE,  
   SCC_COMMAND_DIFF,  
   SCC_COMMAND_HISTORY,  
   SCC_COMMAND_RENAME,  
   SCC_COMMAND_PROPERTIES,  
   SCC_COMMAND_OPTIONS  
};  
```  
  
## <a name="members"></a>Členové  
 SCC_COMMAND_GET  
 Odpovídá [sccget –](../extensibility/sccget-function.md).  
  
 SCC_COMMAND_CHECKOUT  
 Odpovídá [scccheckout –](../extensibility/scccheckout-function.md).  
  
 SCC_COMMAND_CHECKIN  
 Odpovídá [scccheckin –](../extensibility/scccheckin-function.md).  
  
 SCC_COMMAND_UNCHECKOUT  
 Odpovídá [sccuncheckout –](../extensibility/sccuncheckout-function.md).  
  
 SCC_COMMAND_ADD  
 Odpovídá [sccadd –](../extensibility/sccadd-function.md).  
  
 SCC_COMMAND_REMOVE  
 Odpovídá [sccremove –](../extensibility/sccremove-function.md).  
  
 SCC_COMMAND_DIFF  
 Odpovídá [sccdiff –](../extensibility/sccdiff-function.md).  
  
 SCC_COMMAND_HISTORY  
 Odpovídá [scchistory –](../extensibility/scchistory-function.md).  
  
 SCC_COMMAND_RENAME  
 Odpovídá [sccrename –](../extensibility/sccrename-function.md).  
  
 SCC_COMMAND_PROPERTIES  
 Odpovídá [sccproperties –](../extensibility/sccproperties-function.md).  
  
 SCC_COMMAND_OPTIONS  
 Odpovídá [sccsetoption –](../extensibility/sccsetoption-function.md).  
  
## <a name="see-also"></a>Viz také:  
 [Ovládací prvek moduly plug-in zdrojového kódu](../extensibility/source-control-plug-ins.md)   
 [Sccgetcommandoptions –](../extensibility/sccgetcommandoptions-function.md)   
 [Sccpopulatelist –](../extensibility/sccpopulatelist-function.md)