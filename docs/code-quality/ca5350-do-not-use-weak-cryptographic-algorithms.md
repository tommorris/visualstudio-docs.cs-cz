---
title: "CA5350: Nepoužívejte slabé kryptografické algoritmy | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 4c51bb8a-fcfa-46aa-ab61-634be84c4a7a
caps.latest.revision: "11"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7bcc92434640306105ccec8100d66e9c38426f88
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="ca5350-do-not-use-weak-cryptographic-algorithms"></a>CA5350: Nepoužívejte slabé kryptografické algoritmy
|||  
|-|-|  
|TypeName|DoNotUseWeakCryptographicAlgorithms|  
|CheckId|CA5350|  
|Kategorie|Microsoft.Cryptography|  
|Narušující změna|Bez ukončování řádků|  
  
> [!NOTE]
>  Toto upozornění byl naposledy aktualizován. listopadu 2015.  
  
## <a name="cause"></a>příčina  
 Algoritmy šifrování, jako <xref:System.Security.Cryptography.TripleDES> a algoritmy hash, jako <xref:System.Security.Cryptography.SHA1> a <xref:System.Security.Cryptography.RIPEMD160> se považují za slabé.  
  
 Tyto kryptografické algoritmy neposkytují tolik zajištění zabezpečení jako více moderní svými protějšky. Kryptografické algoritmy hash <xref:System.Security.Cryptography.SHA1> a <xref:System.Security.Cryptography.RIPEMD160> zadejte menší kolizí odporu než více moderní délkami algoritmů hash. Šifrovací algoritmus <xref:System.Security.Cryptography.TripleDES> poskytuje méně bity zabezpečení než více moderních šifrovacích algoritmů.  
  
## <a name="rule-description"></a>Popis pravidla  
 Slabé šifrování algoritmy hash funkce pro používají a dnes z mnoha důvodů, ale nepoužívejte zaručit důvěrnost dat, které chrání.  
  
 Toto pravidlo spustí, když se najde 3DES, algoritmů SHA1 nebo RIPEMD160 v editoru kódu a generuje upozornění pro uživatele.  
  
## <a name="how-to-fix-violations"></a>Jak vyřešit porušení  
 Použijte kryptograficky silnější možnosti:  
  
-   Pro šifrování TripleDES, použijte <xref:System.Security.Cryptography.Aes> šifrování.  
  
-   Pro funkce hash SHA1 nebo RIPEMD160, použijte těch, které jsou v [SHA-2](https://msdn.microsoft.com/en-us/library/windows/desktop/aa382459.aspx) rodiny (například <xref:System.Security.Cryptography.SHA512>, <xref:System.Security.Cryptography.SHA384>, <xref:System.Security.Cryptography.SHA256>).  
  
## <a name="when-to-suppress-warnings"></a>Kdy potlačit upozornění  
 Potlačíte upozornění na toto pravidlo, když úroveň ochrany, které jsou potřebné pro data nevyžaduje záruku zabezpečení.  
  
## <a name="pseudo-code-example"></a>Příklad pseudo kódu  
 Od verze době psaní tohoto textu znázorňuje následující ukázka kódu pseudo vzoru zjistil tímto pravidlem.  
  
### <a name="sha-1-hashing-violation"></a>Porušení hash SHA-1  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA1.Create();  
  
```  
  
### <a name="solution"></a>Řešení  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA256.Create();  
  
```  
  
### <a name="ripemd160-br-br-hashing-violation"></a>RIPEMD160 <br /><br />Hash porušení  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = RIPEMD160Managed.Create();  
  
```  
  
### <a name="solution"></a>Řešení  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA256.Create();  
  
```  
  
### <a name="tripledes-encryption-violation"></a>Porušení šifrování TripleDES  
  
```  
using System.Security.Cryptography;   
...    
using (TripleDES encAlg = TripleDES.Create())   
{   
  ...   
}  
```  
  
### <a name="solution"></a>Řešení  
  
```  
using System.Security.Cryptography;   
...   
using (AesManaged encAlg = new AesManaged())   
{   
  ...   
}  
```