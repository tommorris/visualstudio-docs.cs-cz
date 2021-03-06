---
title: Spuštění testů jednotek jako 64bitový proces v sadě Visual Studio
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: conceptual
helpviewer_keywords:
- unit tests, creating
- unit tests, running
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: cf8a815cb0827ed69c24686053bf118a48c020eb
ms.sourcegitcommit: 495bba1d8029646653f99ad20df2f80faad8d58b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2018
ms.locfileid: "39379901"
---
# <a name="run-a-unit-test-as-a-64-bit-process"></a>Spuštění testů jednotek v podobě 64bitového procesu

Pokud máte 64bitový počítač, můžete spustit testy jednotky a zaznamenat informace o pokrytí kódu jako 64bitový proces.

## <a name="to-run-a-unit-test-as-a-64-bit-process"></a>Spuštění testování částí jako 64bitový proces

1. Pokud váš kód nebo testů byly kompilovány jako 32-bit/x86, ale chcete nyní spustit jako 64bitový proces, znovu zkompilovat jako **jakýkoli procesor**, nebo volitelně jako **64-bit**.

    > [!TIP]
    > Kvůli maximální flexibilitě, kompilovat testovací projekty s **jakýkoli procesor** konfigurace. Poté můžete spouštět na 32bitových a 64bitových agentech. Neexistuje žádná výhoda pro kompilaci testovacích projektů s **64-bit** konfigurace.

2. V nabídce sady Visual Studio zvolte **testovací**, klikněte na tlačítko **nastavení**a klikněte na tlačítko **architekturu procesoru**. Zvolte **x64** spustit testy jako 64bitový proces.

   - nebo –

   Zadejte `<TargetPlatform>x64</TargetPlatform>` v *s příponou .runsettings* souboru. Výhodou této metody je, že můžete zadat skupiny nastavení v různých souborů a rychle přepínat mezi různými nastaveními. Můžete také kopírovat nastavení mezi řešeními. Další informace najdete v tématu [konfigurace testů jednotek s použitím souboru .runsettings](../test/configure-unit-tests-by-using-a-dot-runsettings-file.md).

## <a name="see-also"></a>Viz také:

- [Spouštění testování částí pomocí Průzkumníka testů](../test/run-unit-tests-with-test-explorer.md)
- [Testování částí kódu](../test/unit-test-your-code.md)
