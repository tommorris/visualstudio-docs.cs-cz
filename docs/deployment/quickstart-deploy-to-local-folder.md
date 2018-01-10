---
title: "Nasazení do místní složky - Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 11/22/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: quickstart
helpviewer_keywords: deployment, local folder
ms.assetid: adb461c4-812a-4b8c-b2ab-96002379f6a9
caps.latest.revision: "1"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 3b97ca67c9e8d8a4cfb7d99a6c518c8e49a8c426
ms.sourcegitcommit: 9357209350167e1eb7e50b483e44893735d90589
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/05/2018
---
# <a name="deploy-a-web-app-or-net-core-app-to-a-local-folder-using-the-visual-studio-publish-tool"></a>Nasazení do místní složky pomocí nástroje Visual Studio publikovat webovou aplikaci nebo aplikaci .NET Core

Můžete použít **publikovat** nástroj pro publikování aplikace do místní složky. 

Tento postup platí pro technologii ASP.NET, ASP.NET Core, .NET Core a Python aplikace v sadě Visual Studio. Pro platformu Node.js kroky jsou podporované, ale uživatelské rozhraní se liší.

## <a name="create-a-new-project"></a>Vytvoření nového projektu 

1. V sadě Visual Studio, vyberte **soubor > Nový projekt**.

1. V části **Visual C#** nebo **jazyka Visual Basic**, zvolte **.NET Core**a potom v prostředním podokně vyberte **konzolové aplikace (.NET Core)**.

1. Zadejte název jako **MyLocalApp** a klikněte na tlačítko **OK**.

    Visual Studio vytvoří projekt.

## <a name="deploy-to-a-local-folder"></a>Nasazení do místní složky

1. V Průzkumníku řešení klikněte pravým tlačítkem na projekt a zvolte **publikovat**.

    ![Zvolte publikování](../deployment/media/quickstart-publish.png "zvolte publikování")

1. V **publikovat** podokně vyberte **složky**.

    ![Vyberte složku,](../deployment/media/quickstart-publish-folder.png "vyberte složku,")

1. Zadejte cestu nebo klikněte na tlačítko **Procházet** a přejděte do místní složky.

1. Klikněte na tlačítko **publikování**.

    Visual Studio vytvoří projekt a publikuje do zadané složky.

    V podokně publikovat zobrazuje souhrn profil.

1. Chcete-li konfigurovat nastavení nasazení, klikněte na tlačítko **nastavení** v souhrnu profilu.

    ![Nastavení profilu](../deployment/media/quickstart-profile-settings.png "nastavení profilu") 

1. Konfigurovat možnosti, například zda ladění nebo verze konfigurace nasazení a pak klikněte na tlačítko **Uložit**.

1. Chcete-li znovu publikovat, klikněte na tlačítko **publikovat**.

Publikované soubory žádným způsobem, který chcete nasaďte. Můžete například zabalit v souboru Zip, použijte příkaz jednoduché kopírování nebo nasadit všechny instalačním balíčkem podle svého výběru.

## <a name="next-steps"></a>Další kroky

- [Nasazení aplikace .NET Core pomocí nástroje publikování](/dotnet/core/deploying/deploy-with-vs)
- [Balíček aplikace na ploše pro Microsoft Store (Desktop mostu)](/windows/uwp/porting/desktop-to-uwp-packaging-dot-net)
- (.NET) [Nasazení rozhraní .NET Framework a aplikace](/dotnet/framework/deployment/)