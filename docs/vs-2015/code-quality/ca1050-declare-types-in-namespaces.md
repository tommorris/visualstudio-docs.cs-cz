---
title: 'CA1050: Deklarujte typy v oborech názvů | Dokumentace Microsoftu'
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
- CA1050
- DeclareTypesInNamespaces
helpviewer_keywords:
- DeclareTypesInNamespaces
- CA1050
ms.assetid: 1002748d-ac8d-404f-85dd-7a12d1ad3e05
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ef0559cc727e7ffd667ee72ebe241a958fa57450
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42900603"
---
# <a name="ca1050-declare-types-in-namespaces"></a>CA1050: Deklarujte typy v oborech názvů
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1050: deklarujte typy v oborech názvů](https://docs.microsoft.com/visualstudio/code-quality/ca1050-declare-types-in-namespaces).

|||
|-|-|
|TypeName|DeclareTypesInNamespaces|
|CheckId|CA1050|
|Kategorie|Microsoft.Design|
|Narušující změna|Narušující|

## <a name="cause"></a>příčina
 Veřejný nebo chráněný typ definovaný vně rozsahu pojmenovaného oboru názvů.

## <a name="rule-description"></a>Popis pravidla
 Typy jsou deklarovány v oborech názvů, aby se zabránilo kolize názvů a zároveň jako způsob organizace souvisejících typů v hierarchii objektů. Typy, které jsou mimo všechny pojmenovaného oboru názvů jsou v globálním oboru názvů, který se nedá odkazovat v kódu.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, umístěte typ v oboru názvů.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 I když si už nikdy nemusíte potlačit upozornění tohoto pravidla, je bezpečné k tomu, když sestavení nebude nikdy používat společně s ostatními sestaveními.

## <a name="example"></a>Příklad
 Následující příklad ukazuje knihovnu, která má typ nesprávně deklarované mimo obor názvů a typ, který má stejný název deklarovaný v oboru názvů.

 [!code-csharp[FxCop.Design.TypesLiveInNamespaces#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.TypesLiveInNamespaces/cs/FxCop.Design.TypesLiveInNamespaces.cs#1)]
 [!code-vb[FxCop.Design.TypesLiveInNamespaces#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.TypesLiveInNamespaces/vb/FxCop.Design.TypesLiveInNamespaces.vb#1)]

## <a name="example"></a>Příklad
 Následující aplikace používá knihovnu, která byla definována dříve. Všimněte si, že je vytvořen typ, který je deklarovaná mimo obor názvů, když název `Test` není kvalifikován pomocí oboru názvů. Všimněte si také, že pro přístup k `Test` zadejte `Goodspace`, vyžaduje se název oboru názvů.

 [!code-csharp[FxCop.Design.TestTypesLive#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.TestTypesLive/cs/FxCop.Design.TestTypesLive.cs#1)]
 [!code-vb[FxCop.Design.TestTypesLive#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.TestTypesLive/vb/FxCop.Design.TestTypesLive.vb#1)]



