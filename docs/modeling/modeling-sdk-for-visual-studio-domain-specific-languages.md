---
title: Sada Modeling SDK pro sadu Visual Studio – jazyky domény
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language Tools
- Domain-Specific Language
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6dc87ba31e1f693559384977588471af753738e7
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2018
ms.locfileid: "31950839"
---
# <a name="modeling-sdk-for-visual-studio---domain-specific-languages"></a>Sada Modeling SDK pro sadu Visual Studio – jazyky domény
Pomocí sady SDK modelování pro [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], můžete vytvořit výkonné založené na modelu vývojové nástroje, které můžete integrovat do [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Stejným způsobem můžete vytvořit jednu nebo několik definic modelu a integrovat je do sady nástrojů.

 V centru MSDK je definice modelu, který je vytvořen, aby představoval pojmy v oblasti vašeho podnikání. Model s celou řadu nástrojů, jako je například graficky zobrazení, můžete obklopit možnost pro generování kódu a další artefakty příkazy pro transformaci v modelu a umožňuje interakci s kódem a jiných objektů nástroje [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Při vývoji lze model kombinovat s dalšími modely a nástroji, jež tvoří výkonnou sadu nástrojů, které jsou zaměřeny na vývoj.

 MSDK umožňuje rychlý vývoj modelu ve formě jazyka specifického pro doménu (DSL). Začínáte se speciálním editorem, kterým definujete schéma nebo abstraktní syntaxi a grafickou notaci. Z této definice vygeneruje VMSDK následující položky:

-   Model implementace s rozhraním API silného typu, který je spuštěn v obchodě založeném na transakcích.

-   Průzkumník založený na stromové architektuře.

-   Grafický editor, ve kterém uživatelé mohou zobrazit model nebo jeho části, které definujete.

-   Metody serializace, které uloží modely ve formátu XML pro čtení.

-   Zařízení pro generování programového kódu a jiných artefaktů pomocí šablonování textu.

 Můžete přizpůsobit a rozšířit všechny tyto funkce. Vaše rozšíření jsou integrována tak, že můžete i nadále aktualizovat definici DSL a znovu generovat funkce bez ztráty rozšíření.

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]

 [Příspěvky blogu související](https://blogs.msdn.microsoft.com/visualstudioalm/tag/code-index/)

 Pokyny k rozšířené postupy a řešení potíží, najdete v článku [Visual Studio DSL & modelování rozšíření nástrojů fórum](http://go.microsoft.com/fwlink/?LinkID=186074).

## <a name="in-this-section"></a>V tomto oddílu
 [Začínáme s jazyky specifickými pro doménu](../modeling/getting-started-with-domain-specific-languages.md)

 [Porozumění modelům, třídám a vztahům](../modeling/understanding-models-classes-and-relationships.md)

 [Jak se definuje jazyk specifický pro doménu](../modeling/how-to-define-a-domain-specific-language.md)

 [Přizpůsobení a rozšíření jazyka specifického pro doménu](../modeling/customizing-and-extending-a-domain-specific-language.md)

 [Ověřování v jazyce specifickém pro doménu](../modeling/validation-in-a-domain-specific-language.md)

 [Zápis kódu pro úpravu jazyka specifického pro doménu](../modeling/writing-code-to-customise-a-domain-specific-language.md)

 [Vytváření kódu z jazyka specifického pro doménu](../modeling/generating-code-from-a-domain-specific-language.md)

 [Porozumění kódu DSL](../modeling/understanding-the-dsl-code.md)

 [Přizpůsobení souborového úložiště a serializace XML](../modeling/customizing-file-storage-and-xml-serialization.md)

 [Nasazení řešení jazyka specifického pro doménu](../modeling/deploying-domain-specific-language-solutions.md)

 [Vytvoření jazyka specifického pro doménu založeného na modelu Windows Forms](../modeling/creating-a-windows-forms-based-domain-specific-language.md)

 [Vytvoření jazyka specifického pro doménu založeného na WPF](../modeling/creating-a-wpf-based-domain-specific-language.md)

 [Postupy: Rozšíření Návrháře DSL](../modeling/how-to-extend-the-domain-specific-language-designer.md)

 [Verze sady Visual Studio podporované pro Visualization & Modeling SDK](../modeling/supported-visual-studio-editions-for-visualization-amp-modeling-sdk.md)

 [Postupy: Migrace jazyka specifického pro doménu na novou verzi](../modeling/how-to-migrate-a-domain-specific-language-to-a-new-version.md)

 [Referenční dokumentace rozhraní API k sadě Modeling SDK pro Visual Studio](../modeling/api-reference-for-modeling-sdk-for-visual-studio.md)
