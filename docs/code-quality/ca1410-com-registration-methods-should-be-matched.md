---
title: 'CA1410: Metody registrace modelu COM by si měly odpovídat'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1410
- ComRegistrationMethodsShouldBeMatched
helpviewer_keywords:
- CA1410
- ComRegistrationMethodsShouldBeMatched
ms.assetid: f3b2e62d-fd66-4093-9f0c-dba01ad995fd
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 1d4cbff52a5b5b5ef5fc46ef0b2f93926f097485
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2018
ms.locfileid: "45550886"
---
# <a name="ca1410-com-registration-methods-should-be-matched"></a>CA1410: Metody registrace modelu COM by si měly odpovídat

|||
|-|-|
|TypeName|ComRegistrationMethodsShouldBeMatched|
|CheckId|CA1410|
|Kategorie|Microsoft.Interoperability|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Typ deklaruje metodu, která je označena <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> atribut, ale nedeklaruje metodu označenou atributem <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName> atribut, nebo naopak.

## <a name="rule-description"></a>Popis pravidla
 Pro klienty modelu COM (Component Object) k vytvoření [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] typ, typ musí být nejprve registrována. Pokud je k dispozici, metodu, která je označena <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute> atribut je volána v průběhu procesu registrace ke spouštění kódu zadaného uživatelem. Odpovídající metodu označenou atributem <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute> atribut je volána v průběhu procesu zrušení registrace operací metoda registrace.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, přidejte odpovídající registraci nebo zrušení registrace metody.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění na toto pravidlo.

## <a name="example"></a>Příklad
 Následující příklad ukazuje typ, který porušuje pravidla. Komentářem kódu ukazuje oprava porušení zásady.

 [!code-csharp[FxCop.Interoperability.ComRegistration#1](../code-quality/codesnippet/CSharp/ca1410-com-registration-methods-should-be-matched_1.cs)]
 [!code-vb[FxCop.Interoperability.ComRegistration#1](../code-quality/codesnippet/VisualBasic/ca1410-com-registration-methods-should-be-matched_1.vb)]

## <a name="related-rules"></a>Související pravidla
 [CA1411: Metody registrace modelu COM by neměly být viditelné](../code-quality/ca1411-com-registration-methods-should-not-be-visible.md)

## <a name="see-also"></a>Viz také:

- <xref:System.Runtime.InteropServices.RegistrationServices?displayProperty=fullName>
- [Registrování sestav pomocí modelu COM](/dotnet/framework/interop/registering-assemblies-with-com)
- [Regasm.exe (nástroj registrace sestavení)](/dotnet/framework/tools/regasm-exe-assembly-registration-tool)