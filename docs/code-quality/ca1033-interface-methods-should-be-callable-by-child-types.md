---
title: "CA1033: Metody rozhraní by měla být volatelné podřízenými typy | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- InterfaceMethodsShouldBeCallableByChildTypes
- CA1033
helpviewer_keywords:
- CA1033
- InterfaceMethodsShouldBeCallableByChildTypes
ms.assetid: 9f171497-a5e3-4769-a77b-7aed755b2662
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4694e1dbcbcf541b502edbe5f2520229ee33f4a6
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="ca1033-interface-methods-should-be-callable-by-child-types"></a>CA1033: Metody rozhraní by měla být volatelné podřízenými typy
|||  
|-|-|  
|TypeName|InterfaceMethodsShouldBeCallableByChildTypes|  
|CheckId|CA1033|  
|Kategorie|Microsoft.Design|  
|Narušující změna|Nenarušující|  
  
## <a name="cause"></a>příčina  
 Nezapečetěný externě viditelný typ poskytuje explicitní implementaci metod veřejného rozhraní a neposkytuje alternativní externě viditelnou metodu stejného názvu.  
  
## <a name="rule-description"></a>Popis pravidla  
 Vezměte v úvahu základní typ, který explicitně implementuje metodu veřejné rozhraní. Typ, který je odvozena ze základního typu mají přístup k metodě zděděné rozhraní pouze prostřednictvím odkaz na aktuální instanci (`this` v jazyce C#), je převést na rozhraní. Odvozený typ (explicitně) znovu implementuje metodu zděděné rozhraní, můžete již použít základní implementaci. Provolání odkaz na aktuální instanci vyvolá odvozené implementace; To způsobí, že rekurze a případné zásobníku přetečení.  
  
 Toto pravidlo nevytváří sestavu narušení explicitní implementace <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> při externě viditelné `Close()` nebo `System.IDisposable.Dispose(Boolean)` metoda je k dispozici.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Opravit porušení toto pravidlo, implementovat nový metodu, která zpřístupňuje stejné funkce a je viditelná pro odvozené typy nebo změnit implicitními implementaci. Pokud narušující změně je přijatelné, alternativou je k vytvoření typu zapečetěná.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Je bezpečné potlačit upozornění na toto pravidlo, je-li metodu externě viditelné je zadaný, který má stejnou funkci ale jiný název než – explicitně implementovaná metoda.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje typu, `ViolatingBase`, která porušuje pravidlo a typu, `FixedBase`, který ukazuje oprava porušení zásady.  
  
 [!code-csharp[FxCop.Design.ExplicitMethodImplementations#1](../code-quality/codesnippet/CSharp/ca1033-interface-methods-should-be-callable-by-child-types_1.cs)]  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní](/dotnet/csharp/programming-guide/interfaces/index)