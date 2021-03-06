---
title: 'CA1900: Pole hodnot by měla být přenosná | Dokumentace Microsoftu'
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
- CA1900
- ValueTypeFieldsShouldBePortable
helpviewer_keywords:
- ValueTypeFieldsShouldBePortable
- CA1900
ms.assetid: 1787d371-389f-4d39-b305-12b53bc0dfb9
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b0a636c1de245aa46adb0b0e43c6802dddf57810
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42676930"
---
# <a name="ca1900-value-type-fields-should-be-portable"></a>CA1900: Pole hodnot by měla být přenosná
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější dokumentaci k sadě Visual Studio 2017, najdete v části [CA1900: pole hodnot by měla být přenosná](https://docs.microsoft.com/visualstudio/code-quality/ca1900-value-type-fields-should-be-portable) na webu docs.microsoft.com.  
  
|||  
|-|-|  
|TypeName|ValueTypeFieldsShouldBePortable|  
|CheckId|CA1900|  
|Kategorie|Microsoft.Portability|  
|Narušující změna|Zásadní – Pokud je pole viditelné mimo sestavení.<br /><br /> Bez konce – Pokud pole není viditelné mimo sestavení.|  
  
## <a name="cause"></a>příčina  
 Toto pravidlo zkontroluje, že budou při zařazení na nespravovaný kód v 64bitových operačních systémech správně zarovnány struktury, které jsou deklarovány pomocí explicitního rozložení. Nezarovnané přístupy a proces se chybově ukončit, pokud toto porušení nebyl vyřešen IA-64 není povolena.  
  
## <a name="rule-description"></a>Popis pravidla  
 Struktury, které mají explicitní rozložení obsahující nezarovnané pole příčina selhání v 64bitových operačních systémech.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Všechna pole, která jsou menší než 8 bajtů musí mít posuny, které jsou násobkem jejich velikost a pole, které mají 8 bajtů nebo více musí mít posuny, které jsou násobkem 8. Druhým řešením je použití `LayoutKind.Sequential` místo `LayoutKind.Explicit`, pokud přiměřené.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Toto upozornění má výjimka potlačit pouze v případě, že dojde k chybě.

