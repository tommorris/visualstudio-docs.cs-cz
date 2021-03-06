---
title: Nastavení sady Visual Studio spuštění zátěžového testu z příkazového řádku
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, command line
- load tests, run settings, selecting
ms.assetid: 175d1d58-f09a-4449-b132-a29a394a7c8e
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 263f8a671897b5f9c8af835f13214139e3abef17
ms.sourcegitcommit: 495bba1d8029646653f99ad20df2f80faad8d58b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2018
ms.locfileid: "39382474"
---
# <a name="how-to-select-a-load-test-run-setting-to-use-from-the-command-line"></a>Postupy: Výběr nastavení, můžete používat z příkazového řádku pro spuštění zátěžového testu

Zátěžový test může obsahovat *parametry běhu*, které jsou vlastnosti, které ovlivňují způsob běhu zátěžového testu. Parametry spuštění jsou uspořádány podle kategorií v **vlastnosti** okna. Zátěžový test při svém spuštění používá parametry spuštění, které jsou aktuálně nastaveny jako aktivní.

 Pokud zátěžový test obsahuje pouze jeden parametr spuštění, jedná se vždy o aktivní uzel. Pokud zátěžový test obsahuje více uzlů parametrů spuštění, můžete vybrat ten, který má použít při spuštění zátěžového testu z příkazového řádku. Zobrazit [postupy: přidání dalších parametrů běhu k zátěžovému testu](../test/how-to-add-additional-run-settings-to-a-load-test.md).

## <a name="to-change-the-run-setting-from-the-command-line"></a>Chcete-li změnit nastavení spuštění z příkazového řádku

1.  Pokud chcete použít různé parametry spuštění z příkazového řádku využít tak strategii kontextových parametrů, použijte následující příkaz:

    `Set Test.UseRunSetting= CorporateStagingWebServer`

2.  Spusťte zátěžový test pomocí nástroje mstest:

    `mstest /testcontainer:loadtest1.loadtest`

## <a name="see-also"></a>Viz také:

- [Konfigurace parametrů spuštění zátěžového testu](../test/configure-load-test-run-settings.md)
- [Určení sad čítačů a mezních pravidel pro počítače v rámci zátěžového testu](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)
- [Postupy: přidání dalších parametrů běhu k zátěžovému testu](../test/how-to-add-additional-run-settings-to-a-load-test.md)
- [Postupy: výběr aktivního parametru spuštění pro zátěžový test](../test/how-to-select-the-active-run-setting-for-a-load-test.md)
