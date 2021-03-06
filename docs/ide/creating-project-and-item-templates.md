---
title: Šablony sady Visual Studio pro projekty a soubory
ms.date: 01/02/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- templates [Visual Studio], project
- templates [Visual Studio], item
- item templates [Visual Studio]
- project templates [Visual Studio]
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 62e51a5a03011874acc723eaf159e3f7130d1340
ms.sourcegitcommit: 0aafcfa08ef74f162af2e5079be77061d7885cac
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/01/2018
ms.locfileid: "34573255"
---
# <a name="project-and-item-templates"></a>Šablony projektů a položek

Šablony projektů a položek poskytují opakovaně použitelné zástupných procedur, která uživatelům umožňují některé základní kódu a struktura, která můžete přizpůsobit pro vlastní účely.

## <a name="visual-studio-templates"></a>šablony sady Visual Studio

Několik předdefinovaných projektů a šablon položek je nainstalováno pomocí sady Visual Studio. Například Visual Basic a C# **aplikace pro Windows Forms** a **knihovny tříd** šablony, které jsou zobrazeny v **nový projekt** dialogové okno jsou šablony projektů. Položky zobrazit šablony v **přidat novou položku** dialogové okno pole a zahrnout položek, jako jsou soubory kódu, soubory XML, stránky HTML a stylů.

Tyto šablony představují výchozí bod pro uživatele zahájíte vytváření projektů nebo rozšířit existující projekty. Šablony projektů poskytují soubory, které jsou požadovány pro konkrétní typ projektu, zahrnují standardní odkazy na sestavení a nastavují výchozí vlastnosti projektu a možnosti kompilátoru. Šablony položek může pohybovat složitost z jedné prázdný soubor, který má příponou, k více soubory zdrojového kódu se zakázaným inzerováním kód, informace o návrháři souborů a vložené prostředky.

Můžete použít nainstalovaných šablon v **nový projekt** a **přidat novou položku** dialogových oken, vytvářet vlastní šablony, nebo stažení a použití šablony vytvořené komunitou. Další informace najdete v tématu [postupy: vytváření šablon projektu](../ide/how-to-create-project-templates.md) a [postupy: vytváření šablon položek](../ide/how-to-create-item-templates.md).

## <a name="contents-of-a-template"></a>Obsah šablony

Všechny šablony projektů a položek, ať už nainstalované s Visual Studio nebo vytvořené vámi, funkce pomocí stejné zásady a mají podobný obsah. Všechny šablony obsahují následující položky:

- Soubory, které mají být vytvořeny při použití této šablony. Tyto soubory zahrnují soubory zdrojového kódu, vložené prostředky, soubory projektu a tak dále.

- Jeden *.vstemplate* soubor obsahující metadata potřebná k zobrazení šablony v **nový projekt** a **přidat novou položku** dialogových oken a vytvoření projektu nebo položky z Šablona. Další informace o *.vstemplate* soubory, najdete v části [parametry šablony](../ide/template-parameters.md).

Když jsou tyto soubory do komprimované *.zip* souboru a put ve správné složce, Visual Studio automaticky zobrazí je v následujících umístěních:

- Šablony projektu se zobrazí v **nový projekt** dialogové okno.

- Šablony položek se zobrazí v **přidat novou položku** dialogové okno.

Další informace o složkách šablony najdete v tématu [postupy: hledání a organizace šablon](../ide/how-to-locate-and-organize-project-and-item-templates.md).

## <a name="see-also"></a>Viz také:

- [Postupy: vytváření šablon projektu](../ide/how-to-create-project-templates.md)
- [Postupy: vytváření šablon položek](../ide/how-to-create-item-templates.md)
- [Parametry šablony](../ide/template-parameters.md)
- [Přizpůsobení šablony](../ide/customizing-project-and-item-templates.md)
- [Balíčky NuGet ve šablony sady Visual Studio](/nuget/visual-studio-extensibility/visual-studio-templates)