---
title: Přesunutí deklarace do blízkosti odkazu proměnné v sadě Visual Studio
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- csharp
ms.workload:
- dotnet
ms.openlocfilehash: fc6ee94cbebb1cb35dd524017f22bd8ab3812468
ms.sourcegitcommit: aea5cdb76fbc7eb31d1e5cc3c8d6adb0c743220f
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2018
ms.locfileid: "44124954"
---
# <a name="move-declaration-near-reference-refactoring"></a>Přesunutí deklarace do blízkosti odkazu refaktoring

Tento refaktoring platí pro:

- C#

**Co:** můžete přesouvat deklarace proměnných blíž k jejich využití.

**Kdy:** máte deklarace proměnných, které mohou být v užší oboru.

**Důvod, proč:** může ponechat, jak je, ale mohou způsobit problémy čitelnost nebo skrytí informace. Toto je příležitost dobře se Refaktorovat pro lepší čitelnost.

## <a name="how-to"></a>Postupy

1. Umístěte ukazatel myši v deklaraci proměnné.

1. Dále proveďte jednu z následujících akcí:

   - **Klávesnice**
     - Stisknutím klávesy **Ctrl**+**.** aktivační událost **rychlé akce a Refaktoringy** nabídky a vybereme **přesunutí deklarace do blízkosti odkazu** z automaticky otevíraného okna okno náhledu.
   - **Myši**
     - Klikněte pravým tlačítkem na kód, vyberte **rychlé akce a Refaktoringy** nabídky a vybereme **přesunutí deklarace do blízkosti odkazu** z automaticky otevíraného okna okno náhledu.

1. Až budete spokojení s změny, stiskněte klávesu **Enter** nebo klikněte na opravit v nabídce a změny budou potvrzeny.

Příklad:

```csharp
// Before
int x;
if (condition)
{
    x = 1;
    Console.WriteLine(x);
}

// Move declaration near reference

// After
if (condition)
{
    int x = 1;
    Console.WriteLine(x);
}
```

## <a name="see-also"></a>Viz také:

- [Refactoring](../refactoring-in-visual-studio.md)
- [Náhled změn](../../ide/preview-changes.md)