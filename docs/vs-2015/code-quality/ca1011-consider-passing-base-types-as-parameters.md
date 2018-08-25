---
title: 'CA1011: Zvažte předání základních typů jako parametrů | Dokumentace Microsoftu'
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
- ConsiderPassingBaseTypesAsParameters
- CA1011
helpviewer_keywords:
- CA1011
- ConsiderPassingBaseTypesAsParameters
ms.assetid: ce1e1241-dcf4-419b-9363-1d5bc4989279
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: aa1cfd44b80757d0cf24dbab16b5e8f982eca551
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629327"
---
# <a name="ca1011-consider-passing-base-types-as-parameters"></a>CA1011: Zvažte předání základních typů jako parametrů
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1011: Zvažte předání základních typů jako parametrů](https://docs.microsoft.com/visualstudio/code-quality/ca1011-consider-passing-base-types-as-parameters).  
  
TypeName | ConsiderPassingBaseTypesAsParameters |  
| ID kontroly | CA1011 |  
| Kategorie | Microsoft.Design|  
| Zásadní změna | Zásadní |  
  
## <a name="cause"></a>příčina  
 Deklarace metody obsahuje formální parametr, který je odvozený typ a metodu volá pouze členy základního typu parametru.  
  
## <a name="rule-description"></a>Popis pravidla  
 Je-li v deklaraci metody zadán jako parametr základní typ, lze jako příslušný argument k metodě předat kterýkoliv typ odvozený z tohoto základního typu. Pokud argument je použit uvnitř těla metody, konkrétní metody, která se spustí záviset na typu argumentu. Pokud je další funkce, která je poskytována odvozený typ není vyžadována, umožňuje použití základního typu širší využití metody.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Chcete-li opravit porušení tohoto pravidla, změňte na jeho základní typ typu parametru.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Je bezpečné potlačit upozornění tohoto pravidla  
  
-   Pokud metoda vyžaduje konkrétní funkce, která je poskytována odvozený typ  
  
     \- nebo –  
  
-   k vynucení pouze odvozený typ, nebo více odvozeného typu, je předán metodě.  
  
 V takových případech bude kód robustnější kvůli silný typ kontroly, které poskytuje kompilátoru a modulu runtime.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje metodu, `ManipulateFileStream`, který jde použít jenom s <xref:System.IO.FileStream> objektu, který porušuje tato pravidla. Druhá metoda `ManipulateAnyStream`, splňuje pravidlo tak, že nahradíte <xref:System.IO.FileStream> parametr pomocí <xref:System.IO.Stream>.  
  
 [!code-cpp[FxCop.Design.ConsiderPassingBaseTypes#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.ConsiderPassingBaseTypes/cpp/FxCop.Design.ConsiderPassingBaseTypes.cpp#1)]
 [!code-csharp[FxCop.Design.ConsiderPassingBaseTypes#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ConsiderPassingBaseTypes/cs/FxCop.Design.ConsiderPassingBaseTypes.cs#1)]
 [!code-vb[FxCop.Design.ConsiderPassingBaseTypes#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.ConsiderPassingBaseTypes/vb/FxCop.Design.ConsiderPassingBaseTypes.vb#1)]  
  
## <a name="related-rules"></a>Související pravidla  
 [CA1059: Členové by neměli zveřejňovat určité konkrétní typy](../code-quality/ca1059-members-should-not-expose-certain-concrete-types.md)


