---
title: 'CA1809: Vyhněte se nadměrným místním hodnotám | Dokumentace Microsoftu'
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
- CA1809
- AvoidExcessiveLocals
helpviewer_keywords:
- AvoidExcessiveLocals
- CA1809
ms.assetid: 5c81ea43-cb49-448f-980f-a1dd9764043c
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c41836e2a7e7e5530d83ff0eaf854b88de42f38f
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42901738"
---
# <a name="ca1809-avoid-excessive-locals"></a>CA1809: Vyhněte se nadměrným místním hodnotám
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1809: Vyhněte se nadměrným místním hodnotám](https://docs.microsoft.com/visualstudio/code-quality/ca1809-avoid-excessive-locals).

|||
|-|-|
|TypeName|AvoidExcessiveLocals|
|CheckId|CA1809|
|Kategorie|Microsoft.Performance|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Člen obsahuje více než 64 místních proměnných, z nichž některé mohou být vygenerovaný kompilátorem.

## <a name="rule-description"></a>Popis pravidla
 Běžnou optimalizací výkonu je uložení hodnoty v registru procesoru místo v paměti, což se označuje jako *enregistering* hodnotu. Modul common language runtime bere v úvahu pro enregistration až 64 místních proměnných. Proměnné, které nejsou uloženy v registrech procesoru jsou vloženy do zásobníku a musí přesunout do registru před manipulaci. Chcete-li možnost povolit, že všechny místní proměnné získat uloženy v registrech procesoru, omezte počet lokálních proměnných na 64.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, Refaktorujte implementace používat více než 64 místních proměnných.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Je bezpečné, můžete potlačit upozornění tohoto pravidla nebo zakážete pravidlo, pokud výkon není problém.

## <a name="related-rules"></a>Související pravidla
 [CA1804: Odeberte nepoužívané místní hodnoty](../code-quality/ca1804-remove-unused-locals.md)



