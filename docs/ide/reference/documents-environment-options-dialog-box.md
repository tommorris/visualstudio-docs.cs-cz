---
title: Dokumenty, prostředí, dialogové okno Možnosti
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.Environment.Documents
- VS.ToolsOptionsPages.Environment.Documents
- VS.ToolsOptionsPag.Environment.Documents
helpviewer_keywords:
- Documents Environment Options dialog box
- defaults, directories
- error messages, customizing
- files [Visual Studio], default options
- files [Visual Basic], auto-loading modified
- windows, customizing environment
- in-memory editing
- folders [Visual Studio], specifying where Open File goes
- Open File dialog box
- windows, enabling re-use of current
- notifications, files changed
- files [Visual Studio], displaying in Solution Explorer
- default directories
- read-only files, editing
- Options dialog box, showing Miscellaneous Files
- directories [Visual Studio], IDE environment options
- Options dialog box, Documents page
- warnings, files changed
- Solution Explorer, displaying files in
ms.assetid: 4e3ccf1b-cd68-4db6-9470-710c911b47fc
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ceccf3c051e3c85fa4b8e64ecbc33c388e9a884f
ms.sourcegitcommit: 5b767247b3d819a99deb0dbce729a0562b9654ba
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/20/2018
ms.locfileid: "39178176"
---
# <a name="documents-environment-options-dialog-box"></a>Dokumenty, prostředí, dialogové okno Možnosti
Pomocí této stránky **možnosti** dialogové okno pro řízení zobrazování dokumentů v integrovaném vývojovém prostředí (IDE) a spravovat externí změny dokumentů a souborů. Toto dialogové okno se zpřístupní po kliknutí **možnosti** na **nástroje** nabídky a následným výběrem **dokumenty** v **prostředí** uzlu. Pokud **dokumenty** se nezobrazují v seznamu vyberte **zobrazit všechna nastavení** v **možnosti** dialogové okno.

> [!NOTE]
> Dostupné možnosti v dialogových oknech, názvy a umístění příkazů, které vidíte, mohou lišit od informací uvedených v nápovědě v závislosti na aktivních nastaveních nebo edici. Chcete-li změnit nastavení, zvolte **nastavení importu a exportu** na **nástroje** nabídky. Další informace najdete v tématu [přizpůsobení integrovaného vývojového prostředí sady Visual Studio](../../ide/personalizing-the-visual-studio-ide.md).


 **Znovu použít aktuální okno dokumentu, je-li uložit** při výběru, zavře aktuální dokument, pokud byla uložena a ve stejném okně se otevře nový dokument. Pokud vaše aktuální dokument nebyl uložen, zůstane otevřený a je otevřen nový dokument v samostatném okně. Tato možnost vybrána, nové dokumenty vždy otevře v samostatném systému windows.

 Tuto možnost použijte, pokud provádět více dokumentu vyjímání a operace vložení zřídka a chcete minimalizovat počet otevřené dokumenty a okna v váš pracovní prostor.

 **Rozpoznat, kdy soubor se změnil mimo prostředí** při výběru této možnosti zprávu okamžitě vás upozorní na změny otevřeného souboru, které byly provedeny pomocí editoru mimo rozhraní IDE. Zpráva umožňuje znovu načíst soubor ze služby storage.

 **Automaticky načíst změny, je-li uložit** případě, že máte **rozpoznat změnu souboru mimo prostředí** vybrané a otevření souboru v integrovaném vývojovém prostředí změny mimo rozhraní IDE, upozornění je vygenerována ve výchozím nastavení. Pokud je tato možnost povolena, bez upozornění se zobrazí a dokument je znovu načten v integrovaném vývojovém prostředí, aby se získaly externích změn.

 **Povolit úpravy souborů jen pro čtení. Zobrazit upozornění při pokusu o uložení** Pokud tato možnost bude nabídnuta můžete otevřít a upravit soubor jen pro čtení. Až skončíte, je nutné použít **uložit jako**příkazu pro uložení souboru podle nového názvu, pokud chcete uložit záznam změn.

 **Otevřít soubor pomocí adresáře aktuálně aktivního dokumentu** při výběru, tato možnost určuje, že **otevřít soubor** dialogové okno zobrazí adresář aktivního dokumentu. Pokud tato možnost vybrána, **otevřít soubor** dialogové okno zobrazí adresář naposledy použila k otevření souboru.

 **Kontrola konce řádků při načtení** tuto možnost mít editoru kontroly ukončení řádků v souboru a zobrazí okno se zprávou, pokud jsou zjištěny nekonzistence v formátování konce řádků.

 **Zobrazit upozornění, když se upraví globální akce zpět upravovat soubory** tuto možnost použijte pro zobrazení zprávy když **globální zpět** příkazu se vrátit zpět refaktoringu změny provedené v souborech, které byly změněny po operace refaktoringu. Vrací do stavu před Refaktoring souboru může zrušit změny provedené v souboru.

 **Zobrazit různé soubory v Průzkumníku řešení** výběr této možnosti se zobrazí **různé soubory** uzel v **Průzkumníka řešení**. Různé soubory jsou soubory, které nejsou přiřazeny k projektu nebo řešení, ale může objevit v **Průzkumníka řešení** pro vaše pohodlí.

> [!NOTE]
> Vyberte tuto možnost **zobrazit v prohlížeči** příkaz **souboru** nabídku webové dokumenty, které nejsou součástí webovou aplikaci služby active.

 **\<** *n* **> položek uložených v ostatních souborech projektu** určuje počet souborů pro uchování v **MiscellaneousFiles** složky **Průzkumníka řešení**. Tyto soubory jsou uvedené i v případě, že už nejsou otevřená v editoru. Můžete zadat libovolný celé číslo od 0 do 256. Výchozí hodnota je 0.

 Například pokud se tato možnost nastavena na 5 a máte 10 různé soubory otevřené po zavření všech 10 souborů, první 5 stále v zobrazí **různé soubory** složky.

 **Pokud data nelze uložit v znakové stránce uložit dokumenty znakové sady Unicode** výběrem této možnosti způsobí soubory, které obsahují informace, které jsou kompatibilní s vybranou znakovou stránku, která se má uložit jako Unicode ve výchozím nastavení.

## <a name="see-also"></a>Viz také

- [Prostředí, dialogové okno Možnosti](../../ide/reference/environment-options-dialog-box.md)
- [Složka Ostatní soubory](../../ide/reference/miscellaneous-files.md)
- [Hledání a nahrazení textu](../../ide/finding-and-replacing-text.md)