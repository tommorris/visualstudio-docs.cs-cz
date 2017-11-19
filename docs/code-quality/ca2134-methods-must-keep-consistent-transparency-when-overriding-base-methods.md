---
title: "CA2134: Metody musí zachovávat konzistentní transparentnost, při přepisování základních metod | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CA2134
ms.assetid: 3b17e487-0326-442e-90e1-dc0ba9cdd3f2
caps.latest.revision: "9"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: feb33e630322237522c98ff3f803bc44b3fbcc86
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods"></a>CA2134: Metody musejí při přepisování základních metod zachovávat konzistentní transparentnost
|||  
|-|-|  
|TypeName|MethodsMustOverrideWithConsistentTransparency|  
|CheckId|CA2134|  
|Kategorie|Microsoft.Security|  
|Narušující změna|Narušující|  
  
## <a name="cause"></a>příčina  
 Toto pravidlo aktivuje se v případě metody označené jako <xref:System.Security.SecurityCriticalAttribute> přepíše metodu, která je transparentní nebo označené s <xref:System.Security.SecuritySafeCriticalAttribute>. Pravidlo také aktivuje se v případě metodu, která je transparentní nebo označené s <xref:System.Security.SecuritySafeCriticalAttribute> přepíše metodu, která je označena <xref:System.Security.SecurityCriticalAttribute>.  
  
 Pravidlo je použito při přepisování virtuální metody nebo implementaci rozhraní.  
  
## <a name="rule-description"></a>Popis pravidla  
 Toto pravidlo aktivuje na pokusy o změnu usnadnění zabezpečení metody další řetězem dědičnosti. Například pokud je virtuální metoda v základní třídě průhledných nebo kritická, pak odvozené třídy musí přepsat pomocí metody průhledných nebo kritická. Naopak pokud virtuální kritické pro zabezpečení, odvozené třídy musí přepsat pomocí metody kritické zabezpečení. Totéž platí pro implementaci metody rozhraní.  
  
 Nevynutí se průhlednost pravidla, pokud kód je JIT zkompilovat místo v době běhu tak, aby výpočtu průhlednost neobsahuje informace o dynamickém typu. Výsledek výpočtu průhlednost proto musí být možné určit výhradně z statické typy probíhá kompilována, bez ohledu na typ dynamické.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Opravit porušení toto pravidlo, změňte průhlednost metody, která je přepsání virtuální metody nebo implementace rozhraní tak, aby odpovídaly průhlednost virtuální nebo metodu rozhraní.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Není potlačení upozornění od tohoto pravidla. Porušení tohoto pravidla způsobí runtime <xref:System.TypeLoadException> pro sestavení, které používají průhlednost úrovně 2.  
  
## <a name="examples"></a>Příklady  
  
### <a name="code"></a>Kód  
 [!code-csharp[FxCop.Security.CA2134.MethodsMustOverrideWithConsistentTransparency#1](../code-quality/codesnippet/CSharp/ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods_1.cs)]  
  
## <a name="see-also"></a>Viz také  
 [Kód transparentní pro zabezpečení, úroveň 2](http://msdn.microsoft.com/Library/4d05610a-0da6-4f08-acea-d54c9d6143c0)