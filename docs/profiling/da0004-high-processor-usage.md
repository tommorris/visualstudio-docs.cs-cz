---
title: "DA0004: Vysoké využití procesoru | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.performance.rules.DAHighProcessorUsage
- vs.performance.rules.DA0004
- vs.performance.DA0004
- vs.performance.4
ms.assetid: 2c4fb569-929e-4f1d-8c50-b590ee371351
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5eeb6d43ff388050ad9c1fa8140f2e6bdfb352ac
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="da0004-high-processor-usage"></a>DA0004: Vysoké využití procesoru
|||  
|-|-|  
|Id pravidla|DA0004|  
|Kategorie|Použití nástroje pro profilaci|  
|Metod profilace|Instrumentace<br /><br /> Vzorkování|  
|Zpráva|Vaše využití procesoru je větší než 75 % konzistentně. Zvažte použití režimu vzorkování pro aplikace vázané na procesor.|  
|Typ pravidla|Informace o|  
  
 Pokud je profil s použitím vzorkování, využívání paměti rozhraním .NET nebo metody sporu prostředků, musí shromažďovat alespoň 10 vzorků pro aktivaci tohoto pravidla.  
  
## <a name="cause"></a>příčina  
 Využití procesoru (CPU) byla v profilaci data, která nebyla shromážděna pomocí metody instrumentace výrazně vysoká. Zvažte použití vzorkování metoda profilace při profilace procesor vázaný aplikace.  
  
## <a name="rule-description"></a>Popis pravidla  
 V průběhu této spuštění profilování byly konzistentně velmi zaneprázdněny procesoru (nebo procesory). Vysoké využití procesoru může znamenat aplikace vázané na procesor. Instrumentované profily nejsou obvykle co nejúčinnější způsob, jak prozkoumat využití procesoru scénáře. Vzorkování je obvykle účinnější, pokud jsou profilace aplikací, které stráví velkou část doba pro jejich provádění pokyny na procesor.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Vezměte v úvahu profilace aplikace znovu pomocí metody vzorkování místo metody instrumentace, pokud požadujete časování funkce, nebo vás zajímá více Principy vstupu a výstupu než kritické body procesoru.