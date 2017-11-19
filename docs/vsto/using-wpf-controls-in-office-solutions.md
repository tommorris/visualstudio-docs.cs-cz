---
title: "Použití ovládacích prvků grafického subsystému WPF v řešeních pro systém Office | Microsoft Docs"
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
helpviewer_keywords: WPF [Office development in Visual Studio]
ms.assetid: 305a212b-0a95-40ad-87aa-22896fe80a04
caps.latest.revision: "25"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f15eea2c0f1e7e62990d860007a7efc4966cb8cc
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="using-wpf-controls-in-office-solutions"></a>Použití ovládacích prvků WPF v řešeních pro systém Office
  I když řešení vytvořená pomocí nástrojů pro vývoj pro Office v sadě Visual Studio jsou navrženy pro práci s přímo s Windows Forms – ovládací prvky, které můžete použít ovládacích prvků WPF v řešeních. Windows Presentation Foundation (WPF) představuje alternativu k Windows Forms pro návrh uživatelského rozhraní. WPF pomocí značek jazyka nazývaného rozšiřitelné aplikace Markup Language (XAML) poskytuje nové techniky zařadit uživatelského rozhraní, média a dokumenty. Další informace najdete v tématu [Úvod k použití WPF v sadě Visual Studio 2015](/dotnet/framework/wpf/getting-started/introduction-to-wpf-in-vs).  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
 Libovolný element uživatelského rozhraní, který může hostovat ovládací prvky Windows Forms v řešení Office může hostovat ovládacích prvků WPF. Mezi ně patří následující prvky:  
  
-   Dokumenty a listy v přizpůsobeních na úrovni dokumentu.  
  
-   Podokna akcí v přizpůsobeních na úrovni dokumentu.  
  
-   Vlastní podokna úloh v doplňcích VSTO.  
  
-   Oblasti formuláře v doplňcích VSTO pro Outlook.  
  
## <a name="adding-wpf-controls-to-office-projects-at-design-time"></a>Přidání ovládacích prvků WPF v době návrhu do projektů Office  
 Nelze přidat ovládacích prvků WPF přímo k elementům uživatelského rozhraní v řešeních pro systém Office. Místo toho přidejte **uživatelského ovládacího prvku (WPF)** položku do projektu a používejte ho jako návrhové ploše pro ovládacích prvků WPF. Potom můžete přidáte uživatelský ovládací prvek WPF do elementu uživatelského rozhraní v projektu.  
  
#### <a name="to-add-wpf-controls-to-an-actions-pane-custom-task-pane-or-form-region"></a>Přidání ovládacích prvků WPF do podokna akce, vlastního podokna úloh nebo oblasti formuláře  
  
1.  Otevřete projekt, do které chcete přidat vlastního podokna úloh, podokna akcí nebo oblasti formuláře.  
  
2.  Přidat **uživatelského ovládacího prvku (WPF)** položku do projektu.  
  
3.  Z **sada nástrojů**, přidání ovládacích prvků WPF na plochu návrháře ovládací prvek WPF uživatele.  
  
     Ve výchozím nastavení, pokud Návrháře WPF uživatele řízení je otevřený **sada nástrojů** obsahuje pouze ovládacích prvků WPF.  
  
4.  Sestavte projekt.  
  
5.  Přidání podokna akcí, oblasti formuláře nebo vlastního podokna úloh do projektu:  
  
    -   Oblasti formuláře, přidejte **oblasti formuláře aplikace Outlook** položku do projektu. Další informace najdete v tématu [postupy: přidání oblasti formuláře do projektu doplňku aplikace Outlook](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md).  
  
    -   Podokna akcí, přidejte **ovládací prvek podokna akce** nebo **uživatelský ovládací prvek** položku do projektu. Další informace najdete v tématu [postupy: Přidání podokna akcí do dokumentů aplikace Word nebo sešitů aplikace Excel](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md) a [postupy: Přidání podokna akcí do dokumentů aplikace Word nebo sešitů aplikace Excel](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md).  
  
    -   Vlastní podokna úloh, přidejte **uživatelský ovládací prvek** položku do projektu. Další informace najdete v tématu [postupy: Přidání vlastního podokna úloh do aplikace](../vsto/how-to-add-a-custom-task-pane-to-an-application.md).  
  
6.  Z *ProjectName* **uživatelských ovládacích prvků WPF** kartě **sada nástrojů**, přetáhněte uživatelský ovládací prvek WPF designer pro podokna akce, oblasti formuláře nebo vlastního podokna úloh.  
  
     Visual Studio automaticky vytvoří <xref:System.Windows.Forms.Integration.ElementHost> objekt, který je hostitelem uživatelský ovládací prvek WPF element uživatelského rozhraní.  
  
7.  Znovu sestavte projekt.  
  
#### <a name="to-add-wpf-controls-to-a-document-or-worksheet-in-a-document-level-project"></a>Přidání ovládacích prvků WPF k dokumentu nebo sešitu v projektech na úrovni dokumentu  
  
1.  Otevřete projekt na úrovni dokumentu pro Word či Excel.  
  
2.  Přidat **uživatelského ovládacího prvku (WPF)** položku do projektu.  
  
3.  Z **sada nástrojů**, přidání ovládacích prvků WPF na plochu návrháře ovládací prvek WPF uživatele.  
  
4.  Sestavte projekt.  
  
5.  Přidat **uživatelský ovládací prvek** položky (to znamená, uživatel ovládacího prvku Windows Forms) k projektu.  
  
6.  Otevřete návrháře uživatelského ovládacího prvku Windows Forms.  
  
7.  Z *ProjectName* **uživatelských ovládacích prvků WPF** kartě **sada nástrojů**, přetáhněte uživatelský ovládací prvek WPF do návrháře.  
  
     Visual Studio automaticky vytvoří <xref:System.Windows.Forms.Integration.ElementHost> objekt, který je hostitelem uživatelský ovládací prvek WPF v ovládacím prvku Windows Forms uživatele.  
  
8.  Napište kód, který prostřednictvím kódu programu přidá uživatelského ovládacího prvku Windows Forms k dokumentu nebo sešitu. Další informace najdete v tématu [přidání ovládacích prvků do dokumentů Office za běhu](../vsto/adding-controls-to-office-documents-at-run-time.md).  
  
    > [!NOTE]  
    >  Nelze přetáhnout uživatelského ovládacího prvku Windows Forms k dokumentu nebo listu v návrháři.  
  
9. Znovu sestavte projekt.  
  
## <a name="hosting-wpf-controls-by-using-the-elementhost-class"></a>Hostování ovládacích prvků WPF pomocí elementhost – třída  
 Visual Studio poskytuje funkce, které vám pomohou používat ovládací prvky Windows Forms v řešeních pro systém Office, ale neposkytuje podobné funkce pro ovládacích prvků WPF. Například přidáním ovládací prvky Windows Forms k dokumentům a listy v době návrhu tak, že přetáhnete ovládacích prvků z **sada nástrojů**, nebo v době běhu pomocí pomocné metody. Tyto nástroje však nejsou k dispozici pro ovládacích prvků WPF.  
  
 Řídí použití WPF <xref:System.Windows.Forms.Integration.ElementHost> třída jako vrstva integrace mezi ovládacího prvku Windows Forms nebo formuláře a ovládacích prvků WPF. Při přidání ovládacích prvků WPF k řešení v době návrhu, Visual Studio automaticky generuje <xref:System.Windows.Forms.Integration.ElementHost> objektu za vás.  
  
## <a name="wpf-resources"></a>Prostředky grafického subsystému WPF  
 Další informace o architektuře a problémy návrhu pro hostování ovládacích prvků WPF ve formulářích a ovládací prvky Windows Forms najdete v následujících tématech:  
  
-   [Architektura vstupní interoperabilita WPF a Windows Forms](/dotnet/framework/wpf/advanced/windows-forms-and-wpf-interoperability-input-architecture)  
  
-   [Windows Forms a mapování vlastností WPF](/dotnet/framework/wpf/advanced/windows-forms-and-wpf-property-mapping)  
  
-   [WPF a vzájemná spolupráce Windows Forms](/dotnet/framework/wpf/advanced/wpf-and-windows-forms-interoperation)  
  
-   [Windows Forms a ovládacích prvků ekvivalentní WPF](/dotnet/framework/wpf/advanced/windows-forms-controls-and-equivalent-wpf-controls)  
  
 Další informace o přidávání ovládacích prvků WPF v době návrhu pro ovládací prvky Windows Forms a formuláře v sadě Visual Studio najdete v následujících tématech:  
  
-   [Návod: Vytvoření nového obsahu WPF v rozhraní Windows Forms v době návrhu](/dotnet/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time)  
  
-   [Návod: Uspořádání obsahu WPF ve Windows Forms v době návrhu](/dotnet/framework/winforms/advanced/walkthrough-arranging-wpf-content-on-windows-forms-at-design-time)  
  
-   [Návod: Určení stylu obsahu WPF](/dotnet/framework/winforms/advanced/walkthrough-styling-wpf-content)  
  
## <a name="see-also"></a>Viz také  
 [Přizpůsobení uživatelského rozhraní sady Office](../vsto/office-ui-customization.md)   
 [Windows Forms – ovládací prvky na přehled dokumenty sady Office](../vsto/windows-forms-controls-on-office-documents-overview.md)   
 [Přehled podokna akcí](../vsto/actions-pane-overview.md)   
 [Vlastní podokna úloh](../vsto/custom-task-panes.md)   
 [Vytváření oblastí formulářů aplikace Outlook](../vsto/creating-outlook-form-regions.md)   
 [Postupy: Přidání podokna akcí do dokumentů aplikace Word nebo sešitů aplikace Excel](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md)   
 [Postupy: Přidání podokna akcí do dokumentů aplikace Word nebo sešitů aplikace Excel](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md)   
 [Postupy: Přidání vlastního podokna úloh do aplikace](../vsto/how-to-add-a-custom-task-pane-to-an-application.md)   
 [Postupy: přidání oblasti formuláře do projektu doplňku aplikace Outlook](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md)  
  
  