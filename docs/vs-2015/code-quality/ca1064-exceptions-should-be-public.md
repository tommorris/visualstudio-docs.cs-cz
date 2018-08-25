---
title: 'CA1064: Výjimky by měly být veřejné | Dokumentace Microsoftu'
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
- CA1064
- ExceptionsShouldBePublic
helpviewer_keywords:
- ExceptionsShouldBePublic
- CA1064
ms.assetid: 83eb224c-2456-4368-acf4-3b3378e67759
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 7a40a832ddd9342896105c6c1ede8fdcbf2266a9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674508"
---
# <a name="ca1064-exceptions-should-be-public"></a>CA1064: Výjimky by měly být veřejné
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1064: výjimky by měly být veřejné](https://docs.microsoft.com/visualstudio/code-quality/ca1064-exceptions-should-be-public).  
  
TypeName | ExceptionsShouldBePublic |  
| ID kontroly | CA1064 |  
| Kategorie | Microsoft.Design|  
| Zásadní změna | Bez zásadní |  
  
## <a name="cause"></a>příčina  
 Neveřejné výjimka je odvozena přímo z <xref:System.Exception>, <xref:System.SystemException>, nebo <xref:System.ApplicationException>.  
  
## <a name="rule-description"></a>Popis pravidla  
 Interní výjimka je jenom viditelné uvnitř svého vlastního vnitřního rozsahu. Jakmile výjimka přesáhne hranice vnitřního rozsahu, lze pro zachycení výjimky použít pouze základní výjimku. Pokud je vnitřní výjimka zděděna z <xref:System.Exception>, <xref:System.SystemException>, nebo <xref:System.ApplicationException>, externí kód nebude mít dostatečné informace o tom, co dělat, s výjimkou.  
  
 Ale pokud kód má veřejnou výjimek, který později slouží jako základ pro vnitřní výjimku, je možné logicky předpokládat, že kód dál si budete moct udělat něco inteligentní s základní výjimku. Veřejné výjimka bude mít více informací, než co poskytují T:System.Exception, T:System.SystemException nebo T:System.ApplicationException.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Zveřejněte výjimku nebo odvozovat vnitřní výjimka z veřejné výjimka, která není <xref:System.Exception>, <xref:System.SystemException>, nebo <xref:System.ApplicationException>.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Potlačí zprávy z tohoto pravidla, pokud máte jistotu, že ve všech případech, že privátní výjimka bude zachycena v rámci svého vlastního vnitřního rozsahu.  
  
## <a name="example"></a>Příklad  
 Toto pravidlo je vyvoláno na první příklad metody FirstCustomException, protože třída výjimky je odvozena přímo z výjimky a je interní. Toto pravidlo ve třídě SecondCustomException neaktivuje, protože i když třída je odvozena přímo z výjimky, třída je deklarována jako veřejné. Třída třetí také neaktivuje pravidla vzhledem k tomu, že není odvozena přímo z <xref:System.Exception?displayProperty=fullName>, <xref:System.SystemException?displayProperty=fullName>, nebo <xref:System.ApplicationException?displayProperty=fullName>.  
  
 [!code-csharp[FxCop.Design.ExceptionsShouldBePublic.CA1064#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.design.exceptionsshouldbepublic.ca1064/cs/ca1064 - exceptionsshouldbepublic.cs#1)]


