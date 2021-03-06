---
title: 'CA2207: Inicializujte vloženou hodnotu statických polí | Dokumentace Microsoftu'
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
- InitializeValueTypeStaticFieldsInline
- CA2207
helpviewer_keywords:
- CA2207
- InitializeValueTypeStaticFieldsInline
ms.assetid: d1ea9d8b-ecc2-46ca-86e2-c41dd0e76658
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0f90e52ed5d80c9b3e97415e920d7d6f4f0972fc
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902269"
---
# <a name="ca2207-initialize-value-type-static-fields-inline"></a>CA2207: Inicializujte vloženou hodnotu statických polí
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA2207: Inicializujte vloženou hodnotu statických polí](https://docs.microsoft.com/visualstudio/code-quality/ca2207-initialize-value-type-static-fields-inline).

|||
|-|-|
|TypeName|InitializeValueTypeStaticFieldsInline|
|CheckId|CA2207|
|Kategorie|Microsoft.Usage|
|Narušující změna|Pevné|

## <a name="cause"></a>příčina
 Hodnotový typ deklaruje explicitní statický konstruktor.

## <a name="rule-description"></a>Popis pravidla
 Při deklaraci value-type. při inicializaci výchozí, pokud všechna pole typu hodnoty jsou nastavené na hodnotu nula a všechna pole typu odkazu jsou nastaveny na `null` (`Nothing` v jazyce Visual Basic). Explicitní statický konstruktor je zaručeno, se spustí před konstruktor instance nebo volá statický člen typu. Proto pokud typ je vytvořen bez nutnosti volat konstruktor instance, statický konstruktor není zaručeno, že ke spuštění.

 Pokud všechna statická data je vložená inicializována a je deklarována bez explicitní statický konstruktor, kompilátory jazyků C# a Visual Basic přidejte `beforefieldinit` příznak do definice třídy jazyka MSIL. Kompilátory taky přidat privátní statický konstruktor, který obsahuje kód Statická inicializace. Tato privátní statický konstruktor se zaručeně spustí předtím, než jsou přístupné všechny statické pole typu.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li vyřešit porušení tohoto pravidla inicializujte všechna statická data, když je deklarovaný a statický konstruktor odeberte.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění na toto pravidlo.

## <a name="related-rules"></a>Související pravidla
 [CA1810: Inicializujte odkazový typ statického pole vloženě](../code-quality/ca1810-initialize-reference-type-static-fields-inline.md)



