---
title: 'Krok 9: Vyzkoušejte jiné funkce'
ms.custom: ''
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: conceptual
ms.assetid: 1b0c5c80-e5a6-4f69-a4a4-0e89a82d4de0
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: bc842af3723a8b056d1de684bd798f4fda37cff8
ms.sourcegitcommit: 04a717340b4ab4efc82945fbb25dfe58add2ee4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
ms.locfileid: "32065075"
---
# <a name="step-9-try-other-features"></a>Krok 9: Vyzkoušejte jiné funkce
Chcete-li získat další informace, zkuste změnit ikony a barvy, přidat časovač hry a zvuky. Chcete-li, aby hra byla náročnější, zkuste zvětšit hrací plochu a upravte časovač.  
  
 Si můžete stáhnout dokončené verzi příkladu [dokončení odpovídající herní kurz ukázka](http://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).  
  
## <a name="to-try-other-features"></a>Vyzkoušení dalších funkcí  

-   Nahraďte ikony a barvy těmi, které zvolíte.  

    > [!TIP]
    >  Podívejte se na jmenovky [Forecolor](http://msdn.microsoft.com/library/system.windows.forms.control.forecolor.aspx) vlastnost.  

-   Přidejte časovač hry, který sleduje, jak dlouho hráči trvá, než vyhraje.  

    > [!TIP]
    >  K tomuto účelu můžete přidat popisek zobrazíte uplynulý čas na výše uvedeného formuláře <xref:System.Windows.Forms.TableLayoutPanel>, a přidejte další časovač do formuláře pro sledování času. Použijte kód ke spuštění časovače, když hráč zahájí hru, a zastavení časovače, jakmile hráč spojí poslední dvě ikony.  

-   Pokud hráč najde shodu, přidejte zvuk, jiný zvuk, když hráč odkryje dvě ikony, které neodpovídají, a třetí zvuk, když program znovu skryje ikony.  

    > [!TIP]
    >  Přehrávání zvuků, můžete použít <xref:System.Media> oboru názvů. V tématu [přehrání zvuků v aplikaci Windows Forms (C#)](http://youtu.be/qOh4ooHg1UU) nebo [postup přehrajte zvuk v jazyce Visual Basic](http://youtu.be/-4oPDeQrtMs) Další informace.  
  
-   Udělejte hru obtížnější tím, že zvětšíte hrací plochu.  

    > [!TIP]
    >  Budete potřebovat více než jen přidání řádků a sloupců do TableLayoutPanel - také musíte vzít v úvahu počet ikony, které vytvoříte.  

-   Udělejte hru náročnější tím, že skryjete první ikonu, pokud je hráč příliš pomalý a nezvolí druhou ikonu do vypršení určitého časového limitu.  

## <a name="to-continue-or-review"></a>Chcete-li pokračovat nebo přezkoumat  
  
-   Pokud si nevíte rady nebo máte otázky k programování, můžete zveřejnit svůj dotaz na jednom z diskuzních fór MSDN. V tématu [jazyka Visual Basic fórum](http://social.msdn.microsoft.com/Forums/home?forum=vbgeneral) a [Visual C# fórum](http://social.msdn.microsoft.com/Forums/home?forum=csharpgeneral).  
  
-   K dispozici jsou užitečné bezplatné video výukové materiály. Další informace o programování v jazyce Visual Basic, najdete v části [základy jazyka Visual Basic: vývoj pro začátečníky absolutní](http://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners). Další informace o programování v jazyce Visual C#, najdete v části [Základy C#: vývoj pro začátečníky absolutní](http://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners).  
  
-   Chcete-li vrátit k předchozímu kroku kurzu, přečtěte si téma [krok 8: Přidejte metodu k ověření, zda hráč vyhrál](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md).
