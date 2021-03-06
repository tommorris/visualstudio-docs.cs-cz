---
title: 'CA1058: Typy by neměly rozšířit určité základní typy | Dokumentace Microsoftu'
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
- TypesShouldNotExtendCertainBaseTypes
- CA1058
helpviewer_keywords:
- CA1058
- TypesShouldNotExtendCertainBaseTypes
ms.assetid: 8446ee40-beb1-49fa-8733-4d8e813471c0
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: d4eb5b13813ca8bf06a64c638f399186a88a17c4
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42900868"
---
# <a name="ca1058-types-should-not-extend-certain-base-types"></a>CA1058: Typy by neměly rozšířit určité základní typy
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1058: typy by neměly rozšířit určité základní typy](https://docs.microsoft.com/visualstudio/code-quality/ca1058-types-should-not-extend-certain-base-types).

|||
|-|-|
|TypeName|TypesShouldNotExtendCertainBaseTypes|
|CheckId|CA1058|
|Kategorie|Microsoft.Design|
|Narušující změna|Narušující|

## <a name="cause"></a>příčina
 Externě viditelný typ rozšiřuje určité základní typy. Toto pravidlo v současné době sestavy typy, které jsou odvozeny z následujících typů:

-   <xref:System.ApplicationException?displayProperty=fullName>

-   <xref:System.Xml.XmlDocument?displayProperty=fullName>

-   <xref:System.Collections.CollectionBase?displayProperty=fullName>

-   <xref:System.Collections.DictionaryBase?displayProperty=fullName>

-   <xref:System.Collections.Queue?displayProperty=fullName>

-   <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>

-   <xref:System.Collections.SortedList?displayProperty=fullName>

-   <xref:System.Collections.Stack?displayProperty=fullName>

## <a name="rule-description"></a>Popis pravidla
 Pro [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] verze 1 se doporučuje k odvození nové výjimky z <xref:System.ApplicationException>. Došlo ke změně doporučení a nové výjimky musí být odvozený z: <xref:System.Exception?displayProperty=fullName> nebo jeden z jejích podtříd v <xref:System> oboru názvů.

 Nelze vytvořit podtřídu <xref:System.Xml.XmlDocument> Pokud budete chtít vytvořit zobrazení základní objekt model nebo zdroj dat XML.

### <a name="non-generic-collections"></a>Obecné kolekce
 Použít a/nebo rozšířit obecných kolekcí, kdykoli je to možné. Pokud dříve dodán se netýkají obecné kolekce ve vašem kódu.

 **Příklady nesprávné použití**

```csharp
public class MyCollection : CollectionBase
{
}

public class MyReadOnlyCollection : ReadOnlyCollectionBase
{
}
```

 **Příklady správné použití**

```csharp
public class MyCollection : Collection<T>
{
}

public class MyReadOnlyCollection : ReadOnlyCollection<T>
{
}
```

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, odvodit typ z různých základního typu nebo obecné kolekce.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění tohoto pravidla pro porušení o <xref:System.ApplicationException>. Je bezpečné potlačit upozornění tohoto pravidla pro porušení o <xref:System.Xml.XmlDocument>. Je bezpečné pro potlačení varování týkající se obecné kolekce, pokud kód byla vydána dříve.



