---
title: "CA2135: Sestavení úrovně 2 nesmějí obsahovat LinkDemands | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CA2135
ms.assetid: 7a775285-42d2-4f13-8434-3fdb0deeebe6
caps.latest.revision: "10"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2374b8de7e3d4f915f836f718b32dee028bee9ff
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="ca2135-level-2-assemblies-should-not-contain-linkdemands"></a>CA2135: Sestavení úrovně 2 nesmějí obsahovat LinkDemands
|||  
|-|-|  
|TypeName|SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands|  
|CheckId|CA2135|  
|Kategorie|Microsoft.Security|  
|Narušující změna|Narušující|  
  
## <a name="cause"></a>příčina  
 Třída nebo člen třídy používá <xref:System.Security.Permissions.SecurityAction> v aplikaci, která používá zabezpečení Level 2.  
  
## <a name="rule-description"></a>Popis pravidla  
 Pravidla LinkDemand jsou v sadě pravidel zabezpečení úrovně 2 již zastaralá. Místo použití LinkDemands vynutit zabezpečení v době kompilace za běhu (JIT), označit metody, typy a pole s <xref:System.Security.SecurityCriticalAttribute> atribut.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Chcete-li opravit porušení toto pravidlo, odeberte <xref:System.Security.Permissions.SecurityAction> a označit typ nebo člen s <xref:System.Security.SecurityCriticalAttribute> atribut.  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Nepotlačujte upozornění na toto pravidlo.  
  
## <a name="example"></a>Příklad  
 V následujícím příkladu <xref:System.Security.Permissions.SecurityAction> měla by být odebrána a označené jako metodu <xref:System.Security.SecurityCriticalAttribute> atribut.  
  
 [!code-csharp[FxCop.Security.CA2135.SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2135-level-2-assemblies-should-not-contain-linkdemands_1.cs)]