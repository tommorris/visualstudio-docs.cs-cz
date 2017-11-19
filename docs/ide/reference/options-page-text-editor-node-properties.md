---
title: "Stránka Možnosti, vlastnosti uzlu textového editoru | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Tools Options settings, Text Editor node properties
- automation [Visual Studio], controlling Tools Options
ms.assetid: 19438302-0677-4f4d-9720-5667e6a22ab2
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5a917167b8e81445d0ec47a1dd44cf74f5d87d4f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="options-page-text-editor-node-properties"></a>Stránka Možnosti, vlastnosti uzlu textového editoru
Tento dokument popisuje některé stránky (nebo vlastnosti kolekce), jsou přidružené **textového editoru** kategorie, `DTE.Properties("TextEditor", <Property Page>)`, z **možnosti** dialogové okno. Název každé část je hovoru, který se používá pro přístup k `Properties` kolekce a tabulkou v každou část jsou uvedeny vlastnosti v kolekci.  
  
 Makra jazyka Visual Basic v [řízení nastavení možnosti](http://msdn.microsoft.com/Library/a09ed242-7494-4cde-bbd1-7a8ec617965d) ukazují, jak zobrazit aktuální možnosti a jejich hodnoty pro každou stránku **možnosti** dialogové okno.  
  
## <a name="general"></a>Obecné  
 `DTE.Properties("TextEditor", "General")`  
  
|Název položky vlastnosti|Hodnota|Popis|  
|------------------------|-----------|-----------------|  
|GoToAnchorAfterEscape|Get/Set (Boolean)|Pokud `True`, stisknutí řídicí při výběru způsobí, že bod vložení přesunout do kterého byla spuštěna akce, který vytvořili výběr. `False`Posune kurzor na konec výběru.|  
|DragNDropTextEditing|Get/Set (Boolean)|Určuje, zda lze při operacích kopírování nebo vyjmutí a vložení vybranou oblast textu přetáhnout v dokumentu z jednoho místa do jiného.|  
|HorizontalScrollBar|Get/Set (Boolean)|Určuje, zda se v oknech editoru zobrazuje vodorovný posuvník.|  
|VerticalScrollBar|Get/Set (Boolean)|Určuje, zda se v oknech editoru zobrazuje svislý posuvník.|  
|SelectionMargin|Get/Set (Boolean)|Určuje, zda je na levé straně podokna textu místo pro speciální operace výběru, ikony pro kreslení zarážek atd.|  
|MarginIndicatorBar|Get/Set (Boolean)|Určuje, zda se zobrazuje svislá čára, která odděluje levý okraj podokna textu od hlavní části tohoto podokna.|  
|UndoCaretActions|Get/Set (Boolean)|Pokud `True`. operace vrácení zpět zahrnují pohybu bod vložení, výběr příkazy a tak dále, kromě úpravy akcí, které upravují vyrovnávací paměti.|  
|AutoDelimiterHighlighting|Get/Set (Boolean)|Určuje, zda při zadání koncového oddělovače zvýrazní editor počáteční oddělovač. Editor vždy zobrazí počáteční oddělovač tučně bez ohledu na hodnotu této vlastnosti.|  
|EditorEmulation|Get/Set (Enum)||  
|DetectUTF8WithoutSignature|Get/Set (Boolean)|Zjistí, zda soubor používá kódování UTF-8, pokud nemá signaturu kódování.|  
|TrackChanges|Get/Set (Boolean)||  
  
## <a name="plain-text"></a>Prostý text  
 `DTE.Properties("TextEditor", "PlainText")`  
  
 `PlainText` Možností editoru vliv na nastavení editoru při úpravách textových souborů. Každý programovací jazyk a [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] balíčku má svou vlastní konkrétní **textového editoru** nastavení. Například pro zobrazení nebo změny [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] použít nastavení editoru `DTE.Properties("TextEditor", "CSharp") or DTE.Properties("TextEditor", "CSharp-Specific")`. Pro **skript SQL** použít nastavení editoru `DTE.Properties("TextEditor", "SQL ")`.  
  
|Název položky vlastnosti|Hodnota|Popis|  
|------------------------|-----------|-----------------|  
|AutoListMembers|Get/Set (Boolean)|Určuje, zda se automaticky zobrazí dostupný seznam členů, když uživatel zadá za odkaz na proměnnou tečku.|  
|AutoListParams|Get/Set (Boolean)|Určuje, zda se automaticky zobrazí popis seznamu argumentů, když uživatel zadá za název funkce závorku (.|  
|HideAdvancedMembers|Get/Set (Boolean)|Určuje, zda se mají v seznamech doplňování výrazů vypisovat všechny členy nebo pouze nejpoužívanější.|  
|VirtualSpace|Get/Set (Boolean)|Určuje, zda se prázdné znaky zobrazují jako grafika. Toto nastavení na `true` způsobí, že `WordWrap` vlastnost položky (v tomto seznamu) na hodnotu `false`.|  
|WordWrap|Get/Set (Boolean)|Určuje, zda se dlouhé řádky v tomto zobrazení zalamují na hranicích slov. Toto nastavení na `true` způsobí, že `VirtualSpace` vlastnost položky (v tomto seznamu) na hodnotu `false`.|  
|WordWrapGlyphs|Get/Set (Boolean)|Zobrazí piktogram na konci řádku; označuje, že se tento řádek zalamuje na další řádek.|  
|EnableLeftClickForURLs|Get/Set (Boolean)|Určuje, zda editor podtrhuje adresy URL a umožňuje v systémem zaregistrovaném webovém prohlížeči přejít na tuto adresu URL jedním kliknutím.|  
|IndentStyle|Get/Set (<xref:EnvDTE.vsIndentStyle>)|Určuje styl odsazení: výchozí, inteligentní nebo žádné.|  
|TabSize|Get/Set (Long)|Představuje počet mezer pro tabulátor. Nastavení celého čísla mimo rozsah 1–60 (včetně) se nezdaří.|  
|InsertTabs|Get/Set (Boolean)|Pokud `True`, jsou použity znaky KARTĚ, pokud se používá odsazení.|  
|IndentSize|Get/Set (Long)|Představuje počet mezer pro jednu úroveň odsazení. Nastavení celočíselné hodnoty mimo rozsah 1–60 (včetně) se nezdaří.|  
|ShowLineNumbers|Get/Set (Boolean)|Určuje, zda se při zobrazení dokumentu v základním editoru zobrazují na levém okraji čísla řádků.|  
|ShowNavigationBar|Get/Set (Boolean)|Určuje, zda se v horní části oken editoru zobrazují rozevírací seznamy a tlačítka.|  
|CutCopyBlankLines|Get/Set (Boolean)|Vyjme nebo zkopíruje prázdné řádky, pokud jsou vybrány.|  
  
## <a name="see-also"></a>Viz také  
 [Ovládání možnosti nastavení](http://msdn.microsoft.com/Library/a09ed242-7494-4cde-bbd1-7a8ec617965d)   
 [Určení názvů vlastností položky na stránkách možnosti](http://msdn.microsoft.com/Library/d450422d-47c7-4eeb-9f9f-3286264bc5aa)   
 [Stránka Možnosti, vlastnosti uzlu prostředí](../../ide/reference/options-page-environment-node-properties.md)   
 [Stránka Možnosti, písma a barvy vlastnosti uzlu](../../ide/reference/options-page-fonts-and-colors-node-properties.md)