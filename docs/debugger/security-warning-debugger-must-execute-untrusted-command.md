---
title: "Upozornění zabezpečení: Ladicí program musí spustit nedůvěryhodný příkaz | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.sourceserver.securityalert
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: e5c004b3-b364-4098-ac98-770076ca9981
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 21daec7113462221b392b5f29b1604a24fe5c74c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="security-warning-debugger-must-execute-untrusted-command"></a>Upozornění zabezpečení: Ladicí program musí spustit nedůvěryhodný příkaz.
Toto dialogové okno upozornění se zobrazí, když používáte zdrojového serveru. Znamená to, ladicího programu je potřeba provést k získání zdrojového kódu příkaz není v seznamu důvěryhodných příkazy pro zdrojový Server, které jsou obsažené v souboru srcsvr.ini. Pokud je to platný příkaz, můžete ho přidat do souboru srcsvr.ini. Jinak by neměl spustit ho. Další informace najdete v tématu [zadejte symbolu (.pdb) a zdrojových souborů](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).  
  
## <a name="message-text"></a>Text zprávy  
 **Ladicí program musí spustit následující nedůvěryhodný příkaz získat zdrojového kódu ze zdrojového serveru.**  
  
 **Pokud ladění symbolů souboru (\*PDB) není ze známé a důvěryhodné zdroje, tento příkaz může být neplatná nebo nebezpečných ke spuštění.**  
  
 **Opravdu chcete spustit tento příkaz?**  
  
## <a name="uielement-list"></a>Seznam prvků uživatelského rozhraní  
 Textové pole  
 Příkaz ze souboru PDB ke spuštění.  
  
 Spustit  
 Povolte příkaz ke spuštění.  
  
 Nespouštět  
 Zastavte provádění příkazu a stahování souborů ze zdrojového serveru.  
  
## <a name="see-also"></a>Viz také  
 [Zadání symbolu (.pdb) a zdrojových souborů](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)   
 [Zabezpečení ladicího programu](../debugger/debugger-security.md)   
 [Zdrojový Server](http://msdn.microsoft.com/library/windows/desktop/ms680641\(v=vs.85\).aspx)