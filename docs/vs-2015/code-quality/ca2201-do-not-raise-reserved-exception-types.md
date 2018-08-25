---
title: 'CA2201: Nevyvolávejte vyhrazené typy výjimek | Dokumentace Microsoftu'
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
- DoNotRaiseReservedExceptionTypes
- CA2201
helpviewer_keywords:
- CA2201
- DoNotRaiseReservedExceptionTypes
ms.assetid: dd14ef5c-80e6-41a5-834e-eba8e2eae75e
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: af74a7d5943cd8a09b38cee430d75de73ca3ac03
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673881"
---
# <a name="ca2201-do-not-raise-reserved-exception-types"></a>CA2201: Nevyvolávejte vyhrazené typy výjimek
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [CA2201: nevyvolávejte vyhrazené typy výjimek](https://docs.microsoft.com/visualstudio/code-quality/ca2201-do-not-raise-reserved-exception-types).  
  
TypeName | DoNotRaiseReservedExceptionTypes |  
| ID kontroly | CA2201 |  
| Kategorie | Microsoft.Usage|  
| Zásadní změna | Zásadní |  
  
## <a name="cause"></a>příčina  
 Metoda vyvolá typ výjimky, která je příliš obecné, nebo, který je vyhrazen v modulu runtime.  
  
## <a name="rule-description"></a>Popis pravidla  
 Následující typy výjimek jsou příliš obecné poskytnout dostatek informací pro uživatele:  
  
-   <xref:System.Exception?displayProperty=fullName>  
  
-   <xref:System.ApplicationException?displayProperty=fullName>  
  
-   <xref:System.SystemException?displayProperty=fullName>  
  
 Následující typy výjimek jsou vyhrazené a měla by být vyvolána pouze podle modulu common language runtime:  
  
-   <xref:System.ExecutionEngineException?displayProperty=fullName>  
  
-   <xref:System.IndexOutOfRangeException?displayProperty=fullName>  
  
-   <xref:System.NullReferenceException?displayProperty=fullName>  
  
-   <xref:System.OutOfMemoryException?displayProperty=fullName>  
  
 **Nevyvolávat obecné výjimky**  
  
 Pokud abyste vyvolali typ výjimky, jako například <xref:System.Exception> nebo <xref:System.SystemException> v knihovnu nebo architekturu nutí uživatelům zachytit všechny výjimky, včetně Neznámý výjimky, které nejsou věděli, jak zpracovat.  
  
 Místo toho vyvolat více odvozený typ, který již existuje v rámci nebo vytvořit vlastní typ, který je odvozen z <xref:System.Exception>.  
  
 **Vyvolat konkrétní výjimky**  
  
 V následující tabulce jsou uvedeny parametry a výjimek, které má být vyvolána při ověření parametru, včetně hodnoty parametru přístupového objektu set vlastnosti:  
  
|Popis parametru|Výjimka|  
|---------------------------|---------------|  
|`null` Referenční dokumentace|<xref:System.ArgumentNullException?displayProperty=fullName>|  
|Mimo povolený rozsah hodnot (například index pro kolekci nebo seznamu)|<xref:System.ArgumentOutOfRangeException?displayProperty=fullName>|  
|Neplatný `enum` hodnota|<xref:System.ComponentModel.InvalidEnumArgumentException?displayProperty=fullName>|  
|Obsahuje formátu, který splňuje specifikace parametru metody (například řetězec formátu pro `ToString(String)`)|<xref:System.FormatException?displayProperty=fullName>|  
|Jinak neplatných|<xref:System.ArgumentException?displayProperty=fullName>|  
  
 Když operace je neplatná pro aktuální stav vyvolání výjimky objektu <xref:System.InvalidOperationException?displayProperty=fullName>  
  
 Při provádění operace na objektu, který byl uvolněn throw <xref:System.ObjectDisposedException?displayProperty=fullName>  
  
 Když se nepodporuje operace (například v překryté **Stream.Write** v Stream otevřen pro čtení) throw <xref:System.NotSupportedException?displayProperty=fullName>  
  
 Při převodu způsobí přetečení (například v přetížení operátoru přetypování) throw <xref:System.OverflowException?displayProperty=fullName>  
  
 U všech ostatních situacích zvažte možnost vytvořit vlastní typ, který je odvozen z <xref:System.Exception> a, který výjimku.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Chcete-li opravit porušení tohoto pravidla, změňte typ vyvolaná výjimka na konkrétní typ, který není součástí vyhrazené typy.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Nepotlačujte upozornění na toto pravidlo.  
  
## <a name="related-rules"></a>Související pravidla  
 [CA1031: Nezachycujte výjimky obecného typu](../code-quality/ca1031-do-not-catch-general-exception-types.md)


