---
title: 'CA1823: Vyhněte se nepoužitým privátním polím | Dokumentace Microsoftu'
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
- AvoidUnusedPrivateFields
- CA1823
helpviewer_keywords:
- AvoidUnusedPrivateFields
- CA1823
ms.assetid: 614f94f6-0dc7-430f-8124-cb889a4a720f
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bfe51ab6c163c82d413c5c7cc74edc0b980abd85
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42900324"
---
# <a name="ca1823-avoid-unused-private-fields"></a>CA1823: Vyhněte se nepoužitým privátním polím
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1823: Vyhněte se nepoužitým privátním polím](https://docs.microsoft.com/visualstudio/code-quality/ca1823-avoid-unused-private-fields).

|||
|-|-|
|TypeName|AvoidUnusedPrivateFields|
|CheckId|CA1823|
|Kategorie|Microsoft.Performance|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Toto pravidlo je oznamují soukromé pole ve vašem kódu existuje, ale nepoužívá všechny cesty kódu.

## <a name="rule-description"></a>Popis pravidla
 Byla zjištěna soukromá pole, která v rámci sestavení zjevně nejsou přístupná.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, odeberte pole nebo přidejte kód, který ji používá.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Je bezpečné potlačit upozornění tohoto pravidla.

## <a name="related-rules"></a>Související pravidla
 [CA1812: Vyhněte se nevytvořeným instancím vnitřních tříd](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

 [CA1801: Revize nepoužitých parametrů](../code-quality/ca1801-review-unused-parameters.md)

 [CA1804: Odeberte nepoužívané místní hodnoty](../code-quality/ca1804-remove-unused-locals.md)

 [CA1811: Vyhněte se nevolanému místnímu kódu](../code-quality/ca1811-avoid-uncalled-private-code.md)



