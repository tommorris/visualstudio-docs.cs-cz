---
title: Převedení metody Get na vlastnost a převod vlastnosti na metodu Get v sadě Visual Studio
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
ms.devlang: csharp
author: gewarren
ms.author: gewarren
manager: douge
f1_keywords:
- vs.csharp.refactoring.convertmethodtoproperty
dev_langs:
- csharp
ms.workload:
- dotnet
ms.openlocfilehash: b12dcbcf5a008ff7d4b839f3f4c6b90d43b3b05e
ms.sourcegitcommit: aea5cdb76fbc7eb31d1e5cc3c8d6adb0c743220f
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2018
ms.locfileid: "44124779"
---
# <a name="convert-get-method-to-property--convert-property-to-get-method-refactorings"></a>Převedení metody Get na vlastnost / vlastnost převést na refaktoringy Get – metoda

Tyto refaktoringy platí pro:

- C#

## <a name="convert-get-method-to-property"></a>Převedení metody Get na vlastnost

**Co:** umožňuje převést metody Get na vlastnosti (a volitelně metodu Set).

**Kdy:** měl odpovídající metodu Get, který neobsahuje žádnou logiku.

### <a name="how-to"></a>Postupy

1. Umístěte ukazatel myši v názvu metody Get.

1. Dále proveďte jednu z následujících akcí:

   - **Klávesnice**
     - Stisknutím klávesy **Ctrl**+**.** aktivační událost **rychlé akce a Refaktoringy** nabídky a vybereme **nahraďte metodu pomocí vlastnosti** z automaticky otevíraného okna okno náhledu.
   - **Myši**
     - Klikněte pravým tlačítkem na kód, vyberte **rychlé akce a Refaktoringy** nabídky a vybereme **nahraďte metodu vlastnost** z automaticky otevíraného okna okno náhledu.

1. (Volitelné) Pokud máte metodu Set, můžete také metodu Set v tuto chvíli převést tak, že vyberete **metoda nahradit Get a Set – metoda s vlastností**.

1. Pokud jste spokojení se změnou ve verzi preview kód, stiskněte **Enter** nebo klikněte na opravu z nabídky a změny budou potvrzeny.

Příklad:

```csharp
private int MyValue;

// Before
public int GetMyValue()
{
    return MyValue;
}

// Replace 'GetMyValue' with property

// After
public int MyValue
{
    get { return MyValue; }
}
```

## <a name="convert-property-to-get-method"></a>Převod vlastnosti na metodu Get

**Co:** umožňuje převod vlastnosti na metodu Get

**Kdy:** mít zadanou vlastnost, která zahrnuje více než okamžitě nastavení a získání hodnoty

### <a name="how-to"></a>Postupy

1. Umístěte ukazatel myši v názvu metody Get.

1. Dále proveďte jednu z následujících akcí:

   - **Klávesnice**
     - Stisknutím klávesy **Ctrl**+**.** aktivační událost **rychlé akce a Refaktoringy** nabídky a vybereme **vlastnost nahraďte metody** z automaticky otevíraného okna okno náhledu.
   - **Myši**
     - Klikněte pravým tlačítkem na kód, vyberte **rychlé akce a Refaktoringy** nabídky a vybereme **vlastnost nahraďte metody** z automaticky otevíraného okna okno náhledu.

1. Pokud jste spokojení se změnou ve verzi preview kód, stiskněte **Enter** nebo klikněte na opravu z nabídky a změny budou potvrzeny.

## <a name="see-also"></a>Viz také:

- [Refactoring](../refactoring-in-visual-studio.md)
- [Náhled změn](../../ide/preview-changes.md)