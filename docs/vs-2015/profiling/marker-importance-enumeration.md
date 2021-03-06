---
title: marker_importance – výčet | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_importance
helpviewer_keywords:
- Concurrency::diagnostic::marker_importance enumeration
ms.assetid: d5524ea0-0227-4d8e-9122-332291042df5
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1564de8b63efa48ad83b1aa09f1fce75ff3fbd75
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670119"
---
# <a name="markerimportance-enumeration"></a>marker_importance – výčet
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [marker_importance – výčet](https://docs.microsoft.com/visualstudio/profiling/marker-importance-enumeration).  
  
Představuje úroveň důležitosti značek Vizualizátor souběžnosti.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
enum marker_importance;  
```  
  
## <a name="members"></a>Členové  
  
### <a name="values"></a>Hodnoty  
  
|Název|Popis|  
|----------|-----------------|  
|`critical_importance`|Určuje, že má značku stěžejní význam.|  
|`high_importance`|Určuje, že značky má vysokou důležitostí.|  
|`low_importance`|Určuje, zda má značku s nízkou důležitostí.|  
|`normal_importance`|Určuje, že značky má normální význam.|  
  
## <a name="requirements"></a>Požadavky  
 **Záhlaví:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::Diagnostic –  
  
## <a name="see-also"></a>Viz také  
 [diagnostic – obor názvů](../profiling/diagnostic-namespace.md)



