---
title: "Návod: Vytvoření vlastní karty pomocí kódu XML pásu karet | Microsoft Docs"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Ribbon [Office development in Visual Studio], tabs
- customizing the Ribbon, tabscustom Ribbon, tabs
- Ribbon [Office development in Visual Studio], XML
- XML [Office development in Visual Studio], Ribbon
- Ribbon [Office development in Visual Studio], customizing
- Custom tab [Office development in Visual Studio]
ms.assetid: f6391a01-df1a-4a0f-bfbb-a9526c73b2b3
caps.latest.revision: "35"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: office
ms.openlocfilehash: 8933345017cef96c17ed69a42dc3e095fcf7c7ae
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/22/2017
---
# <a name="walkthrough-creating-a-custom-tab-by-using-ribbon-xml"></a>Návod: Vytvoření vlastní karty pomocí kódu XML pásu karet
  Tento návod ukazuje, jak vytvořit vlastní karty pásu karet pomocí **pásu karet (XML)** položky.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
 Tento návod znázorňuje následující úlohy:  
  
-   Přidání tlačítek do **doplňky** kartě. **Doplňky** karta je karta výchozí, který je definován v souboru XML pásu karet.  
  
-   Automatizace aplikace Microsoft Office Word s použitím tlačítka na **doplňky** kartě.  
  
> [!NOTE]  
>  Váš počítač může v následujících pokynech zobrazovat odlišné názvy nebo umístění některých prvků uživatelského rozhraní sady Visual Studio. Tyto prvky jsou určeny edicí sady Visual Studio a použitým nastavením. Další informace najdete v tématu [přizpůsobení prostředí Visual Studio IDE](../ide/personalizing-the-visual-studio-ide.md).  
  
## <a name="prerequisites"></a>Požadavky  
 K dokončení tohoto návodu budete potřebovat následující komponenty:  
  
-   [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]  
  
-   Aplikace Microsoft Word.  
  
## <a name="creating-the-project"></a>Vytvoření projektu  
 Prvním krokem je vytvoření projektu doplňku VSTO pro Word. Bude později upravit **doplňky** karta tohoto dokumentu.  
  
#### <a name="to-create-a-new-project"></a>Chcete-li vytvořit nový projekt  
  
1.  Vytvoření **doplňku pro aplikaci Word** projektu s názvem **MyRibbonAddIn**.  
  
     Další informace najdete v tématu [postupy: vytváření projektů Office v sadě Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md).  
  
     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]Otevře se **ThisAddIn.cs** nebo **ThisAddIn.vb** kód soubor a přidá **MyRibbonAddIn** projektu do **Průzkumníku řešení**.  
  
## <a name="creating-the-vsto-add-ins-tab"></a>Vytvoření karty doplňků VSTO  
 Chcete-li vytvořit **doplňky** přidejte **pásu karet (XML)** položku do projektu. Dále v tomto návodu přidáte některé tlačítka na této kartě.  
  
#### <a name="to-create-the-add-ins-tab"></a>K vytvoření karty doplňky  
  
1.  Na **projektu** nabídky, klikněte na tlačítko **přidat novou položku**.  
  
2.  V **přidat novou položku** dialogové okno, vyberte **pásu karet (XML)**.  
  
3.  Změňte název nové pásu karet na **MyRibbon**a klikněte na tlačítko **přidat**.  
  
     **MyRibbon.cs** nebo **MyRibbon.vb** soubor se otevře v návrháři. Soubor XML, který je pojmenován **MyRibbon.xml** je také přidán do projektu.  
  
4.  V **Průzkumníku řešení**, klikněte pravým tlačítkem na **ThisAddin.cs** nebo **ThisAddin.vb**a potom klikněte na **kód zobrazení**.  
  
5.  Přidejte následující kód, který **ThisAddin** třídy. Tento kód přepíše metodu CreateRibbonExtensibilityObject a vrátí třídy XML pásu karet do aplikace Office.  
  
     [!code-csharp[Trin_Ribbon_Custom_Tab_XML#1](../vsto/codesnippet/CSharp/Trin_Ribbon_Custom_Tab_XML_O12/ThisAddIn.cs#1)]
     [!code-vb[Trin_Ribbon_Custom_Tab_XML#1](../vsto/codesnippet/VisualBasic/Trin_Ribbon_Custom_Tab_XML_O12/ThisAddIn.vb#1)]  
  
6.  V **Průzkumníku řešení**, klikněte pravým tlačítkem myši **MyRibbonAddIn** projektu a pak klikněte na **sestavení**. Ověřte, že sestavení projektu bez chyb.  
  
## <a name="adding-buttons-to-the-add-ins-tab"></a>Přidání tlačítka na kartu doplňky  
 Cílem pro tento doplněk VSTO je umožnit uživateli, způsob, jak přidat často používaný text a určité tabulky v aktivním dokumentu. Poskytnout uživatelské rozhraní, přidávat dvě tlačítka **doplňky** kartě úpravou souboru XML pásu karet. Dále v tomto návodu určíte metody zpětného volání pro tlačítka. Další informace o souboru XML karet najdete v tématu [XML karet](../vsto/ribbon-xml.md).  
  
#### <a name="to-add-buttons-to-the-add-ins-tab"></a>Přidání tlačítka do karta Doplňky  
  
1.  V **Průzkumníku řešení**, klikněte pravým tlačítkem na **MyRibbon.xml** a pak klikněte na **otevřete**.  
  
2.  Nahraďte obsah **kartě** element s následující kód XML. Tato konfigurace XML změní štítek výchozí skupinu ovládací prvek pro **obsahu**, a přidá dvě nová tlačítka s popisky **vložit Text** a **Vložit tabulku**.  
  
    ```  
    <tab idMso="TabAddIns">  
        <group id="ContentGroup" label="Content">  
            <button id="textButton" label="Insert Text"  
                 screentip="Text" onAction="OnTextButton"  
                 supertip="Inserts text at the cursor location."/>  
            <button id="tableButton" label="Insert Table"  
                 screentip="Table" onAction="OnTableButton"  
                 supertip="Inserts a table at the cursor location."/>  
        </group>  
    </tab>  
    ```  
  
## <a name="automating-the-document-by-using-the-buttons"></a>Automatizace v dokumentu s použitím tlačítka  
 Je nutné přidat `onAction` metody zpětného volání pro **vložit Text** a **Vložit tabulku** tlačítka k provádění akcí, když uživatel klikne, je. Další informace o metody zpětného volání pro ovládací prvky pásu karet najdete v tématu [XML karet](../vsto/ribbon-xml.md).  
  
#### <a name="to-add-callback-methods-for-the-buttons"></a>Chcete-li přidat metody zpětného volání pro tlačítka  
  
1.  V **Průzkumníku řešení**, klikněte pravým tlačítkem na **MyRibbon.cs** nebo **MyRibbon.vb**a potom klikněte na **otevřete**.  
  
2.  Přidejte následující kód do horní části **MyRibbon.cs** nebo **MyRibbon.vb** souboru. Tento kód vytvoří alias <xref:Microsoft.Office.Interop.Word> oboru názvů.  
  
     [!code-csharp[Trin_RibbonButtons#1](../vsto/codesnippet/CSharp/Trin_RibbonButtons/MyRibbon.cs#1)]
     [!code-vb[Trin_RibbonButtons#1](../vsto/codesnippet/VisualBasic/Trin_RibbonButtons/MyRibbon.vb#1)]  
  
3.  Přidejte následující metodu do `MyRibbon` třídy. Toto je metoda zpětného volání pro **vložit Text** tlačítko, které přidá řetězec do aktuálního umístění kurzoru v aktivním dokumentu.  
  
     [!code-csharp[Trin_Ribbon_Custom_Tab_XML#2](../vsto/codesnippet/CSharp/Trin_Ribbon_Custom_Tab_XML_O12/MyRibbon.cs#2)]
     [!code-vb[Trin_Ribbon_Custom_Tab_XML#2](../vsto/codesnippet/VisualBasic/Trin_Ribbon_Custom_Tab_XML_O12/MyRibbon.vb#2)]  
  
4.  Přidejte následující metodu do `MyRibbon` třídy. Toto je metoda zpětného volání pro **Vložit tabulku** tlačítko, která přidává tabulku pro aktivní dokument na aktuální pozici kurzoru.  
  
     [!code-csharp[Trin_Ribbon_Custom_Tab_XML#3](../vsto/codesnippet/CSharp/Trin_Ribbon_Custom_Tab_XML_O12/MyRibbon.cs#3)]
     [!code-vb[Trin_Ribbon_Custom_Tab_XML#3](../vsto/codesnippet/VisualBasic/Trin_Ribbon_Custom_Tab_XML_O12/MyRibbon.vb#3)]  
  
## <a name="testing-the-vsto-add-in"></a>Testování doplňku VSTO  
 Při spuštění projektu, otevře se aplikace Word a na kartě s názvem **doplňky** se zobrazí na pásu karet. Klikněte na tlačítko **vložit Text** a **Vložit tabulku** tlačítka na **doplňky** kartě k testování kódu.  
  
#### <a name="to-test-your-vsto-add-in"></a>K testování vaší doplňku VSTO  
  
1.  Stisknutím klávesy F5 spusťte projekt.  
  
2.  Potvrďte, že **doplňky** karta je zobrazena na pásu karet.  
  
3.  Klikněte **doplňky** kartě.  
  
4.  Potvrďte, že **obsahu** skupiny je zobrazen na pásu karet.  
  
5.  Klikněte **vložit Text** tlačítka na **obsahu** skupiny.  
  
     Řetězec se přidá do dokumentu na aktuální pozici kurzoru.  
  
6.  Klikněte **Vložit tabulku** tlačítka na **obsahu** skupiny.  
  
     Tabulka se přidá do dokumentu na aktuální pozici kurzoru.  
  
## <a name="next-steps"></a>Další kroky  
 Další informace o tom, jak přizpůsobit rozhraní Office z těchto témat:  
  
-   Přizpůsobení pásu karet jinou aplikaci Office. Další informace o aplikacích, které podporují přizpůsobení pásu karet najdete v tématu [přehled pásu karet](../vsto/ribbon-overview.md).  
  
-   Přizpůsobení pásu karet Office aplikace pomocí Návrháře pásu karet. Další informace najdete v tématu [Návrhář pásu karet](../vsto/ribbon-designer.md).  
  
-   Vytvořte vlastní akce podokně. Další informace najdete v tématu [přehled podokna akcí](../vsto/actions-pane-overview.md).  
  
-   Přizpůsobení uživatelského rozhraní systému Microsoft Office Outlook pomocí oblastí formulářů aplikace Outlook. Další informace najdete v tématu [návod: Návrh oblasti formuláře aplikace Outlook](../vsto/walkthrough-designing-an-outlook-form-region.md).  
  
## <a name="see-also"></a>Viz také  
 [Přehled pásu karet](../vsto/ribbon-overview.md)   
 [Kódu XML pásu karet](../vsto/ribbon-xml.md)   
 [Návod: Vytvoření vlastní karty pomocí návrháře pásu karet](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)  
  
  