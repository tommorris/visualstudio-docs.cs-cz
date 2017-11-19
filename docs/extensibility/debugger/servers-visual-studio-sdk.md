---
title: Servery (Visual Studio SDK) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- servers, debugging
- debugging [Debugging SDK], servers
ms.assetid: 62236d64-7956-448c-9ac3-5528f3edac1d
caps.latest.revision: "17"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 496e9b361dbb7f5c3eb5cf5197a1351a1182af3e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="servers-visual-studio-sdk"></a>Servery (Visual Studio SDK)
Z hlediska architektuře ladicího programu **server**:  
  
-   Je kontejnerem porty a všichni dodavatelé port a slouží ke komunikaci porty a všichni dodavatelé port pro relaci ladění správce (SDM) a ladění moduly.  
  
-   Můžete identifikovat podle názvu a výčet jeho porty a všichni dodavatelé portu.  
  
-   Je reprezentována [IDebugCoreServer2](../../extensibility/debugger/reference/idebugcoreserver2.md) rozhraní, což je pouze realizován pomocí sady Visual Studio (jedna instance serveru pro každou instanci sady Visual Studio spuštěná).  
  
## <a name="see-also"></a>Viz také  
 [Porty](../../extensibility/debugger/ports.md)   
 [Port dodavatelů](../../extensibility/debugger/port-suppliers.md)   
 [Koncepty ladicí program](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugCoreServer2](../../extensibility/debugger/reference/idebugcoreserver2.md)