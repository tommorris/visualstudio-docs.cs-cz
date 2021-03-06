---
title: T4 – direktiva Output
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: 6044dd970029b3f233f8b20eb2e334b5041ceb33
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2018
ms.locfileid: "31953533"
---
# <a name="t4-output-directive"></a>T4 – direktiva Output

V [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] textové šablony `output` – direktiva se používá k definování kódování souboru transformovaných a příponu názvu souboru.

 Například pokud vaše [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] projekt obsahuje soubor šablony s názvem **MyTemplate.tt** obsahující následující direktivu:

 `<#@output extension=".cs"#>`

 potom [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] vygeneruje soubor s názvem **MyTemplate.cs**

 `output` – Direktiva nevyžaduje v běhu (předběžně zpracované) textové šablony. Místo toho, aplikace získá generované řetězec voláním `TextTransform()`. Další informace najdete v tématu [generování textu běhu pomocí textových šablon T4](../modeling/run-time-text-generation-with-t4-text-templates.md).

## <a name="using-the-output-directive"></a>Using – direktiva Output

```
<#@ output extension=".fileNameExtension" [encoding="encoding"] #>
```

 Měla by existovat více než jeden `output` direktivy v každé šabloně text.

## <a name="extension-attribute"></a>atribut rozšíření
 Určuje příponu názvu souboru výstupního souboru generovaný text.

 Výchozí hodnota je **.cs**

 Příklady: `<#@ output extension=".txt" #>`

 `<#@ output extension=".htm" #>`

 `<#@ output extension=".cs" #>`

 `<#@ output extension=".vb" #>`

 Přípustné hodnoty: Žádné platná přípona názvu souboru.

## <a name="encoding-attribute"></a>kódování atributu
 Určuje kódování použité při vygenerování výstupní soubor. Příklad:

 `<#@ output encoding="utf-8"#>`

 Výchozí hodnota je kódování použité k textovému souboru šablony.

 Přípustné hodnoty: `us-ascii`

 `utf-16BE`

 `utf-16`

 `utf-8`

 `utf-7`

 `utf-32`

 `0` (Výchozí nastavení systému)

 Obecně platí, můžete použít název_webového_serveru řetězec nebo číslo CodePage každého kódování vrácený <xref:System.Text.Encoding.GetEncodings%2A?displayProperty=fullName>.