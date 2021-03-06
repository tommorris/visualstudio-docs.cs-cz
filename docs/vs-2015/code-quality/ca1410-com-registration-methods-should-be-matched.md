---
title: 'CA1410: Metody registrace modelu COM by si měly odpovídat | Dokumentace Microsoftu'
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
- CA1410
- ComRegistrationMethodsShouldBeMatched
helpviewer_keywords:
- CA1410
- ComRegistrationMethodsShouldBeMatched
ms.assetid: f3b2e62d-fd66-4093-9f0c-dba01ad995fd
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e7b21b7afc6c422cf77a920fd7abb3d3fbfb2193
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902854"
---
# <a name="ca1410-com-registration-methods-should-be-matched"></a>CA1410: Metody registrace modelu COM by si měly odpovídat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1410: metody registrace modelu COM by si měly odpovídat](https://docs.microsoft.com/visualstudio/code-quality/ca1410-com-registration-methods-should-be-matched).

|||
|-|-|
|TypeName|ComRegistrationMethodsShouldBeMatched|
|CheckId|CA1410|
|Kategorie|Microsoft.Interoperability|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Typ deklaruje metodu, která je označena <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> atribut, ale nedeklaruje metodu označenou atributem <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName> atribut, nebo naopak.

## <a name="rule-description"></a>Popis pravidla
 Pro klienty modelu COM (Component Object) k vytvoření [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] typ, typ musí být nejprve registrována. Pokud je k dispozici, metodu, která je označena <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute> atribut je volána v průběhu procesu registrace ke spouštění kódu zadaného uživatelem. Odpovídající metodu označenou atributem <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute> atribut je volána v průběhu procesu zrušení registrace operací metoda registrace.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, přidejte odpovídající registraci nebo zrušení registrace metody.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění na toto pravidlo.

## <a name="example"></a>Příklad
 Následující příklad ukazuje typ, který porušuje pravidla. Komentářem kódu ukazuje oprava porušení zásady.

 [!code-csharp[FxCop.Interoperability.ComRegistration#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.ComRegistration/cs/FxCop.Interoperability.ComRegistration.cs#1)]
 [!code-vb[FxCop.Interoperability.ComRegistration#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.ComRegistration/vb/FxCop.Interoperability.ComRegistration.vb#1)]

## <a name="related-rules"></a>Související pravidla
 [CA1411: Metody registrace modelu COM by neměly být viditelné](../code-quality/ca1411-com-registration-methods-should-not-be-visible.md)

## <a name="see-also"></a>Viz také
 <xref:System.Runtime.InteropServices.RegistrationServices?displayProperty=fullName> [Registrování sestav pomocí modelu COM](http://msdn.microsoft.com/library/87925795-a3ae-4833-b138-125413478551) [Regasm.exe (Nástroj registrace sestavení)](http://msdn.microsoft.com/library/e190e342-36ef-4651-a0b4-0e8c2c0281cb)



