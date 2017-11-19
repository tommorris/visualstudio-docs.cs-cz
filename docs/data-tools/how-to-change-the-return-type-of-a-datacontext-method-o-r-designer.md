---
title: "Postupy: Změna návratový typ metody DataContext (Návrhář O-R) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c5b66bff-6dbb-43c0-bffa-317133ca5b9e
caps.latest.revision: "2"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 869460f4ac40aece5421611cd83aad6a7f11ef57
ms.sourcegitcommit: ee42a8771f0248db93fd2e017a22e2506e0f9404
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2017
---
# <a name="how-to-change-the-return-type-of-a-datacontext-method-or-designer"></a>Postupy: Změna návratový typ metody DataContext (Návrhář relací objektů)
Návratový typ <xref:System.Data.Linq.DataContext> (vytvořili podle uložená procedura nebo funkce) se liší v závislosti na tom, kde vyřadit uložená procedura nebo funkce v [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)]. Pokud je vyřadit položku přímo do existující třídy entity, <xref:System.Data.Linq.DataContext> metodu, která má návratový typ třídy entita se vytvoří (Pokud je schéma dat vrácených uložená procedura nebo funkce odpovídá tvaru třídy entity). Pokud je položka vyřadit na prázdnou oblast [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)], <xref:System.Data.Linq.DataContext> metoda, která vrátí typ automaticky generované se vytvoří. Můžete změnit návratový typ <xref:System.Data.Linq.DataContext> metoda po přidání do podokna metody. Zkontrolovat nebo změnit návratový typ <xref:System.Data.Linq.DataContext> metoda, vyberte ho a klikněte na tlačítko **návratového typu** vlastnost **vlastnosti** okno.  
  
> [!NOTE]
>  Nelze vrátit <xref:System.Data.Linq.DataContext> metody, které mají návratový typ. nastaveny pro třídu entity, aby návratový typ automaticky vygenerované pomocí **vlastnosti** okno. Vrátit zpátky <xref:System.Data.Linq.DataContext> metoda vrátí typ automaticky generovaný původní objekt databáze musí přetažením na Návrhář relací objektů znovu.  
  
[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]  
  
## <a name="to-change-the-return-type-of-a-datacontext-method-from-the-auto-generated-type-to-an-entity-class"></a>Chcete-li změnit návratový typ metody DataContext z typu automaticky vygenerované třídy entity  
  
1.  Vyberte <xref:System.Data.Linq.DataContext> metoda v podokně metody.  
  
2.  Vyberte **návratového typu** v **vlastnosti** okna a potom vyberte dostupné entity třídy v **návratového typu** seznamu. Pokud třídy požadované entita není v seznamu, přidejte ho do nebo vytvořte ho [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)] ho přidejte do seznamu.  
  
3.  Uložte soubor DBML.  
  
## <a name="to-change-the-return-type-of-a-datacontext-method-from-an-entity-class-back-to-the-auto-generated-type"></a>Chcete-li změnit návratový typ metody DataContext z třídy entity zpět na automaticky generovaný typ  
  
1.  Vyberte <xref:System.Data.Linq.DataContext> metoda v podokně metody a jej odstraňte.  
  
2.  Přetáhněte objekt databáze z **Průzkumníka serveru**/**Průzkumník databáze** na prázdnou část Návrhář relací objektů.  
  
3.  Uložte soubor DBML.  
  
## <a name="see-also"></a>Viz také
[Technologie LINQ to SQL nástroje v sadě Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
[Technologie LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)   
[Metody DataContext (Návrhář relací objektů)](../data-tools/datacontext-methods-o-r-designer.md)   
[Postupy: vytvoření metody DataContext namapované na uložené procedury a funkce (Návrhář relací objektů)](../data-tools/how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-o-r-designer.md)