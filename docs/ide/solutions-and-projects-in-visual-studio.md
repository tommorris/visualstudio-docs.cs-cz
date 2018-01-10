---
title: "Řešení a projektů v sadě Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 10/5/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.addnewsolutionitem
- vs.environment.projects
- vs.openproject
- vs.addnewitem
- vs.addexistingitem
- VS.SolutionExplorer
- vs.newproject
- vs.addexistingsolutionitem
- vs.environment.solutions
- VS.SolutionExplorer.Solutions
helpviewer_keywords:
- solution items [Visual Studio]
- solutions [Visual Studio]
- project items [Visual Studio]
- solutions [Visual Studio], designing
- projects [Visual Studio]
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 4d242a74bd1eaef86e3465d53aa148429af42f7e
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/22/2017
---
# <a name="solutions-and-projects-in-visual-studio"></a>Řešení a projektů v sadě Visual Studio

## <a name="projects"></a>Projekty

Když vytvoříte aplikaci, web, modul plug-in, atd. v sadě Visual Studio spustíte s *projektu*. V logických smysl projekt obsahuje všechny soubory zdrojového kódu, ikony, bitové kopie, datové soubory, atd., které jsou zkompilovány do spustitelný soubor, knihovny nebo webu. Projekt obsahuje také nastavení kompilátoru a ostatní konfigurační soubory, které mohou být potřebné různé služby nebo součásti, které váš program komunikuje s.

> [!NOTE]
> Nemusíte používat řešení nebo projekty v sadě Visual Studio k úpravám, sestavení a ladění kódu. Můžete jednoduše otevřete složku, která obsahuje zdrojové soubory v sadě Visual Studio a začít upravovat. V tématu [vývoj kódu v sadě Visual Studio bez projekty a řešení](../ide/develop-code-in-visual-studio-without-projects-or-solutions.md) Další informace.

Projekt je definován v souboru XML s příponou, třeba .vbproj, .csproj nebo VCXPROJ. Tento soubor obsahuje hierarchii virtuální složek a cesty pro všechny položky v projektu. Obsahuje taky nastavení sestavení.

> [!TIP]
> Podívat se na obsah souboru projektu v sadě Visual Studio, nejdřív uvolnit projekt v Průzkumníku řešení výběrem název projektu a zvolením **uvolnit projekt** z nabídky kontext nebo klikněte pravým tlačítkem. Pak znovu otevřete kontextu nabídku a vyberte **upravit \<projectname\>**.

V sadě Visual Studio je soubor projektu vrstva Průzkumníku řešení používá pro zobrazení obsahu projektu a nastavení. Při kompilaci projektu nástroje MSBuild modul využívá soubor projektu pro vytvoření spustitelného souboru. Můžete také upravit projekty k vytvoření jiné druhy výstup.

## <a name="solutions"></a>Řešení

Je součástí projektu *řešení*. Řešení obsahuje jeden nebo více souvisejících projekty, společně s informacemi o sestavení, Visual Studio okna nastavení a všechny ostatní soubory, které nejsou přidruženy k konkrétní projekt. Řešení je popsán textový soubor (rozšíření .sln) s svůj vlastní jedinečný formát; Obecně není určen k provádění úprav ručně.

Řešení má přidruženou *.suo* soubor, který ukládá nastavení, předvoleb a informace o konfiguraci pro každý uživatel, který pracoval na projekt.

## <a name="creating-new-projects"></a>Vytváření nových projektů

Nejjednodušší způsob, jak vytvořit nový projekt je spuštění z šablona projektu pro konkrétní typ aplikace nebo webu. Šablona projektu se skládá z základní sadu souborů předem generovaného kódu, konfigurační soubory, prostředky a nastavení. Tyto šablony jsou, co se zobrazí v **nový projekt** nebo **nový web** dialogové okno když zvolíte **soubor**, **nový**,  **Projekt** nebo **soubor**, **nové**, **webu**. Další informace najdete v tématu [vytváření řešení a projekty](../ide/creating-solutions-and-projects.md).

Můžete také vytvořit vlastní šablony projektů a položek. Další informace najdete v tématu [vytváření projektů a šablon položek](../ide/creating-project-and-item-templates.md).

## <a name="managing-projects-in-solution-explorer"></a>Správa projektů v Průzkumníku řešení

Po vytvoření nového projektu, můžete použít **Průzkumníku řešení** k zobrazení a správě projektu a řešení a jejich přidružené položky. Následující obrázek znázorňuje Průzkumníku řešení s řešením C#, který obsahuje dva projekty.

![Průzkumník řešení](../ide/media/vs2015_solution_explorer.png "vs2015_solution_explorer")

## <a name="see-also"></a>Viz také

[Integrované vývojové prostředí sady Visual Studio](../ide/visual-studio-ide.md)