---
title: "ID pracovního vytížení a součást Visual Studio zpětnou vazbu klienta 2017 | Microsoft Docs"
description: "Použijte identifikátory pracovního vytížení a součást Visual Studio k poskytnutí zpětné vazby bohaté pro Visual Studio Team Services nebo Team Foundation Server"
keywords: 
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.date: 10/09/2017
ms.topic: article
helpviewer_keywords:
- workload ID, Visual Studio
- component ID, Visual Studio
- install Visual Studio, administrator guide
ms.service: 
ms.technology: vs-ide-install
ms.assetid: 7392a100-100c-458c-9394-828695109015
ms.openlocfilehash: 53c6c8e3a715a4dfd085fe4df7fb8ad098d21ccd
ms.sourcegitcommit: 2c7f48ad6073a81fa927568793633f26cc1f0b15
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2017
---
# <a name="visual-studio-feedback-client-2017-component-directory"></a>Visual Studio zpětnou vazbu klienta 2017 součástí adresáře

V tabulkách na této stránce najdete ID, které můžete použít k instalaci sady Visual Studio pomocí příkazového řádku. Všimněte si, že přidáme další součásti, jako jsme vydání aktualizace pro Visual Studio.

Všimněte si také následující stránka:

* Každé zatížení má vlastní části, a potom podle ID úlohy a tabulku součásti, které jsou k dispozici pro pracovní vytížení.
* Ve výchozím nastavení **požadované** součásti se nainstalují při instalaci zatížení. Pokud zvolíte možnost, můžete taky nainstalovat **doporučeno** a **volitelné** součásti.
* Přidali jsme také oddíl, který uvádí další součásti, které nejsou spojit s jakoukoli úlohu.

Další informace o tom, jak používat tyto identifikátory najdete v tématu [pomocí parametrů příkazového řádku pro instalaci Visual Studio 2017](use-command-line-parameters-to-install-visual-studio.md) stránky. A seznam úloh a ID součástí pro ostatní produkty, naleznete v části [zatížení 2017 Visual Studio a ID součástí](workload-and-component-ids.md) stránky.

## <a name="feedback-client"></a>Feedback Client

**ID:** Microsoft.VisualStudio.Workload.FeedbackClient

**Popis:** klienta Feedback client umožňuje zúčastněným stranám k poskytnutí zpětné vazby bohaté pro Visual Studio Team Services nebo Team Foundation Server.

### <a name="components-included-by-this-workload"></a>Součásti zahrnuté tímto zatížením

ID součásti | Název | Version | Typ závislosti
--- | --- | --- | ---
Microsoft.VisualStudio.Component.TestTools.FeedbackClient | Microsoft Feedback Client | 15.0.26711.1 | Požadováno

## <a name="unaffiliated-components"></a>Nezávislou na komponenty

Toto jsou součásti, které nejsou součástí žádné úlohy, ale může být vybraný jako jednotlivé součásti.

ID součásti | Název | Version
--- | --- | ---
není k dispozici | není k dispozici | není k dispozici

## <a name="get-support"></a>Získat podporu
V některých případech může problémů. Pokud se nezdaří instalace Visual Studia, najdete v článku [problémy instalace a upgrade řešení potíží s Visual Studio 2017](troubleshooting-installation-issues.md) stránku Tipy pro odstraňování potíží. Taky můžete hlášení problémů produktu pro nás prostřednictvím [nahlásit problém](../ide/how-to-report-a-problem-with-visual-studio-2017.md) nástroj v prostředí Visual Studio IDE nebo ke sdílení návrh s nám na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Můžete sledovat problémy produktu v [Visual Studio Community vývojáře](https://developercommunity.visualstudio.com/)a klást otázky a odpovědi. Můžete také použít s námi a jinými vývojáři Visual Studio prostřednictvím našich [Visual Studio konverzace v komunitě Gitter](https://gitter.im/Microsoft/VisualStudio) (vyžaduje [Githubu](https://github.com/) účtu).

## <a name="see-also"></a>Viz také

* [ID úlohy a součást Visual Studio](workload-and-component-ids.md)
* [Příručka správce Visual Studio](visual-studio-administrator-guide.md)
* [Používání parametrů příkazového řádku pro instalaci sady Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
  * [Příklady parametr příkazového řádku](command-line-parameter-examples.md)
* [Vytvoření offline instalace sady Visual Studio](create-an-offline-installation-of-visual-studio.md)