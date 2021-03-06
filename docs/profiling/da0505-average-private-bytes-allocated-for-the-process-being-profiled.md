---
title: 'DA0505: Průměr nesdílených bajtů přidělených pro profilovaný proces | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0505
- vs.performance.rules.DA0505
- vs.performance.505
ms.assetid: 32c612ea-d077-44ba-8e6f-3a96333bad00
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 104c78732d4f0171fc372c1bfa2848fb11b34b04
ms.sourcegitcommit: 4cd4aef53e7035d23e7d1d0f66f51ac8480622a1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/05/2018
ms.locfileid: "34766373"
---
# <a name="da0505-average-private-bytes-allocated-for-the-process-being-profiled"></a>DA0505: Průměr Nesdílených bajtů přidělených pro profilovaný Proces
|||  
|-|-|  
|Id pravidla|DA0505|  
|Kategorie|Správa prostředků|  
|Metoda profilace|Všechny|  
|Zpráva|Tyto informace byly získány pouze pro informaci. Čítač soukromých bajtů procesu měří virtuální paměti přidělené procesu, který se profilace. Hodnota hlášené je počítaný průměrem přes všechny intervaly měření.|  
|Typ pravidla|Informace o|  
  
 Pokud je profil s použitím vzorkování, využívání paměti rozhraním .NET nebo metody sporu prostředků, musí shromažďovat alespoň 10 vzorků pro aktivaci tohoto pravidla.  
  
## <a name="rule-description"></a>Popis pravidla  
 Tato zpráva hlásí Průměrná velikost virtuální paměti, který tento proces alokoval aktuálně v bajtech (nesdílených bajtů). Nesdílených bajtů představuje umístění virtuální paměti, které byly přiděleny proces, který lze přistupovat pouze vláken běžících v rámci procesu.  
  
 Pro 32bitové procesů spuštěných na 32bitový počítač horní limit počtu soukromá část adresní prostor procesu je 2 GB. Pomocí [3 GB](http://go.microsoft.com/fwlink/?LinkId=177831) přepínač Boot.ini 32bitovými procesy můžete získat až 3 GB virtuální paměti. 32bitový proces, který běží na 64bitový počítač můžete získat až 4 GB privátní virtuální paměti.  
  
 64bitová verze procesu, který je spuštěn na 64bitový počítač můžete získat až 8 TB privátní virtuální paměti.  
  
 Hodnotu hlášenou je průměrem přes všechny intervaly měření, ve kterých byl aktivní profilovaným procesem.  
  
 Další informace o procesu adresní prostory, najdete v části [virtuální adresní prostor](http://go.microsoft.com/fwlink/?LinkId=177832) v dokumentaci k Windows Správa paměti.  
  
## <a name="how-to-use-rule-data"></a>Jak používat data pravidla  
 Použijte hlášené hodnotu k porovnání výkonu různých verzí nebo sestavení tohoto programu nebo pochopit výkon aplikace v různých scénářích profilování.