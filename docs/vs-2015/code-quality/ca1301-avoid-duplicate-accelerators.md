---
title: 'CA1301: Vyhněte se duplicitním akcelerátorům | Dokumentace Microsoftu'
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
- CA1301
- AvoidDuplicateAccelerators
helpviewer_keywords:
- CA1301
- AvoidDuplicateAccelerators
ms.assetid: 20570a00-864b-459c-a1fa-a6e9db5f1001
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 29fc1fbaee9114cf4fde8ab012301e487abe33ae
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670991"
---
# <a name="ca1301-avoid-duplicate-accelerators"></a>CA1301: Vyhněte se duplicitním akcelerátorům
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA1301: Vyhněte se duplicitním akcelerátorům](https://docs.microsoft.com/visualstudio/code-quality/ca1301-avoid-duplicate-accelerators).  
  
TypeName | AvoidDuplicateAccelerators |  
| ID kontroly | CA1301 |  
| Kategorie | Microsoft.Globalization|  
| Zásadní změna | Ukončování bez |  
  
## <a name="cause"></a>příčina  
 Typ rozšiřuje <xref:System.Windows.Forms.Control?displayProperty=fullName> a obsahuje dva nebo více nejvyšší úrovně ovládacích prvků, které mají stejné přístupové klíče, které jsou uloženy do souboru prostředků.  
  
## <a name="rule-description"></a>Popis pravidla  
 Přístupová klávesa neboli akcelerátor umožňuje klávesnici přístup k ovládacímu prvku pomocí klávesy ALT. Když má více ovládacích prvků duplicitní přístupové klávesy, není chování přístupové klávesy dobře definováno. Uživatel nemusí být možné získat přístup k odpovídající ovládací prvek pomocí přístupového klíče a ovládací prvek než ten, který je určený může být povolený.  
  
 Aktuální implementace tohoto pravidla ignoruje položky nabídky. Položky nabídky v podnabídce stejné ale by neměly mít identické přístupové klíče.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Chcete-li opravit porušení tohoto pravidla, definujte jedinečné přístupových klíčů pro všechny ovládací prvky.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Nepotlačujte upozornění na toto pravidlo.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje minimální formulář, který obsahuje dva ovládací prvky, které mají stejné přístupové klíče. Klíče jsou uložené v souboru prostředků, který není zobrazen; jejich hodnoty se však zobrazí ve komentářem si `checkBox.Text` řádky. Chování duplicitním akcelerátorům se dají prozkoumat výměnou `checkBox.Text` řádky s jejich protějšky komentářem navýšení kapacity. Ale v takovém případě příklad nebude generovat upozornění z pravidla.  
  
 [!code-csharp[FxCop.Globalization.AvoidDuplicateAccels#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.AvoidDuplicateAccels/cs/FxCop.Globalization.AvoidDuplicateAccels.cs#1)]  
  
## <a name="see-also"></a>Viz také  
 <xref:System.Resources.ResourceManager?displayProperty=fullName>   
 [Prostředky v desktopových aplikacích](http://msdn.microsoft.com/library/8ad495d4-2941-40cf-bf64-e82e85825890)


