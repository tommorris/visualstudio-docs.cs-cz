---
title: 'CA1400: Vstupní body nespravovaného kódu by měly existovat. | Dokumentace Microsoftu'
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
- CA1400
- PInvokeEntryPointsShouldExist
helpviewer_keywords:
- PInvokeEntryPointsShouldExist
- CA1400
ms.assetid: 1d64e470-7b2f-4cca-8fb0-ac92829e6332
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0544fb21533e3f114ab1efdc315d844b4cad0acb
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902728"
---
# <a name="ca1400-pinvoke-entry-points-should-exist"></a>CA1400: Vstupní body volání nespravovaného kódu by měly existovat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1400: vstupní body nespravovaného kódu by měla existovat](https://docs.microsoft.com/visualstudio/code-quality/ca1400-p-invoke-entry-points-should-exist).

|||
|-|-|
|TypeName|PInvokeEntryPointsShouldExist|
|CheckId|CA1400|
|Kategorie|Microsoft.Interoperability|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Veřejná nebo chráněná metoda je označena <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>. Nespravovanou knihovnu nelze nalézt nebo nelze metodu porovnat s funkcí v knihovně. Pokud pravidlo nemůže najít název metody, přesně tak, jak je zadaný, hledá ANSI nebo širokoznaké verze metody přidáním přípony názvu metody název "A" nebo "W". Pokud není nalezena žádná shoda, pravidlo se pokusí najít funkci s použitím __stdcall formát názvu (_MyMethod@12, kde 12 představuje délku argumenty). Pokud není nalezena žádná shoda, a název metody, který začíná na "#", toto pravidlo vyhledá funkce jako odkaz na pořadovém místě místo odkazu na název.

## <a name="rule-description"></a>Popis pravidla
 Žádná kontrola v době kompilace je k dispozici, ujistěte se, že metody, které jsou označené <xref:System.Runtime.InteropServices.DllImportAttribute> jsou umístěny v odkazované nespravované knihovně DLL. Pokud žádná funkce, který má zadaný název je v knihovně nebo argumenty metody se neshodují s argumenty funkce, modul common language runtime vyvolá výjimku.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, opravte metodu, která má <xref:System.Runtime.InteropServices.DllImportAttribute> atribut. Ujistěte se, že nespravované knihovny existuje a je ve stejném adresáři jako sestavení, který obsahuje metodu. Pokud knihovna je k dispozici a správně odkazované, ověřte, jestli název metody, návratový typ a podpisu argumentu odpovídají funkce knihovny.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Nepotlačujte upozornění tohoto pravidla, pokud nespravovaná knihovna je ve stejném adresáři jako spravovaná sestavení, která na něj odkazuje. Může být bezpečné pro potlačení upozornění tohoto pravidla v případě, kdy nespravovanou knihovnu nelze nalézt.

## <a name="example"></a>Příklad
 Následující příklad ukazuje typ, který porušuje pravidla. Žádná funkce s názvem `DoSomethingUnmanaged` vyvolá se v souboru kernel32.dll.

 [!code-csharp[FxCop.Interoperability.DLLExists#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.DLLExists/cs/FxCop.Interoperability.DLLExists.cs#1)]

## <a name="see-also"></a>Viz také
 <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>



