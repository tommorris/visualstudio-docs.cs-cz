---
title: 'Postupy: shromažďování dat vzorkování na úrovni řádku | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- performance tools, line-level sampling
ms.assetid: 44803aad-dd39-4c2e-9209-d35185d44983
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a10c8db7a9706c406cb192f9418c1fd8d04e888a
ms.sourcegitcommit: 4cd4aef53e7035d23e7d1d0f66f51ac8480622a1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/05/2018
ms.locfileid: "34765697"
---
# <a name="how-to-collect-line-level-sampling-data"></a>Postupy: shromažďování dat vzorkování na úrovni řádku
Vzorkování na úrovni řádku je schopnost profileru určit procesoru v kódu náročná na výkon procesoru funkce, jako je například funkci, která má vysokou výhradní ukázky, kde má zatěžovat většinu času.  
  
## <a name="overview"></a>Přehled  
 Vzorkování na úrovni řádku, profileru prochází zásobník volání program v nastavených intervalech a agreguje výsledků. Tyto výsledky zobrazit jaké pokyny procesor byla spuštěna při ukázky byly provedeny. Shromážděná data o výhradní ukázky se pak analyzují k identifikaci řádků kód a ukazatele instrukce (IP).  
  
 Vzorkování na úrovni řádku funguje pro spravované, jakož i nativní kód. Sestavy pro zvýšení výkonu, které zobrazit tato data zahrnují zobrazení řádků a zobrazení modulů.  
  
 Informace o zahájení a ukončení znak není k dispozici pro nativní kód. Víceřádkový příkazy řádku začít informace není k dispozici pro nativní kód; k dispozici pouze informace end řádku.  
  
### <a name="available-data"></a>K dispozici data  
 K dispozici vzorkování na úrovni řádku data zahrnují následující informace:  
  
-   Název funkce.  
  
-   Adresa funkce.  
  
-   Řádky začít – číslo řádku jen Vzorkovaná kódu.  
  
-   Konec řádku - koncová číslo řádku zdroje. Toto je obecně stejná jako "Řádku begin" data s výjimkou případů, kdy jediný příkaz programu zahrnuje více řádků zdrojového kódu.  
  
-   Začněte znaků - sloupce začátku souhrnného vzorku. Obvykle se jedná o 0, s výjimkou případů, kdy jeden řádek obsahuje více příkazů programu.  
  
-   Koncový znak - koncová sloupec souhrnného vzorku.  
  
-   IP - adresu, kde agregační vzorku (pouze v zobrazení IP).  
  
 V **moduly** zobrazit, pokud funkci má Statistika na úrovni řádku, statistiku jsou vnořeny pod jednotlivé funkce. Kromě toho jsou uvedené Statistika na úrovni IP, které jsou vnořené v každém řádku.  
  
### <a name="turn-off-line-level-sampling-for-managed-code"></a>Vypnout vzorkování na úrovni řádku pro spravovaný kód  
 Vzorkování na úrovni řádku je ve výchozím nastavení zapnutá. Shromažďování dat na úrovni řádků pro spravovaný kód můžete vypnout pomocí jedné z následujících příkazů:  
  
-   Před profilování, zadejte **vsperfclrenv – /samplelineoff**. To ovlivní aplikace a služby.  
  
     – nebo –  
  
-   Při spouštění aplikace, zadejte **VSPerfCmd /lineoff \<další argumenty >**.  
  
## <a name="see-also"></a>Viz také:  
 [Konfigurace výkonnostních relací](../profiling/configuring-performance-sessions.md)   
 [Analýza dat nástrojů pro měření výkonu](../profiling/analyzing-performance-tools-data.md)