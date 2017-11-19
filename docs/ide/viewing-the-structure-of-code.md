---
title: "Zobrazení struktury kódu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.documentoutline.window
- vs.objectbrowser
- vs.classview
- VS.CodeDefinitionView
- VS.CodeDefinitionWindow
- vs.componentpicker
- vs.callbrowser
helpviewer_keywords:
- document outline window.
- Visual Studio, object browser
- Visual Studio, code definition window
- call hierarchy
- Visual Studio, document outline window
- code definition window
- Visual Studio, class view
- Visual Studio, call hierarchy window
- class view
- object browser
ms.assetid: e6064f58-5ad9-4f05-8c3f-12e994b6583f
caps.latest.revision: "28"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f85bcde09d6748aa781ceefd85ccbf138245aca6
ms.sourcegitcommit: ec1c7e7e3349d2f3a4dc027e7cfca840c029367d
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2017
---
# <a name="viewing-the-structure-of-code"></a>Zobrazení struktury kódu
Můžete zkontrolovat objekty a členů v sadě Visual Studio projekty a objekty a členy v součásti rozhraní .NET Framework, komponenty modelu COM, dynamické knihovny (DLL) a zadejte knihovny (TLB).  
  
 Následující části tohoto dokumentu popisují windows struktura jiný kód.  
  
 [Zobrazení tříd (Visual Basic, C#, C++)](#BKMK_ClassView)  
  
 [Volání hierarchie (Visual Basic, C#, C++)](#BKMK_CallHierarchy)  
  
 [Prohlížeč objektů](#BKMK_ObjectBrowser)  
  
 [Definice kódu – okno (C#, C++)](#BKMK_CodeDefinition)  
  
 Můžete také použít **Průzkumníku řešení** procházet typy a členy v projektech, vyhledejte symboly, zobrazení hierarchie volání metody, najít odkazy na symboly a další bez nutnosti přepínat mezi více okna nástrojů uvedených výše.  
  
 Pokud máte Visual Studio Enterprise můžete vizualizovat struktura kódu a jeho závislosti mezi celé řešení a potom přejít na části kódu, které vás zajímají map kódu. Další informace najdete v tématu [mapování závislostí napříč vaším řešením](../modeling/map-dependencies-across-your-solutions.md).  
  
> [!NOTE]
>  Funkce v prostředí IDE může mít vliv na edicí sady Visual Studio a nastavením, které používáte. Se může lišit od těch popsaných v tomto tématu.  
  
##  <a name="BKMK_ClassView"></a>Zobrazení tříd (Visual Basic, C#, C++)  
 **Třídy zobrazení** se zobrazí jako součást **Průzkumníku řešení** i jako v samostatném okně. **Zobrazení tříd** okno zobrazí prvky aplikace. V horním podokně zobrazí obory názvů, typy, rozhraní, výčty a třídy, a v dolním podokně členy, kteří patří do vybraném v horním podokně typu. Pomocí tohoto okna můžete přesunout definice člen ve zdrojovém kódu (nebo **Prohlížeč objektů** Pokud je element definován mimo řešení).  
  
 Nemáte k sestavení projektu, k zobrazení jeho elementy v **zobrazení tříd**. Okno se aktualizují, jako je upravit kód ve vašem projektu.  
  
 Kód můžete přidat do projektu výběrem uzel projektu a zvolením **přidat** tlačítko Otevřít **přidat novou položku** dialogové okno. Kód je přidaný do samostatného souboru.  
  
 Pokud váš projekt se změnami do správy zdrojového kódu, každý **zobrazení tříd** element zobrazuje ikona označující stav zdroje kódu souboru. Běžné zdrojového kódu příkazy, jako **rezervovat**, **změnami**, a **získat nejnovější verzi** jsou také k dispozici v místní nabídce pro daný element.  
  
### <a name="class-view-toolbar"></a>Panel nástrojů zobrazení – třída  
 Zobrazení tříd nástrojů obsahuje následující příkazy.  
  
|||  
|-|-|  
|**Nová složka**|Vytvoří virtuální složku nebo podsložku, ve kterém můžete uspořádat často používané elementy. Jsou uloženy v aktivním řešení (.suo) souboru. Po přejmenování nebo odstranění elementu v kódu, se může objevit ve složce virtuální jako uzel k chybě. Pokud chcete tento problém opravit, odstraňte uzlu chyby. Pokud jste přejmenovali element, můžete jej přesunout z hierarchie projektu do složky znovu.|  
|**Zpět**|Přejde na dříve vybranou položku.|  
|**Předat dál**|Přejde na další vybranou položku.|  
|**Zobrazení diagramu tříd** (spravovaných jenom projekty kódu)|K dispozici po vyberte obor názvů nebo zadejte v **zobrazení tříd**. Pokud je vybraný obor názvů, třídy diagram zobrazuje všechny typy v ní. Když vyberete typ diagramu tříd zobrazuje pouze typu.|  
  
### <a name="class-view-settings"></a>Nastavení zobrazení – třída  
 **Nastavení zobrazení třídy** na panelu nástrojů zobrazí tlačítko má následující nastavení.  
  
|||  
|-|-|  
|**Zobrazit základní typy**|Základní typy jsou zobrazeny.|  
|**Zobrazit odvozené typy**|Odvozené typy jsou zobrazeny.|  
|**Zobrazit skryté typy a členy**|Skryté typy a členy (není určená pro klienty) se zobrazí světla šedou.|  
|**Zobrazit veřejné členy**|Zobrazí se veřejné členy.|  
|**Zobrazit chráněné členy**|Zobrazí se chráněné členy.|  
|**Zobrazit soukromé členy**|Zobrazí se soukromé členy.|  
|**Zobrazit další členy**|Ostatní typy členů jsou zobrazeny, včetně interní (nebo Friend v jazyce Visual Basic) členy.|  
|**Zobrazit zděděné členy**|Zobrazí se zděděné členy.|  
|**Zobrazit metody rozšíření**|Rozšiřující metody jsou zobrazeny.|  
  
### <a name="class-view-shortcut-menu"></a>Třídy zobrazení místní nabídky  
 Místní nabídky v **zobrazení tříd** může obsahovat následující příkazy, v závislosti na druhu projektu vybrané.  
  
|||  
|-|-|  
|**Přechod na definici**|Najde definici element ve zdrojovém kódu, nebo v **Prohlížeč objektů**, pokud element není definován v otevřeného projektu.|  
|**Procházet definice**|Zobrazí vybranou položku v **Prohlížeč objektů**.|  
|**Najít všechny odkazy**|Vyhledá položku aktuálně vybraného objektu a výsledky zobrazí v okně **Najít výsledky** okno.|  
|**Typ filtru** (spravovaný kód pouze)|Zobrazí vybraný typ nebo obor názvů. Filtr můžete odebrat výběrem **zrušte najít** (X) tlačítko Další **najít** pole.|  
|**Kopírování**|Zkopíruje plně kvalifikovaný název položky.|  
|**Seřadit podle abecedy**|Uvádí typy a členy abecedně podle názvu.|  
|**Řazení podle typ člena**|Uvádí typy a členy v pořadí podle typu (tak, aby třídy předcházet rozhraní, rozhraní předcházet delegáti, a metody předcházet vlastnosti).|  
|**Řazení podle přístup ke členu**|Zobrazí typy a členy v pořadí podle přístup typ, například veřejné nebo soukromé.|  
|**Seskupit podle typ člena**|Seřadí typy a členy do skupin podle typu objektu.|  
|**Přejděte k deklaraci** (pouze kód C++)|Zobrazí deklaraci typ nebo člen ve zdrojovém kódu, pokud je k dispozici.|  
|**Přechod na definici**|Zobrazuje definici typ nebo člen ve zdrojovém kódu, pokud je k dispozici.|  
|**Přejděte na odkaz**|Zobrazí odkaz na typ nebo člen ve zdrojovém kódu, pokud je k dispozici.|  
|**Zobrazení hierarchie volání**|Zobrazuje vybraný metodu v **hierarchie volání** okno.|  
  
##  <a name="BKMK_CallHierarchy"></a>Volání hierarchie (Visual Basic, C#, C++)  
 **Hierarchie volání** okně se zobrazí dané metody (nebo vlastnost nebo konstruktor) je volána kde jsou uvedené metody, které se nazývají z této metody. Můžete zobrazit více úrovní graph volání, která zobrazuje volající/volaný vztahy mezi metody v zadaném oboru.  
  
 Můžete zobrazit **hierarchie volání** okno výběrem – metoda (nebo vlastnosti nebo konstruktor) a pak vyberete **hierarchie tříd zobrazení** v místní nabídce. Zobrazení by měl vypadat podobně jako na následujícím obrázku.  
  
 ![Hierarchie volání více uzlů otevřete](../ide/media/multiplenodes.png "MultipleNodes")  
Hierarchie volání – okno  
  
 Pomocí rozevíracího seznamu na panelu nástrojů můžete určit obor hierarchie: řešení, aktuální projekt nebo aktuálním dokumentu.  
  
 V hlavním podokně se zobrazí volání do a z metody a **volání lokality** podokně zobrazí umístění vybraného volání. Pro členy, kteří jsou virtuální nebo abstraktní **název metody přepsání** uzel se objeví. Pro členy rozhraní **název metody implementuje** uzel se objeví.  
  
 **Hierarchie volání** okno nenajde Metoda skupiny odkazy, které zahrnují míst, kde se přidá jako obslužné rutiny události metodu, nebo je přiřazená delegáta. Chcete-li najít tyto odkazy, použijte **najít všechny odkazy** příkaz.  
  
 V místní nabídce **hierarchie volání** okno obsahuje následující příkazy.  
  
|||  
|-|-|  
|**Přidat jako nový kořen**|Přidá vybraný uzel jako nový kořenový uzel.|  
|**Odebrat kořenové**|Odebere vybraného kořenového uzlu z podokna zobrazení stromu.|  
|**Přechod na definici**|Přejde na původní definici metody.|  
|**Najít všechny odkazy**|Vyhledá v projektu všechny odkazy na vybranou metodu.|  
|**Kopírování**|Zkopíruje vybraný uzel (ale ne jeho dílčí uzly).|  
|**Aktualizace**|Aktualizuje informace.|  
  
##  <a name="BKMK_ObjectBrowser"></a>Prohlížeč objektů  
 **Prohlížeč objektů** zobrazí popisy kódu v projektech.  
  
 Co chcete zobrazit v můžete filtrovat **Prohlížeč objektů**. Pomocí rozevíracího seznamu v horní části okna můžete volit z následujících možností:  
  
-   Žádné rozhraní .NET Framework  
  
-   Silverlight  
  
-   Aktivním řešení  
  
-   Vlastní sada komponent  
  
 Vlastní komponenty mohou zahrnovat spravovaného kódu spustitelné soubory, knihovny sestavení, knihovny typů a .ocx soubory. Není možné přidat vlastní komponenty C++. Vlastní nastavení se ukládají v adresáři aplikace Visual Studio uživatele, % APPDATA%\Microsoft\VisualStudio\15.0\ObjBrowEX.dat.  
  
 Levém podokně **Prohlížeč objektů** zobrazuje fyzické kontejnery, jako jsou součásti rozhraní .NET Framework a COM. Můžete rozbalit uzly kontejneru pro zobrazení, která obsahují obory názvů a pak rozbalte obory názvů do zobrazení, které obsahují typy. Když vyberete typ, její členy (například vlastnosti a metody) jsou uvedeny v pravém podokně. Pravém dolním podokně zobrazí podrobné informace o vybrané položce.  
  
 Můžete vyhledat konkrétní položku pomocí **vyhledávání** pole v horní části okna. Hledání nerozlišují malá a velká písmena. V levém podokně se zobrazí výsledky hledání. Zrušte vyhledávání, vyberte **Smazat hledání** (X) tlačítko Další **vyhledávání** pole.  
  
 **Prohlížeč objektů** sleduje výběr jste udělali a můžete přejít mezi vybrané položky pomocí **dál** a **zpět** tlačítek na panelu nástrojů.  
  
 Můžete použít **Prohlížeč objektů** přidat odkaz na sestavení pro otevřete řešení výběrem položky (sestavení, obor názvů, typ nebo člen) a zvolením **přidat odkaz na** tlačítka na panelu nástrojů.  
  
### <a name="object-browser-settings"></a>Nastavení prohlížeče objektů  
 Pomocí **nastavení prohlížeče objektů** tlačítka na panelu nástrojů můžete nastavit některé z následujících zobrazení.  
  
|||  
|-|-|  
|**Zobrazení oborů názvů**|Zobrazí obory názvů, nikoli fyzické kontejnery, v levém podokně. Obory názvů, které jsou uložené v několika fyzických kontejnerů sloučení.|  
|**Zobrazení kontejnery**|Zobrazí fyzické kontejnery spíše než obory názvů, v levém podokně. **Zobrazit obory názvů** a **kontejnery zobrazení** se vzájemně vylučují nastavení.|  
|**Zobrazit základní typy**|Zobrazí základní typy.|  
|**Zobrazit odvozené typy**|Zobrazí odvozených typů.|  
|**Zobrazit skryté typy a členy**|Zobrazí skryté typy a členy (není určená pro klienty), světla šedou.|  
|**Zobrazit veřejné členy**|Zobrazí veřejné členy.|  
|**Zobrazit chráněné členy**|Zobrazí chráněné členy.|  
|**Zobrazit soukromé členy**|Zobrazí soukromé členy.|  
|**Zobrazit další členy**|Zobrazí členy jiné typy členů, včetně interní (nebo Friend v jazyce Visual Basic).|  
|**Zobrazit zděděné členy**|Zobrazí zděděné členy.|  
|**Zobrazit metody rozšíření**|Zobrazí rozšiřující metody.|  
  
### <a name="object-browser-shortcut-menu-commands"></a>Příkazy nabídky zástupce Prohlížeč objektů  
 V místní nabídce **Prohlížeč objektů** může obsahovat následující příkazy, v závislosti na druhu položky vybrané.  
  
|||  
|-|-|  
|**Procházet definice**|Zobrazuje primární uzel pro vybranou položku.|  
|**Najít všechny odkazy**|Vyhledá položku aktuálně vybraného objektu a výsledky zobrazí v okně **Najít výsledky** okno.|  
|**Filtrování na typ**|Zobrazí vybraný typ nebo obor názvů. Filtr můžete odebrat výběrem **zrušte vyhledávání** tlačítko.|  
|**Kopírování**|Zkopíruje plně kvalifikovaný název položky.|  
|**Odebrat**|Pokud obor je sada vlastní součást, odebere vybrané součásti z oboru.|  
|**Seřadit podle abecedy**|Uvádí typy a členy abecedně podle názvu.|  
|**Řazení podle typu objektu**|Uvádí typy a členy v pořadí podle typu (tak, aby třídy předcházet rozhraní, rozhraní předcházet delegáti, a metody předcházet vlastnosti).|  
|**Řazení podle přístup k objektům**|Zobrazí typy a členy v pořadí podle přístup typ, například veřejné nebo soukromé.|  
|**Seskupit podle typu objektu**|Seřadí typy a členy do skupin podle typu objektu.|  
|**Přejděte k deklaraci** (pouze projekty C++)|Zobrazí deklaraci typ nebo člen ve zdrojovém kódu, pokud je k dispozici.|  
|**Přechod na definici**|Zobrazuje definici typ nebo člen ve zdrojovém kódu, pokud je k dispozici.|  
|**Přejděte na odkaz**|Zobrazí odkaz na typ nebo člen ve zdrojovém kódu, pokud je k dispozici.|  
|**Zobrazení hierarchie volání**|Zobrazuje vybraný metodu v **hierarchie volání** okno.|  
  
##  <a name="BKMK_CodeDefinition"></a>Definice kódu – okno (C#, C++)  
 **Definice kódu** okno zobrazuje definici vybraný typ nebo člen aktivního projektu. Typ nebo člen lze vybrat v editoru kódu nebo v okně zobrazení kódu.  
  
 I když toto okno je jen pro čtení, můžete nastavit zarážky nebo záložky v ní. Chcete-li upravit definici zobrazených, zvolte **upravit definici** v místní nabídce. Tento zdrojový soubor se otevře v editoru kódu a Posune kurzor na řádek, kde začíná definici.  
  
### <a name="code-definition-shortcut-menu"></a>Kód definice místní nabídky  
 V místní nabídce **definice kódu** okno může obsahovat následující příkazy, v závislosti na programovací jazyk.  
  
|||  
|-|-|  
|**Vytvářet testy částí**|Vytvoří testy částí pro vybraný prvek.|  
|**Generovat Diagram pořadí**|Pokud je vybraná metoda, generuje diagram pořadí.|  
|**Vytvoření privátního přístupového objektu**|Pokud se nachází testů jednotek v řešení, generuje metody, která používá test získat přístup ke kódu.|  
|**Přechod na definici**|Najde definici (nebo definice pro částečné třídy) a zobrazí je v **Najít výsledky** okno.|  
|**Najít všechny odkazy**|Vyhledá odkazy na typ nebo člen v řešení.|  
|**Zobrazení hierarchie volání**|Zobrazí metodu v **hierarchie volání** okno.|  
|**Zobrazit volání testů**|Pokud jsou v projektu testování částí, zobrazuje testy, které volají na vybraný úsek kódu.|  
|**Spouštění testů volání**|Pokud jsou v projektu testování částí, spustí testy pro vybraný kód.|  
|**Zarážek**|Vloží zarážku (nebo tracepoint).|  
|**Spustit ke kurzoru**|Spustí program v režimu ladění na pozici kurzoru.|  
|**Kopírování**|Zkopíruje vybraný řádek.|  
|**Osnova**|Standardní popisující příkazy.|  
|**Upravte definici**|Přesune kurzor do definice v okně kód.|  
|**Zvolte kódování**|Otevře se **kódování** okna tak, aby můžete nastavit kódování souboru.|  
  
### <a name="document-outline-window"></a>Osnova dokumentu – okno  
 Můžete použít **Osnova dokumentu** okno ve spojení s návrháře zobrazení, jako je například návrháře XAML stránky nebo Návrhář formulářů Windows nebo s stránky HTML. Toto okno zobrazuje elementy ve stromovém zobrazení, aby mohli zobrazit logické struktury formuláře nebo stránce a najít ovládací prvky, které jsou moc hluboko vložené nebo skrytý.  
  
## <a name="see-also"></a>Viz také  
 [Zobrazení tříd a ikony v prohlížeči objektů](../ide/class-view-and-object-browser-icons.md)