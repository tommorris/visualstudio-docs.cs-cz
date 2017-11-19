---
title: "Chyba: Webový Server nenalezl požadovaný prostředek | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords: debugger, Web application errors
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 782abbf8a5cb30801bbe6041143e031792ff247a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Chyba: Webový server nenalezl požadovaný prostředek.
Z hlediska zabezpečení služba IIS vrátila Obecná chyba.  
  
 Možnou příčinou je konfigurace zabezpečení serveru. Služby IIS 6.0 a starší verze použít rozšíření programu, označuje jako modulem URLScan filtrovat požadavky podezřelé a poškozený. IIS 7.0 má k tomuto účelu filtrování předdefinovaných požadavků. V obou případech filtrování žádostí příliš omezující zabránit v sadě Visual Studio ladění serveru.  
  
 Existuje řada možných příčin této chyby. Několik nejběžnější příčiny zahrnout problém s instalaci služby IIS nebo konfigurace, konfiguraci webového serveru nebo oprávnění systému souborů. Můžete zkusit přístupu k prostředku s prohlížečem. V závislosti na konfiguraci služby IIS, můžete chtít použít místní prohlížeč na serveru nebo zkontrolujte v protokolu chyb služby IIS k získání podrobné chybové zprávy.  
  
 Další informace o řešení potíží s IIS, naleznete v části [správu služby IIS a správa](http://go.microsoft.com/fwlink/?LinkId=255872).  
  
## <a name="see-also"></a>Viz také  
 [Nástroj UrlScan zabezpečení](http://www.microsoft.com/technet/security/tools/urlscan.mspx)   
 [Chyba: Webový Server byl uzamčen a blokuje příkaz DEBUG.](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)