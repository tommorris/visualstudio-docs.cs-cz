---
title: 'CA2204: Literály by měly být zadány správně | Dokumentace Microsoftu'
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
- Literals should be spelled correctly
- CA2204
- LiteralsShouldBeSpelledCorrectly
helpviewer_keywords:
- CA2204
ms.assetid: b0bbcbb6-c92d-4c14-8ef7-9c8b38c791a6
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 39d841fbfa9be3e3ee5764e986a9688ca4113caf
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902380"
---
# <a name="ca2204-literals-should-be-spelled-correctly"></a>CA2204: Literály by měly být zadány správně
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA2204: literály by měly být zadány správně](https://docs.microsoft.com/visualstudio/code-quality/ca2204-literals-should-be-spelled-correctly).

|||
|-|-|
|TypeName|LiteralsShouldBeSpelledCorrectly|
|CheckId|CA2204|
|Kategorie|Microsoft.Usage|
|Narušující změna|Pevné|

## <a name="cause"></a>příčina
 Metoda předává řetězcový literál, který se používá v parametru nebo vlastnost, která vyžaduje lokalizovaný řetězec a řetězcový literál obsahuje jedno nebo více slov, která knihovna kontroly pravopisu společnosti Microsoft nerozpoznala.

## <a name="rule-description"></a>Popis pravidla
 Toto pravidlo zkontroluje řetězcový literál, který je předán jako hodnotu parametru nebo vlastnost, pokud jeden nebo více z následujících případech má hodnotu true:

-   <xref:System.ComponentModel.LocalizableAttribute> Atribut parametru nebo vlastnosti je nastaven na hodnotu true.

-   Název parametru nebo vlastnosti obsahuje "Text", "Zpráva" nebo "Popisu".

-   Název parametru řetězce, který se předá metodě Console.Write nebo Console.WriteLine je "value" nebo "format".

 Toto pravidlo analyzuje řetězcový literál do slov, tokenizací složených slov a zkontroluje pravopis pro každé slovo/token. Informace o analýze algoritmus, najdete v části [CA1704: identifikátory by měly být zadány správně](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

 Ve výchozím nastavení je použít nástroj pro kontrolu pravopisu verze Angličtina (en).

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, opravte pravopis slova nebo přidejte slovo do vlastního slovníku. Informace o tom, jak použít vlastní slovníky najdete v tématu [postupy: přizpůsobení slovníku analýzy kódu](../code-quality/how-to-customize-the-code-analysis-dictionary.md).

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění na toto pravidlo. Správně hláskovaným slov snížit učit se vyžaduje pro nové knihovny softwaru.

## <a name="related-rules"></a>Související pravidla
 [CA1704: Identifikátory by měly být zadány správně](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)

 [CA1703: Řetězce prostředků by měly být zadány správně](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)



