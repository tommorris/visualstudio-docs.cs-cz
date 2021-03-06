---
title: Potíží s metrikami kódu | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f2fdb995-4888-4246-85dc-7bacadd45968
caps.latest.revision: 6
author: erickson-doug
ms.author: gewarren
manager: douge
ms.openlocfilehash: 2cadd72f23fee6b89804fdbe61b105ff36b89caf
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675648"
---
# <a name="troubleshooting-code-metrics-issues"></a>Řešení potíží s metrikami kódu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [potíží metriky kódu](https://docs.microsoft.com/visualstudio/code-quality/troubleshooting-code-metrics-issues).  
  
Některé z těchto problémů může dojít při shromažďování metrik kódu:  
  
-   [Změny ve výpočtech složitost kódu sady Visual Studio 2010](#Changes_in_Visual_Studio_2010_code_complexity_calculations)  
  
##  <a name="Changes_in_Visual_Studio_2010_code_complexity_calculations"></a> Změny ve výpočtech složitost kódu sady Visual Studio 2010  
 Pro stejnou funkci počítá metrika složitost kódu v [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] může lišit od metrika počítá v předchozích verzích [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)] v těchto situacích:  
  
-   Funkce obsahuje jeden nebo více bloky catch. V předchozích verzích [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)], catch bloky nebyly zahrnutých do výpočtu. V [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)], složitost každého bloku catch se přidá do složitost funkce.  
  
-   Funkce obsahuje příkaz switch (Select Case v jazyce Visual Basic). Kompilátor rozdíly mezi [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] a starší verze můžete vygenerovat různé kód jazyka MSIL pro některé příkazů přepínače, které obsahují propuštěním případy.  
  
## <a name="see-also"></a>Viz také  
 [Měření složitosti a udržovatelnosti spravovaného kódu](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)



