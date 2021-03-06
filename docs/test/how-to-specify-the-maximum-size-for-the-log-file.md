---
title: Velikost souboru protokolu pro zátěžové testy v sadě Visual Studio
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, logging
ms.assetid: 417059bf-37ae-4e7a-b9b0-29bd71f1414f
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 29329cb1403745b80d68670f5316ce570582d72c
ms.sourcegitcommit: 495bba1d8029646653f99ad20df2f80faad8d58b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2018
ms.locfileid: "39379394"
---
# <a name="how-to-specify-the-maximum-size-for-the-log-file-for-load-tests"></a>Postupy: určení maximální velikosti souboru protokolu pro zátěžové testy

Ve výchozím nastavení je nastavena maximální velikost souboru protokolu, který se používá pro zátěžové testy 20 megabajtů. Tuto hodnotu můžete změnit úpravou konfiguračního souboru přidruženého ke službě kontroleru.

## <a name="specify-the-maximum-log-file-size-for-load-test"></a>Zadejte maximální velikosti souboru pro zátěžový test

1.  Otevřít *QTCcontroller.exe.config* konfigurační soubor XML v *% ProgramFiles (x86) %\Microsoft Visual Studio\2017\Enterprise\Common7\IDE\QTCcontroller.exe.config*.

2.  Vyhledejte `<add key="LogSizeLimitInMegs" value="20"/>` položku `<appSettings>` značky.

    ```xml
    <appSettings>
        <add key="LogSizeLimitInMegs" value="20"/>
        <add key="AgentConnectionTimeoutInSeconds" value="120"/>
        <add key="AgentSyncTimeoutInSeconds" value="300"/>
        <add key="ControllerServicePort" value="6901"/>
        <add key="ControllerUsersGroup" value="TeamTestControllerUsers"/>
        <add key="ControllerAdminsGroup" value="TeamTestControllerAdmins"/>
        <add key="CreateTraceListener" value="no"/>
      </appSettings>
    ```

3.  Upravit `value ="20"` na maximální povolenou velikost, které se mají určit pro soubor protokolu.

    > [!NOTE]
    > Zadáním hodnoty "0" Určuje, že soubor protokolu je pouze omezen velikostí volného místa na disku.

## <a name="see-also"></a>Viz také:

- [Úprava nastavení protokolování zátěžového testu](../test/modify-load-test-logging-settings.md)
- [Konfigurace portů pro testovací kontroléry a testovací agenty](../test/configure-ports-for-test-controllers-and-test-agents.md)