---
title: 'Rychlý start: Použití sady Visual Studio k vytvoření první aplikace konzoly C#'
description: Zjistěte, jak vytvořit jednoduchou konzolovou aplikaci Hello World v sadě Visual Studio s C#, krok za krokem.
ms.custom: ''
ms.date: 09/21/2018
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: quickstart
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: douge
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: ee40aadd3287018e52910ad6b4a4000db6bcce8a
ms.sourcegitcommit: 6672a1e9d135d7e5cca3cceea07c6fe5a0871475
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2018
ms.locfileid: "47443412"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-c-console-app"></a>Rychlý start: Použití sady Visual Studio k vytvoření první aplikace konzoly C#

V tomto úvodu 5 až 10 minut do integrovaného vývojového prostředí (IDE) sady Visual Studio vytvoříte jednoduchou C# aplikaci, která běží na konzole.

Pokud jste ještě nenainstalovali aplikaci Visual Studio, přejděte [soubory ke stažení Visual Studio](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) stránku a nainstalovat zdarma.

## <a name="create-a-project"></a>Vytvoření projektu

Nejprve vytvoříte aplikaci projektu jazyka C#. Typ projektu obsahuje všechny soubory šablon, které potřebujete, než jste přidali ještě nic!

1. Otevřete Visual Studio 2017.

2. V horním řádku nabídek zvolte **Soubor** > **Nový** > **Projekt**.

3. V **nový projekt** dialogové okno v levém podokně rozbalte **jazyka C#** a klikněte na tlačítko **.NET Core**. V prostředním podokně vyberte **Konzolová aplikace (.NET Core)**. Zadejte název projektu *HelloWorld*.

   ![Konzole šablonu projektu aplikace (.NET Core) v dialogovém okně Nový projekt v integrovaném vývojovém prostředí sady Visual Studio](../ide/media/new-project-csharp-dotnetcore-helloworld-console-app.png)

     Pokud se nezobrazí **Konzolová aplikace (.NET Core)** šablony projektu, zvolte **otevřít instalační program Visual Studio** odkaz v levém podokně **nový projekt** dialogové okno.

   ![Zvolte odkaz otevřít instalační program Visual Studio z dialogového okna Nový projekt](../ide/media/csharp-open-visual-studio-installer-hello-world.png)

     Spustí se instalační program pro Visual Studio. Zvolte **vývoj pro různé platformy .NET Core** úlohy a klikněte na tlačítko **změnit**.

     ![Úlohy pro vývoj pro různé platformy .NET core v instalačním programu sady Visual Studio](../ide/media/dot-net-core-xplat-dev-workload.png)

## <a name="create-the-application"></a>Vytvoření aplikace

Po výběru šablony projektu C# a pojmenujte svůj projekt, Visual Studio vytvoří jednoduchou aplikaci "Hello World". 

(K tomu, které volá <xref:System.Console.WriteLine%2A> metodu pro zobrazení řetězcový literál "Hello World!" v okně konzoly.)

   ![Zobrazení kódu Hello World výchozí ze šablony](../ide/media/csharp-console-helloworld-template.png)

Pokud stisknete **F5**, spustíte program v režimu ladění. V okně konzoly se však viditelné jenom na chvíli předtím, než se toto okno zavře.

(Proto, `Main` metoda ukončí po jeho jediném příkazu, takže aplikace se ukončí.)

### <a name="add-some-code"></a>Přidání kódu

Přidejme nějaký kód pozastavte aplikaci tak, aby v okně konzoly se nepodporuje zavřít, dokud nestisknete klávesu **ENTER**.

1. Přidejte následující kód bezprostředně po volání <xref:System.Console.WriteLine%2A> metody:

   ```csharp
   Console.ReadLine();
   ```

1. Ověřte, že to vypadá to v editoru kódu:

   ![Přidejte kód pro pozastavení aplikace Hello World](../ide/media/csharp-console-helloworld-add-code.png)

## <a name="run-the-application"></a>Spuštění aplikace

1. Zvolte **HelloWorld** tlačítko na panelu nástrojů ke spuštění aplikace v režimu ladění. (Nebo stisknutím klávesy **F5**.)

   ![Klikněte na tlačítko Hello World a spusťte tak aplikaci z panelu nástrojů](../ide/media/csharp-console-hello-world-button.png)

1. Zobrazení vaší aplikace v okně konzoly.

   ![Okna konzoly zobrazuje Hello World!](../ide/media/csharp-console-hello-world.png)

### <a name="close-the-application"></a>Zavřít aplikaci

1. Stisknutím klávesy **ENTER** zavřete okno konzoly.

1. Zavřít **výstup** podokno v sadě Visual Studio.

   ![Zavřete podokno výstup v sadě Visual Studio](../ide/media/csharp-hello-world-close-output-pane.png)

1. Zavřete Visual Studio.

## <a name="next-steps"></a>Další kroky

Blahopřejeme k dokončení tohoto rychlého startu! Doufáme, že jste se dozvěděli ještě něco o jazyce C# a Visual Studio IDE. Další informace najdete v následujících kurzech pokračujte.

> [!div class="nextstepaction"]
> [Začínáme s aplikaci konzoly C# v sadě Visual Studio](tutorial-csharp-console.md)
