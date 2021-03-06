---
title: Nástroj WhiteSource Bolt Benefit | Dokumentace Microsoftu
author: evanwindom
ms.author: jaunger
manager: evelynp
ms.date: 01/11/2017
ms.topic: Get-Started-Article
description: Zjistěte, jak chcete předplatné aktivovat, nástroj WhiteSource Bolt je součástí předplatného sady Visual Studio.
ms.prod: vs-subscription
ms.technology: vs-subscriptions
searchscope: VS Subscription
ms.openlocfilehash: a7c384a8bc4b84aea4982bd195b0d92820c68ecb
ms.sourcegitcommit: a749c287ec7d54148505978e8ca55ccd406b71ee
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/21/2018
ms.locfileid: "46542348"
---
#  <a name="whitesource-bolt-in-visual-studio-subscriptions"></a>Nástroj WhiteSource Bolt v předplatných sady Visual Studio

Vyhledejte a opravte slabá místa opensourcového kódu a generovat komplexní inventární a licenční sestavy všech opensourcových komponent ve vašem buildu. Některá předplatná sady Visual Studio zahrnují bezplatný přístup za šest měsíců.

## <a name="activation-steps"></a>Postup aktivace

1.  K aktivaci vaší výhody nástroj WhiteSource Bolt, přihlaste se k [ https://my.visualstudio.com/benefits ](https://my.visualstudio.com/benefits?wt.mc_id=o~msft~docs) .

2.  Vyhledejte dlaždici nástroj WhiteSource Bolt v části nástroje a klikněte na **získat kód** odkaz v dolní části dlaždice výhodu.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhodu dlaždice](_img\vs-whitesource\vs-whitesource-tile.png)

2.  Obdržíte oznámení zobrazení aktivační kód.  **Zkopírujte kód do vaší schránky**, pak klikněte na tlačítko **aktivovat**.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhodu kódu ](_img\vs-whitesource\vs-whitesource-code.png)

3.  Na webové stránce WhiteSource, klikněte na **aktivovat** tlačítko nebo přejděte dolů k položce **aktivaci účtu** části stránky.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhodu aktivovat](_img\vs-whitesource\vs-whitesource-activate-page-cropped.png)

4.  V **aktivaci účtu** části stránky, provedeme vás provede čtyři kroky:

    - [Nainstalujte](https://marketplace.visualstudio.com/items?itemName=whitesource.ws-bolt) nástroj WhiteSource Bolt rozšíření sady Microsoft Visual Studio Marketplace. Pokud nemáte oprávnění k instalaci rozšíření, přečtěte si téma [instalovat bezplatná rozšíření pro služby Azure DevOps](/azure/devops/marketplace/install-vsts-extension?view=vsts).


    Klikněte na zelené **nainstalovat** tlačítko, pokud používáte Azure DevOps služby, nebo **Stáhnout** tlačítko pro Team Foundation Server.  V tomto příkladu budeme používat služby Azure DevOps.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhody instalace rozšíření](_img\vs-whitesource\vs-whitesource-download-install.png)

    - V dalším kroku vyberte Azure DevOps organizace, kterou chcete použít a klikněte na tlačítko **potvrdit**.  (Pokud ještě jste nenastavili DevOps služby Azure, přejděte [výhody](https://my.visualstudio.com/benefits) stránce a aktivaci vaší výhody služeb Azure DevOps.)

    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhodu potvrzení účtu](_img\vs-whitesource\vs-whitesource-confirm-account.png)

    - Se zobrazí potvrzení, že rozšíření je nainstalované a připravené k použití.  Klikněte na tlačítko **Začínáme** se vraťte na stránku nástroj WhiteSource Bolt a pokračovat.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhody instalace dokončena](_img\vs-whitesource\vs-whitesource-install-complete.png)

5.  Otevřete řídicí panel Projekt Azure DevOps, klikněte na **kanály Azure** nabídku a zvolte **nástroj WhiteSource Bolt**.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhodu přidat rozšíření](_img\vs-whitesource\vs-whitesource-installed-cropped.png)

6. Vložte aktivační kód z dlaždice nástroj WhiteSource Bolt výhoda a klikněte na tlačítko **aktivovat**. Každá aktivační kódy je možné aktivovat pouze jeden projekt.
    > [!div class="mx-imgBorder"]
    > ![WhiteSource výhodu aktivovat kódu](_img\vs-whitesource\vs-whitesource-activate-code-cropped.png)

7.  S aktivací je tak dokončená a budete mít 180 dní zbývajících v rámci předplatného.

8.  Bude potřeba přidat rozšíření nástroj WhiteSource Bolt jako jeden z kroků sestavení.  Video je k dispozici na [nástroj WhiteSource Bolt stránky](https://www.whitesourcesoftware.com/whitesource_bolt_visualstudio_2017/#activate) ukáže, jak.

9. Jakmile jste si vyzkoušeli vaše sestavení, následující komplexní sestavy a řídicí panely se vygeneruje automaticky:
    - Řídicí panel zabezpečení ohrožení zabezpečení
    - Sestava zabezpečení ohrožení zabezpečení
    - Zastaralé knihovny sestav
    - Řídicí panel licence rizik a dodržování předpisů
    - Sestava inventáře

## <a name="eligibility"></a>Způsobilost

| Úroveň předplatného                                                 |     Kanály                                            | Výhody                                                          | Obnovitelné?    |
|--------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------|---------------|
| Visual Studio Enterprise (standardní a roční cloudové)   | VL, Azure, maloobchod, vybrali NFR<sup>1</sup> | 6 měsíců       |  Ano          |
| Visual Studio Professional (standardní a roční cloudové) | VL, Azure, maloobchodního prodeje                                       | Není k dispozici                                                           |NENÍ K DISPOZICI         |
| Visual Studio Test Professional (Standard)                         | VL maloobchodního prodeje                                              | Není k dispozici                                             |  NENÍ K DISPOZICI         |
| Předplatné MSDN Platforms (Standard)                                          | VL maloobchodního prodeje                                              | Není k dispozici                                              | NENÍ K DISPOZICI         |
| Visual Studio Dev Essentials | NENÍ K DISPOZICI  | Není k dispozici |NENÍ K DISPOZICI |
| Visual Studio Enterprise, Visual Studio Professional (měsíční cloud) | Azure                                       | Není k dispozici                                                           |NENÍ K DISPOZICI|

<sup>1</sup>*zahrnuje: Microsoft Partner Network (Enterprise).  Vyloučí: Jiné není pro prodej (NFR), Visual Studio Industry Partner (VSIP), FTE, MCT Software & Services pro vývojáře, BizSpark, Imagine, Vážíme si toho partnera Microsoftu (MVP), ředitel pro oblast (RD), MCT Software & Services, Microsoft Partner Network () Professional).*

Nejste si jistí které předplatné používáte?  Připojte se k [ https://my.visualstudio.com/subscriptions ](https://my.visualstudio.com/subscriptions?wt.mc_id=o~msft~docs) zobrazíte všechna předplatná, která jsou přiřazená e-mailovou adresu. Pokud se nezobrazí všechna předplatná, může mít jeden nebo více přiřazené na jinou e-mailovou adresu.  Bude potřeba přihlásit se přes tento e-mailovou adresu najdete v těchto předplatných.

## <a name="support-resources"></a>Informační zdroje podpory

-  Potřebujete pomoc s nástroj WhiteSource Bolt?  Chat s nástroj WhiteSource Bolt zástupce v za provozu https://www.whitesourcesoftware.com/vse_whitesource_bolt/
-  Potřebujete pomoc se prodeje, předplatnými, účty a fakturací pro předplatná sady Visual Studio, obraťte se na Visual Studio [podpora předplatných](https://visualstudio.microsoft.com/subscriptions/support/).
-  Máte dotaz k Visual Studio IDE, DevOps služby Azure nebo jiných produktů Visual Studio nebo služeb?  Navštivte [Visual Studio – podpora](https://visualstudio.microsoft.com/support/).