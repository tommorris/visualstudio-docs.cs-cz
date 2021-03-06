---
title: 'CA2200: Rethrow pro zachování podrobností zásobníku | Dokumentace Microsoftu'
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
- RethrowToPreserveStackDetails
- CA2200
helpviewer_keywords:
- CA2200
- RethrowToPreserveStackDetails
ms.assetid: 046e1b98-c4dc-4515-874f-9c0de2285621
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 5a79dd4f12a2d97cb707a38f4a46e5a20a8436b1
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902326"
---
# <a name="ca2200-rethrow-to-preserve-stack-details"></a>CA2200: Znovu vyvolejte pro zachování podrobností zásobníku
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA2200: Rethrow pro zachování podrobností zásobníku](https://docs.microsoft.com/visualstudio/code-quality/ca2200-rethrow-to-preserve-stack-details).

|||
|-|-|
|TypeName|RethrowToPreserveStackDetails|
|CheckId|CA2200|
|Kategorie|Microsoft.Usage|
|Narušující změna|Pevné|

## <a name="cause"></a>příčina
 Výjimka je znovu vyvolána a výjimky je jednoznačně uvedena v `throw` příkazu.

## <a name="rule-description"></a>Popis pravidla
 Jakmile je vyvolána výjimka, je součástí informace, které vykonává trasování zásobníku. Trasování zásobníku je seznam hierarchii volání metody, který začíná metody, která vyvolá výjimku a končí u metody, která zachytí výjimku. Pokud výjimka je znovu vyvolána zadáním výjimky v `throw` prohlášení, trasování zásobníku se restartuje v aktuální metodě a dojde ke ztrátě seznam volání metody mezi původní metodou, která vyvolala výjimku a aktuální metoda. Chcete-li zachovat původní informace o trasování zásobníku s tím rozdílem, použijte `throw` příkaz bez zadání výjimku.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, opětovné vyvolání výjimky bez explicitním zadáním výjimky.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění na toto pravidlo.

## <a name="example"></a>Příklad
 Následující příklad ukazuje metodu, `CatchAndRethrowExplicitly`, který porušuje pravidla a metodu, `CatchAndRethrowImplicitly`, který splňuje pravidlo.

 [!code-csharp[FxCop.Usage.Rethrow#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.Rethrow/cs/FxCop.Usage.Rethrow.cs#1)]
 [!code-vb[FxCop.Usage.Rethrow#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.Rethrow/vb/FxCop.Usage.Rethrow.vb#1)]



