---
title: "Sestava značek | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
caps.latest.revision: "6"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1d9d546e96d92c26725bc8a169c413bc7b96feb7
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="markers-report"></a>Sestava značek
Sestava značek obsahuje seznam značek v zobrazených časovém intervalu.  Posouvání přiblížení a oddálení nebo skrytí pruhů, může způsobit značek zobrazí nebo zmizí. Sestava obsahuje tyto informace o každé značky:  
  
-   Čas ho zahájení, relativně k začátku trasování.  
  
-   Jeho trvání. Doba trvání je nulová pro příznaky a zprávy, protože představují pro rychlé.  
  
-   ID vlákna, která ji vygenerovala.  
  
-   Zprostředkovatel událostí sledování pro Windows (ETW), který ji vygenerovala.  
  
-   Řada značky, ze kterého byla zapsána.  
  
-   Kategorie události, které patří do.  
  
-   Úroveň jeho význam.  
  
-   Typ (rozpětí, příznak nebo zprávy).  
  
-   Podrobný popis co reprezentuje  
  
 Vyberte **exportovat** tlačítko pro uložení sestavy značek jako soubor CSV. Data můžete použít v souboru CSV s jinými aplikace nebo nástroje.  
  
> [!NOTE]
>  Sestava značek můžete zobrazit 1000 značek. Úplné sestavu zobrazíte všechny značky, můžete exportujte do souboru CSV.