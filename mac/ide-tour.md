---
title: "Visual Studio pro Mac prohlídka | Microsoft Docs"
description: "Visual Studio pro Mac poskytuje integrované vývojové prostředí pro sestavení aplikací .NET v systému macOS, včetně webů ASP.NET Core a projekty Xamarin pro iOS, Android, Mac a Xamarin.Forms."
author: asb3993
ms.author: amburns
ms.date: 04/14/2017
ms.topic: article
ms.assetid: 7DC64A52-AA41-4F3A-A8A1-8A20BCD81CC7
ms.openlocfilehash: 0f8f3ba04d4e5a8949bc57cb8cf61d470690d786
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="visual-studio-for-mac-tour"></a>Visual Studio pro Mac prohlídka

Visual Studio pro Mac zpracovaní integrovaného vývojového prostředí zaměřené na mobilní telefon pro Xamarin, Xamarin Studio do prostředí pro vývoj mobilních první, první cloudu na Mac. Tento nástroj zaměřené na vývojáře umožňuje využít síly rozhraní .NET k vytváření aplikací pro všechny platformy, které musí vaši uživatelé.

Prostředí uživatele (UX) sady Visual Studio pro Mac je podobná jeho protějšku Windows, ale s nativní systému macOS chování. Vytvoření, otevření nebo vyvíjející aplikaci, bude známou vlastnost pro každý, kdo má použil Visual Studio v systému Windows. Kromě toho Visual Studio pro Mac využívá řadu výkonné nástroje, které jeho protějšku Windows výkonné IDE. Platforma kompilátoru Roslyn se používá pro refaktoring a technologii IntelliSense. Použijte jeho stroje systému a sestavení projektu MSBuild a její zdroj editor podporuje TextMate sady. Používá stejný motory ladicí program pro aplikace Xamarin a .NET Core a stejné návrháře pro Xamarin.iOS a Xamarin.Android.

Tento článek popisuje různé části sady Visual Studio pro Mac, poskytuje podívejte se na některé z funkcí, které umožňují výkonný nástroj pro vytváření aplikací pro různé platformy.

## <a name="ide-tour"></a>Prohlídka IDE

Visual Studio pro Mac jsou uspořádány do několika oddílů pro správu souborů aplikace a nastavení, vytváření kódu aplikace a ladění.

## <a name="welcome-screen"></a>Úvodní obrazovka

Při spuštění aplikace Visual Studio pro Mac zobrazí *úvodní obrazovce* jak je uvedeno níže:

![Úvodní obrazovka](media/ide-tour-image1.png)

Na úvodní obrazovce obsahuje následující části:

- **Panel nástrojů** -poskytuje rychlý přístup k panelu vyhledávání. Při řešení je načtena, slouží k nastavení konfigurací aplikace, pro ladění a pro zobrazení chyb.
- **Začínáme** -poskytuje rychlý přístup k užitečné témata pro vývojáře Začínáme s Visual Studio for Mac.
- **Poslední řešení** -poskytuje rychlý přístup k naposledy otevřeného řešení, jakož i vhodného tlačítka otevírání nebo vytváření projektů.
- **Novinky pro vývojáře** -informačního kanálu, který zajišťuje aktuální na nejnovější informace o Microsoft Developer.

## <a name="solutions-and-projects"></a>Řešení a projekty

Následující obrázek ukazuje Visual Studio pro Mac pomocí aplikace pro načíst:

![Visual Studio pro Mac pomocí aplikace pro načíst](media/ide-tour-image17.png)

V následujících částech najdete přehled hlavními oblastmi v sadě Visual Studio for Mac.

## <a name="solution-pad"></a>Odsazení řešení

Odsazení řešení slouží k uspořádání projekty v řešení, jak je uvedeno níže:

![Uspořádány v řešení pro projekty](media/ide-tour-image18.png)

Toto je, kde soubory pro zdrojový kód, prostředky, uživatelské rozhraní a závislosti jsou uspořádány do projektů specifické pro platformu.

Další informace o použití projekty a řešení v sadě Visual Studio pro Mac, najdete v části [projekty a řešení](~/projects-and-solutions.md) tématu.

## <a name="assembly-references"></a>Odkazy na sestavení
 
Odkazy na sestavení pro každý projekt, jsou k dispozici v části níže zobrazené složky odkazů:

![Složky odkazů v řešení odsazení](media/ide-tour-image19.png)

Další odkazy lze přidat pomocí **upravit odkazy** dialog, který se zobrazí dvojitým kliknutím na odkazy na složku, nebo výběrem **upravit odkazy** na jeho kontextové nabídky akce:
 
![Odkazy na dialogové okno Upravit](media/ide-tour-image20.png)

Další informace o použití odkazy v sadě Visual Studio pro Mac, najdete v části [Správa odkazů v projektu](~/managing-references-in-a-project.md) tématu.

## <a name="dependencies--packages"></a>Závislosti / balíčků

Všechny externí závislosti, které používají ve vaší aplikaci jsou uloženy ve složce závislosti nebo balíčky, podle toho, pokud jste v .net Core nebo Xamarin.iOS/Xamarin.Android projektu. To se obvykle poskytují ve formě NuGet, nebo komponentou.

NuGet je nejoblíbenější Správce balíčků pro .NET – vývoj. S podporou NuGet sady Visual Studio můžete snadno vyhledat a přidat balíčky do projektu do aplikace.

Pokud chcete přidat závislost do vaší aplikace, klikněte pravým tlačítkem na závislosti / balíčky složky a vyberte **přidat balíčky**:

![Přidání balíčku NuGet](media/ide-tour-image21.png)

Informace o použití balíčku NuGet v aplikaci najdete v [projektu včetně NuGet ve vašem projektu](~/nuget-walkthrough.md) tématu.

## <a name="refactoring"></a>Refaktoring

Visual Studio pro Mac nabízí dva způsoby užitečné Refaktorovat kódu: kontextu akce a analýzy zdroje. Další informace o nich [Refactoring](~/refactoring.md) tématu.

## <a name="debugging"></a>Ladění

Visual Studio pro Mac má nativní ladicí program povolení ladění podporu pro aplikace Xamarin.iOS, Xamarin.Mac a Xamarin.Android. Visual Studio pro Mac používá Mono logicky ladicího programu, které je implementované do Mono modulu runtime, což IDE k ladění spravovaného kódu pro všechny platformy. Další informace o ladění webu [ladění](~/debugging.md) tématu.

Ladicí program obsahuje bohatou vizualizérech pro speciální typy například řetězce, barvy, adresy URL, jakož i velikostí, souřadnice a Bézierových křivek.

Další informace o vizualizaci dat ladicího programu, přejděte [vizualizaci dat](~/data-visualizations.md) tématu.

## <a name="version-control"></a>Správa verzí

Visual Studio pro Mac se integruje s Git a Subversion zdrojových systémů řízení. Projekty ve správě zdrojového kódu, jsou označeny větev uvedené vedle názvu řešení: 

![Název větve udávajících projektu ve správě zdrojového kódu](media/ide-tour-image22.png)

Soubory s nepotvrzené změnit mají poznámky na jejich ikony v podokně řešení, jak je uvedeno níže:

![Nepotvrzené soubory v řešení odsazení](media/ide-tour-image23.png)

Další informace o použití správy verzí v sadě Visual Studio, najdete v části [verzí](~/version-control.md) tématu.