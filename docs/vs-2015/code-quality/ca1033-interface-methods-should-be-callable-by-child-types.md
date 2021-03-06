---
title: 'CA1033: Metody rozhraní by měla být volatelné podřízenými typy | Dokumentace Microsoftu'
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
- InterfaceMethodsShouldBeCallableByChildTypes
- CA1033
helpviewer_keywords:
- CA1033
- InterfaceMethodsShouldBeCallableByChildTypes
ms.assetid: 9f171497-a5e3-4769-a77b-7aed755b2662
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a71462661c577bebbd76e7fa05aeca9d613c4c23
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902583"
---
# <a name="ca1033-interface-methods-should-be-callable-by-child-types"></a>CA1033: Metody rozhraní by měla být volatelné podřízenými typy
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1033: metody rozhraní by měla být volatelné podřízenými typy](https://docs.microsoft.com/visualstudio/code-quality/ca1033-interface-methods-should-be-callable-by-child-types).

|||
|-|-|
|TypeName|InterfaceMethodsShouldBeCallableByChildTypes|
|CheckId|CA1033|
|Kategorie|Microsoft.Design|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Nezapečetěný externě viditelný typ poskytuje explicitní implementaci metod veřejného rozhraní a neposkytuje alternativní externě viditelnou metodu stejného názvu.

## <a name="rule-description"></a>Popis pravidla
 Vezměte v úvahu základní typ, který explicitně implementuje metodu veřejných rozhraní. Typ, který se odvozuje od základního typu má přístup k zděděné metody pouze prostřednictvím odkaz na aktuální instanci (`this` v jazyce C#), který je přetypován na rozhraní. Pokud odvozený typ (explicitně) znovu implementuje metodu rozhraní zděděná, lze přistupovat už základní implementaci. Vyvolá odvozené provádění; volání prostřednictvím odkazu na aktuální instanci To způsobí, že rekurze a přetečení zásobníku konečný výsledek.

 Toto pravidlo nevytváří sestavu porušení pro explicitní implementaci <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> při externě viditelného `Close()` nebo `System.IDisposable.Dispose(Boolean)` metoda je k dispozici.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, implementovat novou metodu, která poskytuje stejné funkce a je viditelná pro odvozené typy nebo změňte implicitními implementace. Pokud k zásadní změně je přijatelné, alternativou je učiňte typ zapečetěná.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Je bezpečné potlačit upozornění tohoto pravidla, pokud je externě viditelná metoda, která má stejné funkce, ale jiný název než explicitně implementované metody.

## <a name="example"></a>Příklad
 Následující příklad ukazuje typ, `ViolatingBase`, který porušuje pravidla a typ, `FixedBase`, která zobrazuje oprava porušení zásady.

 [!code-csharp[FxCop.Design.ExplicitMethodImplementations#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ExplicitMethodImplementations/cs/FxCop.Design.ExplicitMethodImplementations.cs#1)]

## <a name="see-also"></a>Viz také
 [Rozhraní](http://msdn.microsoft.com/library/2feda177-ce11-432d-81b4-d50f5f35fd37)



