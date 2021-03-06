---
title: Výčty jazyka Visual C++ v návrháři tříd
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- Class Designer [Visual Studio], enumerations
ms.assetid: 11e90ba1-18cd-44f8-9e26-e3746a7a19d1
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: a42dfb65cc70704bbed662e35b2e2eb0e9c237c4
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2018
ms.locfileid: "31922017"
---
# <a name="visual-c-enumerations-in-class-designer"></a>Výčty Visual C++ v Návrháři tříd

**Třídy návrháře** podporuje C++ `enum` a oboru `enum class` typy. Tady je příklad:

```cpp
enum CardSuit {
   Diamonds = 1,
   Hearts = 2,
   Clubs = 3,
   Spades = 4
};

// or...
enum class CardSuit {
   Diamonds = 1,
   Hearts = 2,
   Clubs = 3,
   Spades = 4
};
```

C++ – výčet obrazce v diagramu tříd vypadat a fungovat jako struktura obrazce, s výjimkou toho, aby četl popisek **výčtu** nebo **výčet tříd**, je růžový místo blue a má barevný vlevo a horní okraj okraje. Výčet tvarů a struktura tvarů mít hranatými rohy.

Další informace o používání `enum` zadejte najdete v tématu [výčty](/cpp/cpp/enumerations-cpp).

## <a name="see-also"></a>Viz také

- [Práce s kódem jazyka Visual C++](working-with-visual-cpp-code.md)
- [Výčty](/cpp/cpp/enumerations-cpp)