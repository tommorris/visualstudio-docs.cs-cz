---
title: 'CA1300: Zadejte možnosti MessageBoxOptions | Dokumentace Microsoftu'
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
- SpecifyMessageBoxOptions
- CA1300
helpviewer_keywords:
- SpecifyMessageBoxOptions
- CA1300
ms.assetid: 9357a724-026e-4a3d-a03a-f14635064ec6
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bf2cf17b41248032caf01b0cfedbe9b70ecbefb2
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2018
ms.locfileid: "42902530"
---
# <a name="ca1300-specify-messageboxoptions"></a>CA1300: Zadejte možnosti MessageBoxOptions
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1300: Zadejte možnosti MessageBoxOptions](https://docs.microsoft.com/visualstudio/code-quality/ca1300-specify-messageboxoptions).

|||
|-|-|
|TypeName|SpecifyMessageBoxOptions|
|CheckId|CA1300|
|Kategorie|Microsoft.Globalization|
|Narušující změna|Nenarušující|

## <a name="cause"></a>příčina
 Metoda volá přetížení <xref:System.Windows.Forms.MessageBox.Show%2A?displayProperty=fullName> metodu, která se nedají <xref:System.Windows.Forms.MessageBoxOptions?displayProperty=fullName> argument.

## <a name="rule-description"></a>Popis pravidla
 Chcete-li zobrazit okno se zprávou správně pro jazykové verze, které používají pořadí čtení zprava doleva, <xref:System.Windows.Forms.MessageBoxOptions> a <xref:System.Windows.Forms.MessageBoxOptions> členy <xref:System.Windows.Forms.MessageBoxOptions> výčtu musí být předán <xref:System.Windows.Forms.MessageBox.Show%2A> – metoda. Zkontrolujte <xref:System.Windows.Forms.Control.RightToLeft%2A?displayProperty=fullName> vlastnost ovládacího prvku obsahujícího k určení, jestli se má použít pořadí čtení zprava doleva.

## <a name="how-to-fix-violations"></a>Jak vyřešit porušení
 Chcete-li opravit porušení tohoto pravidla, zavolejte přetížení <xref:System.Windows.Forms.MessageBox.Show%2A> metodu, která přebírá <xref:System.Windows.Forms.MessageBoxOptions> argument.

## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění
 Je bezpečné potlačit upozornění tohoto pravidla, když knihovny kódu nesmí být lokalizována pro jazykovou verzi, která používá pořadí čtení zprava doleva.

## <a name="example"></a>Příklad
 Následující příklad ukazuje metodu, která zobrazí okno se zprávou, která obsahuje možnosti, které jsou vhodné pro pořadí čtení jazykové verze. Soubor prostředků, který není zobrazený, je potřeba vytvořit příklad. Postupujte podle komentáře v příkladu, k vytvoření příkladu bez souboru prostředků a otestovat funkci zprava doleva.

 [!code-csharp[FxCop.Globalization.SpecifyMBOptions#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.SpecifyMBOptions/cs/FxCop.Globalization.SpecifyMBOptions.cs#1)]
 [!code-vb[FxCop.Globalization.SpecifyMBOptions#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Globalization.SpecifyMBOptions/vb/FxCop.Globalization.SpecifyMBOptions.vb#1)]

## <a name="see-also"></a>Viz také
 <xref:System.Resources.ResourceManager?displayProperty=fullName> [Prostředky v desktopových aplikacích](http://msdn.microsoft.com/library/8ad495d4-2941-40cf-bf64-e82e85825890)



