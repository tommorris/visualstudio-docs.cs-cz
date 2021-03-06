---
title: 'CA2111: Ukazatelé by neměli být viditelné | Dokumentace Microsoftu'
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
- PointersShouldNotBeVisible
- CA2111
helpviewer_keywords:
- CA2111
- PointersShouldNotBeVisible
ms.assetid: b3a8d466-895b-43bc-a2df-5d7058fe915f
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 512d253a4e6cf4d8c92f7091d96cc747a667a646
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42901905"
---
# <a name="ca2111-pointers-should-not-be-visible"></a>CA2111: Ukazatelé by neměli být viditelné
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA2111: ukazatelé by neměli být viditelné](https://docs.microsoft.com/visualstudio/code-quality/ca2111-pointers-should-not-be-visible).

|||
|-|-|
|TypeName|PointersShouldNotBeVisible|
|CheckId|CA2111|
|Kategorie|Microsoft.Security|
|Narušující změna|Narušující|

## <a name="cause"></a>příčina
 Veřejný nebo chráněný <xref:System.IntPtr?displayProperty=fullName> nebo <xref:System.UIntPtr?displayProperty=fullName> pole není jen pro čtení.

## <a name="rule-description"></a>Popis pravidla
 <xref:System.IntPtr> a <xref:System.UIntPtr> jsou typy ukazatelů, které se používají pro přístup k nespravované paměti. Pokud ukazatel není soukromý, interní nebo jen pro čtení, škodlivý kód může změnit hodnotu ukazatele, potenciálně umožňuje přístup k libovolného umístění v paměti nebo může způsobit selhání aplikace nebo systému.

 Pokud máte v úmyslu zabezpečený přístup k typu, který obsahuje pole, ukazatel, přečtěte si téma [CA2112: zabezpečené typy by neměly vystavovat pole](../code-quality/ca2112-secured-types-should-not-expose-fields.md).

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Ukazatel Zabezpečte tím, že je jen pro čtení, interní nebo privátní.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Potlačit upozornění tohoto pravidla, pokud nelze spoléhat na hodnotu ukazatele.

## <a name="example"></a>Příklad
 Následující kód ukazuje ukazatele, které porušují a splňovat pravidla. Všimněte si, že nesoukromých ukazatelů také porušovat pravidla [CA1051: nedeklarujte viditelná pole instance](../code-quality/ca1051-do-not-declare-visible-instance-fields.md).

 [!code-csharp[FxCop.Security.PointersArePrivate#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.PointersArePrivate/cs/FxCop.Security.PointersArePrivate.cs#1)]

## <a name="related-rules"></a>Související pravidla
 [CA2112: Zabezpečené typy by neměly vystavovat pole](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

 [CA1051: Nedeklarujte viditelná pole instance](../code-quality/ca1051-do-not-declare-visible-instance-fields.md)

## <a name="see-also"></a>Viz také
 <xref:System.IntPtr?displayProperty=fullName><xref:System.UIntPtr?displayProperty=fullName>



