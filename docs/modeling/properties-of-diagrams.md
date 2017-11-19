---
title: "Vlastnosti diagramů | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.dsltools.dsldesigner.dsldiagram
helpviewer_keywords: Domain-Specific Language, diagram
ms.assetid: 00bba4b8-6aa6-4027-96cb-4f4c41a77d3c
caps.latest.revision: "25"
author: alancameronwills
ms.author: awills
manager: douge
ms.openlocfilehash: fcd30a30bdae896be5aceb9dc685a5fb762ee4af
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="properties-of-diagrams"></a>Vlastnosti diagramů
Můžete nastavit vlastnosti, které určují, jak diagramy se zobrazí v Návrháři vygenerovaný. Můžete například zadat výchozí barvu textu v diagramu.  
  
 Další informace najdete v tématu [jak definovat jazyka domény](../modeling/how-to-define-a-domain-specific-language.md). Další informace o tom, jak používat tyto vlastnosti najdete v tématu [přizpůsobení a rozšíření jazyka domény](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
 Následující tabulka uvádí vlastnosti diagramů.  
  
|Vlastnost|Popis|Výchozí|  
|--------------|-----------------|-------------|  
|Barva výplně|Barva výplně diagramu.|prázdné|  
|Barva textu|Barva textu, který se zobrazí v diagramu.|černé|  
|Modifikátor přístupu|Modifikátor přístupu – třída (veřejné nebo interní).|Public|  
|Vlastní atributy|Použít k přidání atributů do třídy generovaného kódu.|\<žádné >|  
|Generuje dvojitou odvozené|Pokud `True`, budou generovány základní třídu a částečné třídy (pro podporu přizpůsobení prostřednictvím přepsání). Další informace najdete v tématu [přepsání a rozšíření třídy generované](../modeling/overriding-and-extending-the-generated-classes.md).|False|  
|Má vlastní – konstruktor|Pokud `True`, bude k dispozici vlastní konstruktor v zdrojového kódu. Další informace najdete v tématu [přepsání a rozšíření třídy generované](../modeling/overriding-and-extending-the-generated-classes.md)...|False|  
|Modifikátor dědičnosti|Popisuje typ dědičnost třídy zdrojového kódu, která se generují z diagramu (`none`, `abstract` nebo `sealed`).|Žádné|  
|Základní Diagram|Základní třída tohoto diagramu.|(žádný)|  
|Název|Název tohoto diagramu.|Aktuální název|  
|Obor názvů|Obor názvů, který je přidružený tohoto diagramu.|Aktuální obor názvů|  
|Třída je reprezentovaná|Třída kořenové domény, která představuje tohoto diagramu.|Pokud je k dispozici aktuální kořenová třída|  
|Poznámky|Neformální poznámky, které jsou spojeny s tímto elementem.|\<žádné >|  
|Barva výplně zpřístupňuje jako vlastnost|Pokud `True`, může uživatel nastavit barvu výplně diagram generovaný návrháře. Chcete-li tuto možnost nastavíte, klikněte pravým tlačítkem na tvar diagram a klikněte na **přidat Explosed**.|False|  
|Zpřístupní barvy jako vlastnost|Pokud `True`, může uživatel nastavit v Návrháři generované barvy diagramu. Chcete-li tuto možnost nastavíte, klikněte pravým tlačítkem na tvar diagram a klikněte na **přidat Explosed**.|False|  
|Popis|Popis, který se používá k dokumentu generovaný návrháře.|\<žádné >|  
|Zobrazovaný název|Název, který se zobrazí v Návrháři vygenerovaný pro toto schéma.|\<žádné >|  
|Nápověda – klíčové slovo|Klíčové slovo, které se používá k indexu F1 – Nápověda pro tohoto diagramu.|\<žádné >|  
  
## <a name="see-also"></a>Viz také  
 [Glosář nástroje jazyka domény](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)