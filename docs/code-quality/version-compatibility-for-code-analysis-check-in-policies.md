---
title: Kompatibilita verzí pro zásady vracení se změnami Analýzy kódu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- version compatibility, code analysis check-in policy
- check-in policies, version compatibility for code analysis
ms.assetid: 1af376e3-3be7-4445-803b-76a858567a5b
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 01a8a0c4e859e6f03ba55176d535b0b4e7e6a1b0
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2018
ms.locfileid: "31915812"
---
# <a name="version-compatibility-for-code-analysis-check-in-policies"></a>Kompatibilita verzí pro zásady vracení se změnami Analýzy kódu
Pokud se musí vyhodnotit a vytváření zásad analýzy kódu vrácení se změnami pomocí různých verzích [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)], musíte znát rozdíly v tom [!INCLUDE[vstsTfsOrcasLong](../code-quality/includes/vststfsorcaslong_md.md)] a [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] vyhodnocení zásad vrácení se změnami.

## <a name="version-compatibility-for-evaluating-check-in-policies"></a>Kompatibilita verzí pro vyhodnocení zásad vrácení se změnami

-   Když jsou vyhodnocovány zásad vrácení se změnami analýzy kódu v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], všechna pravidla, které existovaly v sadě [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] , ale nejsou k dispozici v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] jsou ignorovány.

-   Když jsou vyhodnocovány zásad vrácení se změnami analýzy kódu v [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)], všechny nové pravidel, která jsou výhradně pro [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] jsou ignorovány.

-   Pokud zásady vrácení se změnami kódu analysis určuje pravidla sestavení [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] ignoruje všechna pravidla, které jsou určené sestavení, nelze rozpoznat.

-   Je-li zásad vrácení se změnami kódu analysis určuje pravidla sestavení, [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] nerozpozná, zobrazí se zpráva.

## <a name="version-compatibility-for-authoring-check-in-policies"></a>Kompatibilita verzí pro vytváření zásad vrácení se změnami

-   Pokud jste vytvořili zásady pro analýzu kódu vrácení se změnami pomocí [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] verzi [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)], nemůžete použít [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] verzi [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] jej upravit. A navíc [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] nelze vyhodnotit zásadu.

-   Pokud jste vytvořili zásady pro analýzu kódu vrácení se změnami pomocí [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] v [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)], můžete použít [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)] změnit a zásady můžete taky vyhodnocení [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)]. Po úpravě zásad pomocí [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], zásady už můžete upravit pomocí [!INCLUDE[esprtfc](../code-quality/includes/esprtfc_md.md)] v [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)]. [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] můžete vyhodnotit zásady bez problémů s odlišnými silné názvy.

-   K vytvoření zásad vrácení se změnami kódu analysis s nastavením pravidlo, které platí pro obě [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] a [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], musíte vytvořit zásadu v [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)], proveďte všechny potřebné změny a uložení zásady. Pokud existují změny pravidel pouze v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], upravit a uložit zásadu v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)].

     Po uložení zásady v [!INCLUDE[vstsTfsOrcasShort](../code-quality/includes/vststfsorcasshort_md.md)], už můžete změnit nastavení pro pravidla, které existují v [!INCLUDE[vstsTfsRosarioShort](../code-quality/includes/vststfsrosarioshort_md.md)] pouze.