---
title: Úpravy zátěžových testů v sadě Visual Studio
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- Load Test Editor
- load tests, Load Test Editor
ms.assetid: ba16ed02-137e-40bf-a4cb-45d87d922d37
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: f4c29f3b98440c9e8462083a24012944157b848b
ms.sourcegitcommit: 5b767247b3d819a99deb0dbce729a0562b9654ba
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/20/2018
ms.locfileid: "39178410"
---
# <a name="edit-load-tests"></a>Úpravy zátěžových testů

Zátěžové testy spouštět testy výkonnosti webů nebo testů jednotek simulace mnoha uživatelů přistupujících na server ve stejnou dobu. Zátěžový test umožňuje přístup k datům zátěže a výkonu aplikace. Zátěžový test lze nakonfigurovat pro emulaci rozličných podmínek zátěže, jako je uživatelská zátěž nebo typ sítě.

> [!NOTE]
> Zátěžové testování je k dispozici pouze v edici Enterprise sady Visual Studio 2017.

Zátěžový test je definován *scénáře*, *sady čítačů*, a *parametry běhu*. Na následujícím obrázku vysvětluje rozdíly mezi [scénáře](../test/edit-load-test-scenarios.md), [sady čítačů](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md), a [parametry běhu](../test/load-test-run-settings-properties.md):

![Architektura zátěžového testu](../test/media/load_test_editor.png)

## <a name="edit-load-test-scenario-settings"></a>Upravit nastavení scénáře zátěžového testu

Scénáře se používají k modelování způsobu interakce skupiny uživatelů se serverovou aplikací. Scénáře se skládají ze vzoru zatížení, modelu kombinace testů, kombinace testů, kombinace prohlížečů a kombinace sítí. Zátěžový test může mít více než jeden scénář a jeden scénář může obsahovat testy výkonnosti webu a testy jednotek. Seskupením podobných nastavení umožňuje scénář seskupit podobné testy a spustit je současně.

Další informace najdete v tématu [úpravy scénářů zátěžových testů](../test/edit-load-test-scenarios.md) a [vlastnosti scénáře zátěžového testu](../test/load-test-scenario-properties.md).

## <a name="configure-and-manage-performance-counter-sets"></a>Konfigurace a Správa sad čítačů výkonu

Zátěžové testy poskytují pojmenované sady čítačů organizované podle technologie, které jsou užitečné při analýze dat čítače výkonu. Nastavení čítače zahrnují testu zatížení, IIS, ASP.NET a SQL. Když vytvoříte zátěžový test pomocí **nového Průvodce zátěžovým testem**, Počáteční sada předdefinovaných a důležitých čítačů je nakonfigurován pro počítače, které zahrnete do zátěžového testu. Můžete spravovat čítače v **editoru zátěžových testů**.

Další informace najdete v tématu [určení sad čítačů a mezních pravidel pro počítače v rámci zátěžového testu](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md).

## <a name="configure-and-manage-load-test-run-settings"></a>Konfigurace a Správa parametrů spuštění zátěžového testu

Parametry spuštění představují vlastnosti, které ovlivňují způsob, jakým běží zátěžové testy. Parametry spuštění jsou uspořádány podle kategorií v **vlastnosti** okna.

Další informace najdete v tématu [konfigurovat zátěžovým testem nastavení](../test/configure-load-test-run-settings.md) a [zátěžového testu spusťte nastavení](../test/load-test-run-settings-properties.md).

## <a name="see-also"></a>Viz také:

- [Analýza výsledků zátěžových testů](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
- [Analýza mezních pravidel](../test/analyze-threshold-rule-violations-in-load-tests.md)