---
title: 'DA0502: Maximum spotřeby procesoru profilovaným procesem | Dokumentace Microsoftu'
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
- vs.performance.rules.DA0502
- vs.performance.DA0502
- vs.performance.502
ms.assetid: 1ee53df5-b0dc-4265-9d4f-527830d08725
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: be9b9ff318ade6546369e20d5508b2ad79dc0bb9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42628508"
---
# <a name="da0502-maximum-cpu-consumption-by-the-process-being-profiled"></a>DA0502: Maximum Spotřeby procesoru profilovaným Procesem
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [DA0502: spotřeby maximální procesoru profilovaným procesem](https://docs.microsoft.com/visualstudio/profiling/da0502-maximum-cpu-consumption-by-the-process-being-profiled).  
  
Id pravidla | DA0502 |  
| Kategorie | Sledování prostředků |  
| Metoda profilace | Všechny |  
| Zpráva | Toto pravidlo je pouze pro informaci. Process()\\Čítač % času procesoru měří využití CPU procesu, který profilujete. Hlášená hodnota je maximum pozorované přes všechny intervaly měření. |  
| Typ pravidla | Informační |  
  
 Při profilování pomocí vzorkování, paměti .NET nebo metodám sporu prostředků, musíte shromáždit minimálně 10 vzorky k aktivaci tohoto pravidla.  
  
## <a name="rule-description"></a>Popis pravidla  
 Tato zpráva znamená maximální procento času, který byl procesor zaneprázdněný, provádění instrukcí z aplikace. Hlášená hodnota je maximální hodnota uvedená mezi všechny intervaly měření, ve kterých byl aktivní profilovaný proces. Procento, může být větší než 100 % na počítači s více než jeden procesor.  
  
## <a name="how-to-use-the-rule-data"></a>Jak používat Data pravidla  
 Použijte hodnotu pravidla pro porovnání výkonu různých verzí nebo sestavení tohoto programu nebo porozumět výkonu aplikace v různých scénářích profilování.



