---
title: "Přizpůsobení nástroje Element | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6dac48b6-db68-4bcd-8aa2-422c2ad5d28b
caps.latest.revision: "6"
author: alancameronwills
ms.author: awills
manager: douge
ms.openlocfilehash: 2555fe2be42ed58482cdacf174a6cb035a8d7bd5
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="customizing-element-tools"></a>Přizpůsobení nástrojů elementu
V některých z nich DSL představují jeden koncept jako skupinu elementů. Například pokud vytvoříte model, ve kterém součást má pevnou sadu portů, vždy chcete porty, které mají být vytvořeny ve stejnou dobu jako jejich nadřazené součásti. Proto musíte přizpůsobit nástroj pro vytváření element tak, aby vytvoří skupinu elementů ne o jeden. Jak toho docílit, můžete přizpůsobit, jak je nástroj pro vytváření element inicializován.  
  
 Můžete také přepsat, co se stane, když je nástroj přetáhli diagramu nebo element.  
  
## <a name="customizing-the-content-of-an-element-tool"></a>Přizpůsobení obsah nástroj na Element  
 Každý element nástroj ukládá instance <xref:Microsoft.VisualStudio.Modeling.ElementGroupPrototype> (EGP), který obsahuje serializovaná verze jeden nebo více prvků modelu a odkazy. Ve výchozím nastavení obsahuje EGP nástroje k elementu jedna instance třídy, které zadáte pro nástroj. Toto můžete změnit přepsáním *YourLanguage*`ToolboxHelper.CreateElementToolPrototype`. Tato metoda je volána, když je balíček DSL načíst.  
  
 Parametr metody je ID třídy, která jste zadali v definici DSL. Když metoda je volána s třídou, která vás zajímá, můžete přidat další prvky do EGP.  
  
 EGP musí obsahovat odkazy na jeden element main na jiné elementy vložení. Může také zahrnovat referenční odkazy.  
  
 Následující příklad vytvoří main element a dvě vložené prvky. Hlavní třídy se nazývá odpor a má dvě relace vnoření elementů s názvem terminálu. Vnoření vlastnosti role jsou pojmenované Terminal1 a Terminal2 a mohou mít násobnost 1..1.  
  
```  
using Microsoft.VisualStudio.Modeling; ...    
public partial class CircuitDiagramToolboxHelper  
{  
  protected override ElementGroupPrototype    CreateElementToolPrototype(Store store, Guid domainClassId)  
  {  
    // A case for each tool to customize:    
    if (domainClassId == Resistor.DomainClassId)  
    {  
      // Set up the prototype elements and links:  
      Resistor resistor = new Resistor(store);  
      resistor.Terminal1 = new Terminal(store);   
      resistor.Terminal2 = new Terminal(store);  
      resistor.Terminal1.Name = "T1"; // embedding  
      resistor.Terminal2.Name = "T2"; // embedding  
      // We could also set up reference links.  
  
      // Create an element group prototype for the toolbox:  
      ElementGroup egp = new ElementGroup(store.DefaultPartition);  
      egp.AddGraph(resistor, true);  
      // We do not have to explicitly include embedded children.  
      return egp.CreatePrototype();  
    }  
    // Element tools for other classes:  
    else  
      return base.CreateElementToolPrototype(store, domainClassId);  
  }  
}  
```  
  
## <a name="see-also"></a>Viz také  
 [Přizpůsobení Element vytváření a přesun](../modeling/customizing-element-creation-and-movement.md)