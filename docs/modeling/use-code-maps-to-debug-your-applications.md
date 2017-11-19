---
title: "Použití map kódu k ladění aplikací | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: get-started-article
helpviewer_keywords:
- Visual Studio Ultimate, visualizing code
- Visual Studio Ultimate, navigating code visually
- Visual Studio Ultimate, understanding code
- Visual Studio Ultimate, mapping code relationships
- Visual Studio Ultimate, code maps
- mapping code relationships
- code maps
- mapping relationships in code
ms.assetid: 9fd0c9a2-d351-40c8-be88-0749788264bf
caps.latest.revision: "49"
author: alexhomer1
ms.author: ahomer
manager: douge
ms.openlocfilehash: d9d1f6ac733a0feccb3f2fa8175fb85ed035b35c
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="use-code-maps-to-debug-your-applications"></a>Použití map kódu k ladění aplikací
Mapy kódu vám může pomoct vyhnout ztratili v rozsáhlých základů kódu, neznámého kódu nebo starší verze kódu. Například při ladění, budete možná muset podívejte se na kód napříč mnoha soubory a projekty. Použití map kódu k navigaci částí kódu a pochopit vztahy mezi nimi. Tímto způsobem, nemáte k udržování přehledu o tento kód ve vaší head nebo kreslení samostatné diagram. Takže když dojde k přerušení práci, kód mapuje nápovědy aktualizace vaší paměti o kód, který právě pracujete.  
  
 ![Mapa kódu & č. 45; Mapování vazeb v kódu](../modeling/media/codemapstoryboardpaint.png "CodeMapStoryboardPaint")  
  
 **Zelenou šipku ukazuje, kde se zobrazí v editoru kurzor**  
  
 Podrobnosti příkazů a akcích, které můžete použít při práci s map kódu najdete v tématu [Procházet a uspořádání map kódu](../modeling/browse-and-rearrange-code-maps.md).  
  
## <a name="understand-the-problem"></a>Pochopení problému  
 Předpokládejme, že je chyba v programu kreslení, na kterém právě pracujete. Chcete-li reprodukovat chyby, otevřete řešení v sadě Visual Studio a stiskněte klávesu **F5** spustit ladění.  
  
 Při kreslení čáry a zvolte **vrátit zpět Moje poslední tahu**, dokud kreslení na další řádek se nic nestane.  
  
 ![Mapa kódu & č. 45; Zkopírujte chyb](../modeling/media/codemapstoryboardpaint0.png "CodeMapStoryboardPaint0")  
  
 Takže spustíte tak, že na odstranění příčin `Undo` metoda. Najdete ho v `PaintCanvas` třídy.  
  
 ![Mapa kódu & č. 45; Najít kód](../modeling/media/codemapstoryboardpaint1.png "CodeMapStoryboardPaint1")  
  
## <a name="start-mapping-the-code"></a>Spuštění mapování kódu  
 Nyní spustit mapování `undo` metoda a jeho relace. Z editoru kódu můžete přidat `undo` metoda a polí, která odkazuje na novou mapu kódu. Když vytvoříte nové mapování, může zaindexování kódu trvat nějakou dobu. To pomáhá rychlejšímu běhu pozdějších operací.  
  
 ![Mapa kódu & č. 45; Zobrazit související pole a metoda](../modeling/media/codemapstoryboardpaint3.png "CodeMapStoryboardPaint3")  
  
> [!TIP]
>  Zelené zvýraznění zobrazí poslední položky, které byly přidány do mapy. Na zelenou šipku ukazuje kurzor na pozici v kódu. Šipky mezi položkami představují různé vztahy. Pohyb myši nad nimi a jejich popisy tlačítek prozkoumáním můžete získat další informace o položky na mapě.  
  
 ![Mapa kódu & č. 45; Zobrazit tipy](../modeling/media/codemapstoryboardpaint4.png "CodeMapStoryboardPaint4")  
  
## <a name="navigate-and-examine-code-from-the-map"></a>Procházení a zkoumání kódu z mapy  
 Viz definice kód pro každé pole, dvakrát klikněte na pole na mapě nebo vyberte pole a stiskněte klávesu **F12**. Zelená šipka se přesune mezi položkami na mapě. Kurzor v editoru kódu se také přesune automaticky.  
  
 ![Mapa kódu & č. 45; Zkontrolujte definici pole](../modeling/media/codemapstoryboardpaint5.png "CodeMapStoryboardPaint5")  
  
 ![Mapa kódu & č. 45; Zkontrolujte definici pole](../modeling/media/codemapstoryboardpaint5a.png "CodeMapStoryboardPaint5A")  
  
> [!TIP]
>  Zelenou šipku na mapě můžete také přesunout přesunutím kurzoru v editoru kódu.  
  
## <a name="understand-relationships-between-pieces-of-code"></a>Pochopení vztahů mezi částmi kódu  
 Teď chcete vědět, jaké další kód spolupracuje s `history` a `paintObjects` pole. Můžete do mapy přidat všechny metody, které odkazují na tato pole. Můžete to provést z mapy nebo z editoru kódu.  
  
 ![Mapa kódu & č. 45; Najít všechny odkazy](../modeling/media/codemapstoryboardpaint6.png "CodeMapStoryboardPaint6")  
  
 ![Otevření mapy kódu z editoru kódu](../modeling/media/codemapstoryboardpaint6a.PNG "CodeMapStoryboardPaint6A")  
  
> [!NOTE]
>  Pokud přidáte položky z projektu, jež jsou sdílena mezi více aplikacemi, jako je Windows Phone nebo Windows Store, pak tyto položky vždy zobrazí s projekt aktuálně aktivní aplikace na mapě. Ano Pokud změna kontextu na jiný projekt aplikace, pak kontext na mapě změní také pro nově přidané položky z sdílený projekt. Operace, které provádíte s položkou na mapě, se vztahují pouze na ty položky, které sdílejí stejný kontext.  
  
 Změňte rozložení a uspořádejte tak tok vztahů a usnadněte čtení z mapy. Položky kolem mapy lze také přesunout přetažením.  
  
 ![Mapa kódu & č. 45; Změna rozložení](../modeling/media/codemapstoryboardpaint7a.png "CodeMapStoryboardPaint7A")  
  
> [!TIP]
>  Ve výchozím nastavení **přírůstkové rozložení** je zapnutý. To při přidání nových položek mění uspořádání mapy co nejméně. Chcete-li změnit celý mapy pokaždé, když přidáte nové položky, vypněte **přírůstkové rozložení**.  
  
 ![Mapa kódu & č. 45; Změna rozložení](../modeling/media/codemapstoryboardpaint7.png "CodeMapStoryboardPaint7")  
  
 Podívejme se na tyto metody. Na mapě, dvakrát klikněte **PaintCanvas** metoda, nebo vyberte tato metoda a stiskněte klávesu **F12**. Zjistíte, že tato metoda vytvoří `history` a `paintObjects` jako prázdný seznamy.  
  
 ![Mapa kódu & č. 45; Zkontrolujte definici metody](../modeling/media/codemapstoryboardpaint8.png "CodeMapStoryboardPaint8")  
  
 Teď zopakujte stejný postup prozkoumat `clear` definici metody. Zjistíte, které `clear` provádí některé úlohy s `paintObjects` a `history`. Potom zavolá `Repaint` metoda.  
  
 ![Mapa kódu & č. 45; Zkontrolujte definici metody](../modeling/media/codemapstoryboardpaint9.png "CodeMapStoryboardPaint9")  
  
 Nyní zkontrolujte `addPaintObject` definici metody. Provádí taky některé úlohy s `history` a `paintObjects`. Také voláním `Repaint`.  
  
 ![Mapa kódu & č. 45; Zkontrolujte definici metody](../modeling/media/codemapstoryboardpaint10.png "CodeMapStoryboardPaint10")  
  
## <a name="find-the-problem-by-examining-the-map"></a>Nalezení příčiny problému prozkoumáním mapy  
 Zdá se, že všechny metody, které mění `history` a `paintObjects` volání `Repaint`. Ale `undo` není volání metody `Repaint`, i když `undo` upraví stejných polí. Proto si myslíte, že tento problém můžete vyřešit voláním `Repaint` z `undo`.  
  
 ![Mapa kódu & č. 45; Volání metody chybějící najít](../modeling/media/codemapstoryboardpaint11.png "CodeMapStoryboardPaint11")  
  
 Pokud by nebyla nastavena mapa k zobrazení tohoto chybějícího volání, mohlo by být nalezení tohoto problému obtížnější, zejména u složitějšího kódu.  
  
## <a name="share-your-discovery-and-next-steps"></a>Sdílení zjištění a další kroky  
 Předtím, než vy nebo někdo jiný tuto chybu vyřeší, si můžete dělat na mapě poznámky o problému a způsobu jeho řešení.  
  
 ![Mapa kódu & č. 45; Komentáře a příznak položky pro následnými](../modeling/media/codemapstoryboardpaint12.png "CodeMapStoryboardPaint12")  
  
 Můžete například přidat komentáře do mapy a označit položky pomocí barev.  
  
 ![Mapa kódu & č. 45; Označeno jako komentář a příznakem položky](../modeling/media/codemapstoryboardpaint12a.png "CodeMapStoryboardPaint12A")  
  
 Pokud máte nainstalovanou aplikaci Microsoft Outlook, můžete mapu e-mailem odeslat ostatním. Mapu taky můžete exportovat jako obrázek nebo jiný formát.  
  
 ![Mapa kódu & č. 45; Sdílené složky, exportovat, poštovní](../modeling/media/codemapstoryboardpaint13.png "CodeMapStoryboardPaint13")  
  
## <a name="fix-the-problem-and-show-what-you-did"></a>Vyřešení problému a zobrazení provedené činnosti  
 Pokud chcete vyřešit tuto chybu, přidejte volání pro `Repaint` k `undo`.  
  
 ![Mapa kódu & č. 45; Přidejte chybějící volání metody](../modeling/media/codemapstoryboardpaint14.png "CodeMapStoryboardPaint14")  
  
 Chcete-li potvrdit svou opravu, restartujte relaci ladění a zkuste chybu reprodukovat. Teď vyberete **vrátit zpět Moje poslední tahu** funguje podle očekávání a potvrdí provedené správná oprava.  
  
 ![Mapa kódu & č. 45; Potvrďte kód opravu](../modeling/media/codemapstoryboardpaint15.png "CodeMapStoryboardPaint15")  
  
 Můžete aktualizovat mapu, aby zobrazovala provedené opravy.  
  
 ![Mapa kódu & č. 45; Mapování aktualizace se chybí volání metody](../modeling/media/codemapstoryboardpaint16.png "CodeMapStoryboardPaint16")  
  
 Mapu nyní zobrazuje propojení mezi **vrátit zpět** a **překreslit**.  
  
 ![Mapa kódu & č. 45; Aktualizované mapa s volání metody](../modeling/media/codemapstoryboardpaint17.png "CodeMapStoryboardPaint17")  
  
> [!NOTE]
>  Při aktualizaci mapy se může zobrazit zpráva, že byl aktualizován index kódu použitý k vytvoření mapy. To znamená, že někdo změnil kód, což způsobilo, že se vaše mapa neshoduje s aktuálním kódem. To vám nezabrání v aktualizaci mapy, ale chcete-li ověřit, že mapa odpovídá kódu, pravděpodobně ji budete muset znovu vytvořit.  
  
 Nyní jste hotovi s šetření. Úspěšně jste našli a opravili problém pomocí mapování kódu. Máte k dispozici také mapu, která usnadňuje navigaci v rámci kódu, zapamatuje si, co jste se naučili, a zobrazí kroky, které jste provedli v zájmu vyřešení problému.  
  
## <a name="see-also"></a>Viz také  
 [Mapování metod v zásobníku volání při ladění](../debugger/map-methods-on-the-call-stack-while-debugging-in-visual-studio.md)   
 [Vizualizace kódu](../modeling/visualize-code.md)