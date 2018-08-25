---
title: 'CA1309: Použijte Řadový StringComparison | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- UseOrdinalStringComparison
- CA1309
helpviewer_keywords:
- UseOrdinalStringComparison
- CA1309
ms.assetid: 19be0854-cb6e-4efd-a4c8-a5c1fc6f7a71
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e18bd9d15b9b17268e4002268394cf6149722b0a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672312"
---
# <a name="ca1309-use-ordinal-stringcomparison"></a>CA1309: Použijte řadový StringComparison
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1309: použijte Řadový StringComparison](https://docs.microsoft.com/visualstudio/code-quality/ca1309-use-ordinal-stringcomparison).  
  
TypeName | UseOrdinalStringComparison |  
| ID kontroly | CA1309 |  
| Kategorie | Microsoft.Globalization|  
| Zásadní změna | Ukončování bez |  
  
## <a name="cause"></a>příčina  
 Který je nelingvistická operace porovnání řetězců nemá nastaven <xref:System.StringComparison> buď parametr **pořadí** nebo **OrdinalIgnoreCase**.  
  
## <a name="rule-description"></a>Popis pravidla  
 Mnoho řetězec operace, nejdůležitější <xref:System.String.Compare%2A?displayProperty=fullName> a <xref:System.String.Equals%2A?displayProperty=fullName> metody, teď poskytují přetížení přijímající <xref:System.StringComparison?displayProperty=fullName> hodnotu výčet jako parametr.  
  
 Pokud zadáte buď **StringComparison.Ordinal** nebo **StringComparison.OrdinalIgnoreCase**, bude nelingvistická porovnání řetězců. To znamená funkce, které jsou specifické pro přirozený jazyk se ignorují porovnání se při rozhodování. To znamená, že rozhodnutí, která jsou založené na porovnání jednotlivých bajtů a ignorovat velká a malá písmena nebo ekvivalence tabulek, které jsou parametrizovány podle jazykové verze. V důsledku toho podle explicitním nastavením parametru na buď **StringComparison.Ordinal** nebo **StringComparison.OrdinalIgnoreCase**, váš kód často získá rychlost, zvyšuje správnosti a změní spolehlivější.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Chcete-li opravit porušení tohoto pravidla, změňte metodu porovnání řetězce na přetížení přijímající <xref:System.StringComparison?displayProperty=fullName> výčet jako parametr a zadat buď **pořadí** nebo **OrdinalIgnoreCase**. Například změnit `String.Compare(str1, str2)` k `String.Compare(str1, str2, StringComparison.Ordinal)`.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Je bezpečné potlačit upozornění tohoto pravidla, když aplikace a knihovny je určena pro určité místní cílové skupině nebo sémantiku aktuální jazyková verze by měla sloužit.  
  
## <a name="see-also"></a>Viz také  
 [Upozornění globalizace](../code-quality/globalization-warnings.md)   
 [CA1307: Zadejte možnosti StringComparison](../code-quality/ca1307-specify-stringcomparison.md)


