---
title: Objekty, které přidáváte do návrháře použít odlišné datové připojení, než momentálně používané návrhářem | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b2102d218ee74bc2e1a7a2787475c8005c77f2b1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42671100"
---
# <a name="the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer-is-currently-using"></a>Objekty, které přidáváte do návrháře, obsahují jiné datové připojení než připojení momentálně používané návrhářem.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [objekty, které přidáváte do návrháře použít odlišné datové připojení, než momentálně používané návrhářem](https://docs.microsoft.com/visualstudio/data-tools/the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer-is-currently-using).  
  
  
Objekty, které přidáváte do návrháře použijte odlišné datové připojení, než momentálně používané návrhářem. Opravdu chcete připojení používané návrhářem nahradit?  
  
 Při přidávání položek do [!INCLUDE[vs_ordesigner_long](../includes/vs-ordesigner-long-md.md)] ([!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)]), všech položek se používají sdílené datové připojení. (Na návrhovou plochu představuje <xref:System.Data.Linq.DataContext>, který používá jedno připojení pro všechny objekty na povrchu.) Pokud chcete přidat objekt do návrháře, který používá datové připojení, které se liší od aktuálně používá v Návrháři datové připojení, tato zpráva se zobrazí. Chcete-li vyřešit tuto chybu, můžete zachovat existující připojení. Pokud tuto volbu, nebude přidán vybraný objekt. Alternativně můžete přidat objekt a obnovit <xref:System.Data.Linq.DataContext> připojení k nové připojení.  
  
> [!NOTE]
>  Vyberete-li **Ano**, tříd na všech entit [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] jsou mapovány na nového připojení.  
  
### <a name="to-replace-the-existing-connection-with-the-connection-used-by-the-selected-object"></a>Chcete-li nahradit stávající připojení pomocí připojení používané objektem vybraný objekt  
  
-   Klikněte na tlačítko **Ano**.  
  
     Vybraný objekt se přidá do [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)], a DataContext.Connection je nastavená na nové připojení.  
  
### <a name="to-continue-to-use-the-existing-connection-and-cancel-adding-the-selected-object"></a>Chcete-li nadále používat stávající připojení a zrušit přidávání vybraný objekt  
  
-   Klikněte na tlačítko **ne**.  
  
     Akce zrušena. DataContext.Connection zůstane nastavená na existující připojení.  
  
## <a name="see-also"></a>Viz také  
 [Nástroje LINQ to SQL v sadě Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [Technologie LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)   
 [Připojování k datům v sadě Visual Studio](../data-tools/connecting-to-data-in-visual-studio.md)

