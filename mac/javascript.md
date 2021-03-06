---
title: JavaScript
description: Informace o podpoře pro jazyk Javascript v sadě Visual Studio pro Mac
author: conceptdev
ms.author: crdun
ms.date: 05/03/2018
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: 61432695-5B12-4257-B250-48D37EED106D
ms.openlocfilehash: 21ff2211632cba63dafe2a7abf1964e7a89e87c3
ms.sourcegitcommit: 2597236a481afbaf1ad4915743898ee1aee49760
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/10/2018
ms.locfileid: "42624250"
---
# <a name="javascript-support"></a>Podpora jazyka JavaScript

Visual Studio pro Mac poskytuje podporu pro Javascript a Typescript prostřednictvím zvýrazňování syntaxe, formátování kódu a technologii IntelliSense. 

![Podpora editoru typescript](https://msdnshared.blob.core.windows.net/media/2018/03/TypeScript-editor.gif)

Další informace o psaní jazyka JavaScript naleznete v části [psaní kódu jazyka Javascript](https://docs.microsoft.com/scripting/javascript/writing-javascript-code) vodítka.

## <a name="adding-a-javascript-file"></a>Přidání souboru jazyka JavaScript

Soubory jazyka JavaScript jsou nejčastěji přidat do projektů ASP.NET Core prostřednictvím **nový soubor** dialogového okna. Chcete-li přidat soubor jazyka javascript, klikněte pravým tlačítkem na projekt a přejděte na **Přidat > Nový soubor**: 

![přidávají se nové soubory do projektu](media/javascript-image1.png)

V dialogovém okně Nový soubor, vyberte **Web > soubor JS sady prázdné** nebo **Web > soubor Typescript**. Pojmenujte ho a klikněte na tlačítko **nový**:

![Vytvoření nového souboru typescript z této šablony](media/javascript-image2.png)

## <a name="intellisense"></a>technologie IntelliSense

Visual Studio pro Mac používá [jazyková služba JavaScriptu](https://docs.microsoft.com/en-us/visualstudio/ide/javascript-intellisense) na poskytovat technologii Intellisense, díky kterým inteligentní doplňování kódu, informace o parametrech a seznamech členů při psaní kódu.

Technologie intellisense jazyka JavaScript v sadě Visual Studio pro Mac může být založen na odvození typu proměnné, JSDoc nebo Typescript deklarace.

- **Odvození typu** – typ objektu je zajištěno pomocí okolního kontext kódu. Další informace najdete v části Visual Studio na [IntelliSense podle odvození typu](https://docs.microsoft.com/visualstudio/ide/javascript-intellisense#intellisense-based-on-type-inference).
- **JSDoc** – existují situace, kdy odvození typu neposkytuje informace o správném typu. V těchto případech lze explicitně zadat informace o typu [JSDoc](http://usejsdoc.org/about-getting-started.html) poznámky. Další informace najdete v části Visual Studio na [Intellisense podle JSDoc](https://docs.microsoft.com/visualstudio/ide/javascript-intellisense#intellisense-based-on-jsdoc)
- **Soubory TypeScript deklarace** – `.d.ts` soubory se používají k poskytnutí hodnot pro technologie Intellisense jazyka Javascript. Typy deklarované v tomto souboru mohou být použity jako typy v komentářích JSDoc. Další informace najdete v části Visual Studio na [IntelliSense podle soubory TypeScript deklarace](https://docs.microsoft.com/visualstudio/ide/javascript-intellisense#intellisense-based-on-typescript-declaration-files) ![přidání definiční soubor typescriptu](media/javascript-image3.png)