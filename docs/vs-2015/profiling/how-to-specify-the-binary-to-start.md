---
title: 'Postupy: určení binárního souboru ke spuštění | Dokumentace Microsoftu'
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
- vs.performance.property.itemlaunch
helpviewer_keywords:
- profiling tools, launching
- performance tools, launching
- performance sessions, launching
ms.assetid: ba77fcf4-8d78-49f1-b8f3-7dd0acf84306
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ec65dd3a5bcc812ff2f7c42ae4cbbba6080664db
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672409"
---
# <a name="how-to-specify-the-binary-to-start"></a>Postupy: Určení binárního souboru ke spuštění
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: určení binárního souboru ke spuštění](https://docs.microsoft.com/visualstudio/profiling/how-to-specify-the-binary-to-start).  
  
Pro binární soubory profilu například knihovny DLL, je třeba zadat informace v  **\<cíl > stránky vlastností** dialogové okno. Tato informace indikuje, kde najít projekt knihovny DLL volající aplikace.  
  
 **Požadavky**  
  
-   [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
### <a name="to-specify-the-executable-to-start"></a>K určení spustitelného souboru spusťte  
  
1.  V **prohlížeč výkonu**, klikněte pravým tlačítkem na cílový binární soubor a potom klikněte na tlačítko **vlastnosti**.  
  
2.  V **stránky vlastností** dialogové okno, klikněte na tlačítko **spuštění** vlastnosti.  
  
3.  Vyberte **přepsat vlastnosti projektu** zaškrtávací políčko.  
  
4.  V **spustitelný soubor ke spuštění** textové pole, zadejte umístění souboru.  
  
5.  V **argumenty** textové pole, zadejte argumenty, které jsou vyžadovány pro spuštění aplikace.  
  
6.  V **pracovní adresář** textové pole, zadejte umístění adresáře.  
  
7.  Klikněte na tlačítko **OK**.  
  
## <a name="see-also"></a>Viz také  
 [Konfigurace výkonnostních relací](../profiling/configuring-performance-sessions.md)



