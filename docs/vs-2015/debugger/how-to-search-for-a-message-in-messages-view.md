---
title: 'Postupy: hledání zprávy v zobrazení zpráv | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Message Search dialog box
- Messages view
- messages, searching for
ms.assetid: 732b7ccc-54ea-41db-823b-2b96e3e4083e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 984c3f0dc9b61059b53a7caf5a859d3413c99e62
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670162"
---
# <a name="how-to-search-for-a-message-in-messages-view"></a>Postupy: Hledání zprávy v zobrazení zpráv
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: hledání zprávy v zobrazení zpráv](https://docs.microsoft.com/visualstudio/debugger/how-to-search-for-a-message-in-messages-view).  
  
Můžete vyhledat konkrétní zprávy v zobrazení zpráv s použitím jeho popisovač, typ nebo ID zprávy jako kritéria hledání. Některou z těchto – nebo ke kombinaci – bude platný vyhledávací kritéria. Je taky možné specifikovat Počáteční směr hledání. Atributy zprávu aktuálně vybranou se předem načtou pole v dialogovém okně.  
  
### <a name="to-search-for-a-message-in-messages-view"></a>Hledání zprávy v zobrazení zpráv  
  
1.  Uspořádat okna tak tohoto nástroje Spy ++ a aktivní [zobrazení zpráv](../debugger/messages-view.md) okna jsou viditelné.  
  
2.  Z **hledání** nabídce zvolte **najít zprávu**.  
  
     [Dialogové okno hledání zpráv](../debugger/message-search-dialog-box.md) otevře.  
  
3.  Přetáhněte **tažením nástroje hledání** požadované období. Při přetahování nástroj, **hledání zpráv** dialogové okno zobrazí podrobnosti o vybrané okno.  
  
     – nebo –  
  
     Pokud máte popisovač okna jejichž zprávy, které chcete prověřit, zadejte ho do **zpracování** textového pole.  
  
     – nebo –  
  
     Pokud víte, typ nebo ID zprávy, které chcete, vyberte z **typ** a **zpráva** rozevíracích nabídek a zrušte **zpracování** textového pole.  
  
4.  Zrušte zaškrtnutí všech polí, u kterých nechcete k určení hodnot.  
  
    > [!TIP]
    >  Chcete-li přehlednost obrazovky, vyberte **skrýt Spy** možnost. Tato možnost ukrývá hlavním nástroje Spy ++ okně byste museli opustit pouze **najít okno** dialogové okno viditelné nad vaší aplikace. Obnovení hlavního okna nástroje Spy ++, po kliknutí na **OK** nebo **zrušit**, nebo pokud zrušíte výběr **skrýt Spy ++** možnost.  
  
5.  Zvolte **nahoru** nebo **dolů** pro počáteční směr hledání.  
  
6.  Klikněte na tlačítko **OK**.  
  
 Pokud je nalezen odpovídající zprávu, je zvýrazněn v okně zobrazení zprávy. Zobrazit [zobrazení zpráv](../debugger/messages-view.md).



