---
title: 'Postupy: vyloučení projektů ze sestavení | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 17a837ca-5db9-46cd-b5a7-b14ad1d2c47d
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 569f0db1294bd7df2451c4ec496dc5064b122b73
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670031"
---
# <a name="how-to-exclude-projects-from-a-build"></a>Postupy: Vyloučení projektů ze sestavení
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: vyloučení projektů ze sestavení](https://docs.microsoft.com/visualstudio/ide/how-to-exclude-projects-from-a-build).  
  
Vytvoření řešení bez nutnosti všechny projekty, které obsahuje. Například může vyloučit projektu, který naruší sestavení. Může pak sestavíte projekt po můžete prozkoumat a adresu problémy.  
  
 Projekt můžete vyloučit pomocí následujících postupů:  
  
-   Odstraněním dočasně konfiguraci aktivního řešení.  
  
-   Vytvoření konfigurace řešení, která neobsahuje projekt.  
  
 Další informace najdete v tématu [Principy konfigurací sestavení](../ide/understanding-build-configurations.md).  
  
### <a name="to-temporarily-remove-a-project-from-the-active-solution-configuration"></a>K dočasnému odstranění projektu z konfigurace aktivního řešení  
  
1.  V panelu nabídky zvolte **sestavení**, **nástroje Configuration Manager**.  
  
2.  V **projektu kontexty** tabulky, najděte projektu, které chcete vyloučit ze sestavení.  
  
3.  V **sestavení** sloupec pro projekt, zrušte zaškrtnutí políčka.  
  
4.  Zvolte **Zavřít** tlačítko a pak znovu sestavte řešení.  
  
### <a name="to-create-a-solution-configuration-that-excludes-a-project"></a>Pro vytvoření konfigurace řešení, která nezahrnuje projektu  
  
1.  V panelu nabídky zvolte **sestavení**, **nástroje Configuration Manager**.  
  
2.  V **konfigurace aktivního řešení** klikněte na položku  **\<nový >**.  
  
3.  V **název** pole, zadejte název konfigurace řešení.  
  
4.  V **Kopírovat nastavení z:** klikněte na položku konfigurace řešení, na kterém chcete vytvořit novou konfiguraci (například **ladění**) a klikněte na tlačítko **OK** tlačítko .  
  
5.  V **nástroje Configuration Manager** dialogové okno, zrušte zaškrtnutí políčka v **sestavení** sloupec pro projekt, který chcete vyloučit a klikněte na tlačítko **Zavřít** tlačítko.  
  
6.  Na **standardní** nástrojů, ověřte, zda je nová konfigurace řešení v aktivní konfiguraci **konfigurace řešení** pole.  
  
7.  V panelu nabídky zvolte **sestavení**, **znovu sestavit řešení**.  
  
## <a name="see-also"></a>Viz také  
 [Principy konfigurací sestavení](../ide/understanding-build-configurations.md)   
 [Postupy: vytvoření a úprava konfigurací](../ide/how-to-create-and-edit-configurations.md)   
 [Postupy: Sestavení více konfigurací současně](../ide/how-to-build-multiple-configurations-simultaneously.md)



