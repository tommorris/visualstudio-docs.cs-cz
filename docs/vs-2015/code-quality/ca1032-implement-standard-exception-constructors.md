---
title: 'CA1032: Implementujte standardní konstruktory výjimky | Dokumentace Microsoftu'
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
- CA1032
- ImplementStandardExceptionConstructors
helpviewer_keywords:
- CA1032
- ImplementStandardExceptionConstructors
ms.assetid: a8623c56-273a-4c95-8d83-95911a042be7
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a77237f40b8d485b053e4ccbd57f92e275ed653c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666919"
---
# <a name="ca1032-implement-standard-exception-constructors"></a>CA1032: Implementujte standardní konstruktory výjimky
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1032: implementujte standardní konstruktory výjimky](https://docs.microsoft.com/visualstudio/code-quality/ca1032-implement-standard-exception-constructors).  
  
TypeName | ImplementStandardExceptionConstructors |  
| ID kontroly | CA1032 |  
| Kategorie | Microsoft.Design|  
| Zásadní změna | Ukončování bez |  
  
## <a name="cause"></a>příčina  
 Typ rozšiřuje <xref:System.Exception?displayProperty=fullName> a deklaruje všechny požadované konstruktory.  
  
## <a name="rule-description"></a>Popis pravidla  
 Typy výjimek musí implementovat následujících konstruktorů:  
  
-   veřejné NewException()  
  
-   veřejné NewException(string)  
  
-   veřejné NewException (string, výjimka)  
  
-   chráněná nebo privátní NewException (SerializationInfo, StreamingContext)  
  
 Není-li dodána úplná sada konstruktorů, může být obtížné správně ošetřit výjimky. Například konstruktor, který nemá podpis `NewException(string, Exception)` slouží k vytvoření výjimky, které jsou způsobeny další výjimky. Bez tento konstruktor nelze vytvořit a výjimku instance vlastní výjimky, která obsahuje vnitřní (vnořené) výjimku, což je spravovaný kód by měl provést v takové situaci. První tři výjimka konstruktory jsou veřejné konvencí. Čtvrtý konstruktor je chráněný v nezapečetěné třídy a soukromý v třídách sealed. Další informace najdete v tématu [CA2229: implementovat Serializační konstruktory](../code-quality/ca2229-implement-serialization-constructors.md)  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Chcete-li opravit porušení tohoto pravidla, přidejte chybějící konstruktory s výjimkou a ujistěte se, že mají správnou usnadnění.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Je bezpečné potlačit upozornění tohoto pravidla při porušení zásad je způsobena použitím úroveň různý přístup pro veřejné konstruktory.  
  
## <a name="example"></a>Příklad  
 Následující příklad obsahuje typ výjimky, která porušuje pravidlo a typ výjimky, která je implementována správně.  
  
 [!code-csharp[FxCop.Design.ExceptionMultipleCtors#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.ExceptionMultipleCtors/cs/FxCop.Design.ExceptionMultipleCtors.cs#1)]


