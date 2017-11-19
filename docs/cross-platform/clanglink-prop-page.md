---
title: Clang Linkeru vlastnosti (Android C++) | Microsoft Docs
ms.custom: 
ms.date: 10/23/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 66e88848-116c-4eb0-bc57-183394d35b57
author: corob
ms.author: mblome
manager: ghogen
f1_keywords:
- VC.Project.VCLinkerTool.OutputFile
- VC.Project.VCLinkerTool.ShowProgress
- VC.Project.VCLinkerTool.Version
- VC.Project.VCLinkerTool.VerboseOutput
- VC.Project.VCLinkerTool.IncrementalLink
- VC.Project.VCLinkerTool.SharedLibrarySearchPath
- VC.Project.VCLinkerTool.AdditionalLibraryDirectories
- VC.Project.VCLinkerTool.UnresolvedReferences
- VC.Project.VCLinkerTool.OptimizeForMemory
- VC.Project.VCLinkerTool.IgnoreDefaultLibraryNames
- VC.Project.VCLinkerTool.ForceSymbolReferences
- VC.Project.VCLinkerTool.ForceFileOutput
- VC.Project.VCLinkerTool.OmitDebuggerSymbolInformation
- VC.Project.VCLinkerTool.GenerateMapFile
- VC.Project.VCLinkerTool.Relocation
- VC.Project.VCLinkerTool.FunctionBinding
- VC.Project.VCLinkerTool.NoExecStackRequired
- VC.Project.WholeArchive
- VC.Project.AdditionalOptionsPage
- VC.Project.VCLinkerTool.AdditionalDependencies
- VC.Project.VCLinkerTool.LibraryDependencies
ms.openlocfilehash: 0e7b1d5b417250282092a780afc30aee965e4dfa
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="clang-linker-properties-android-c"></a>Vlastnosti Linkeru clang (Android C++)

Vlastnost | Popis | Možnosti
--- | ---| ---
Výstupní soubor | Možnost přepíše výchozí název a umístění program, který vytvoří linkeru. (-o).
Ukázat průběh | Zprávy o průběhu Linkeru výtisků.
Version | -Verze informuje – možnost linkeru uvést číslo verze v hlavičce ke spustitelnému souboru.
Povolit podrobný výstup | -Verbose – možnost informuje linkeru pro výstup podrobných zpráv pro ladění.
Povolit přírůstkové propojování | Možnost informuje linkeru Povolit přírůstkové propojování.
Sdílené knihovny cesty pro hledání | Umožňuje uživateli k naplnění cesta hledání sdílenou knihovnu.
Další knihovny adresáře | Umožňuje uživateli přepsat cestu prostředí knihovny. (-L složku).
Odkazy na symboly nerozpoznané sestavy | Tuto možnost, pokud je povoleno oznámí odkazy na symboly nevyřešená.
Optimalizace pro využití paměti | Optimalizujte pro využití paměti rereading tabulky symbolů podle potřeby.
Ignorovat konkrétní výchozí knihovny | Určuje jeden nebo více názvů výchozí knihovny ignorovat.
Vynutit odkazy na symboly | Vynutí symbolu, které je třeba zadat ve výstupním souboru jako nedefinované symbol.
Ladicí program informací o symbolu | Ladicí program informací o symbolu z výstupního souboru. | **Zahrnout všechny**<br>**Vynechat nepotřebné symboly pro zpracování přemístění**<br>**Vynechat pouze informace symbolu ladicí program**<br>**Vynechat všech informací o symbolu**<br>
Balíček informací o symbolu ladicí program | Odstranit informace symboly ladicí program před balení.  Kopii původní binárního souboru se použije pro ladění.
Mapování názvu souboru | Možnost mapy informuje linkeru pro vytvoření souboru s mapováním se zadaným názvem uživatele.
Po přemístění označte proměnné určené jen pro čtení | Tato možnost označí proměnné jen pro čtení po přemístění.
Povolit okamžitou funkce vazby | Tato možnost označí objektu pro vazbu okamžitou funkce.
Vyžadovat spustitelné zásobníku | Tato možnost označí výstup jako nevyžadující spustitelné zásobníku.
Celý archivu | Celý archivu používá všechny kódu ze zdroje a další závislosti.
Další možnosti | Další možnosti.
Další závislosti | Určuje další položek, které chcete přidat do příkazového řádku odkaz.
Závislosti knihovny | Tato možnost umožňuje zadat další knihovny pro přidání do příkazového řádku linkeru. Další knihovny přidá na konec spuštění příkazového řádku linkeru s 'lib' a konec s '.a' nebo '.so' rozšíření.  (-lFILE)