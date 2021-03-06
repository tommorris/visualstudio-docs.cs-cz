---
title: Řízení barvy, stylu čáry a ostatních vlastností obrazce | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c06d0066-24aa-4c65-b91c-c2089b81ec8d
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 1722a3f8a5ff05589cfad987fff6448d44e96ec8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42628429"
---
# <a name="controlling-color-line-style-and-other-shape-properties"></a>Řízení barvy, stylu čáry a ostatních vlastností obrazce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [řízení barvy, stylu čáry a ostatních vlastností obrazce](https://docs.microsoft.com/visualstudio/modeling/controlling-color-line-style-and-other-shape-properties).  
  
Některé vlastnosti obrazce, jako je barva by bylo možné "vystavit" – to znamená, propojené na doménovou vlastnost obrazce. Ostatní uživatelé mají přímo se dá řídit.  
  
## <a name="exposing-a-property"></a>Vystavení vlastností  
 Některé vlastnosti obrazce, jako je barva může být propojený hodnoty vlastnosti domény.  
  
 V definici DSL vyberte obrazec, konektoru nebo diagramu třídy. V kontextové nabídce, zvolte **přidat vystavený**a klikněte na tlačítko Vlastnosti, třeba Barva výplně.  
  
 Doménová vlastnost, kterou můžete nastavit v kódu programu nebo jako uživatel nyní má obrazec.  
  
## <a name="dynamically-updating-an-exposed-property"></a>Dynamické aktualizace vystavené vlastnosti  
 Obvykle nechcete se ujistit vlastnost vystavené závisí na jiné vlastnosti. Můžete například obrazec, který chcete červenou pokaždé, když se konkrétní doménová vlastnost, která je menší než nula. Pokud chcete nastavit tuto závislost, vytvořit [pravidlo](../modeling/rules-propagate-changes-within-the-model.md). Příklad:  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using Microsoft.VisualStudio.Modeling;  
using Microsoft.VisualStudio.Modeling.Diagrams;  
namespace ExampleNamespace  
{  
 // Attribute associates the rule with class:  
 [RuleOn(typeof(CarShape), FireTime = TimeToFire.TopLevelCommit)]  
 // The rule is a class derived from one of the abstract rules:  
 class CarShapeAddRule : AddRule  
 {  
 // Override the abstract method:  
 public override void ElementAdded(ElementAddedEventArgs e)  
 {  
 base.ElementAdded(e);  
 CarShape shape = e.ModelElement as CarShape;  
 Store store = shape.Store;  
 // Ignore this call if we're currently loading a model:  
 if (store.TransactionManager.CurrentTransaction.IsSerializing)   
  return;  
 Car car = shape.ModelElement as Car;  
 // Code here propagates change as required - for example:  
 shape.FillColor = car.Somebool ? System.Drawing.Color.Red : System.Drawing.Color.Green;   
 }  
}  
 // The rule must be registered:  
 public partial class ExampleDomainModel  
 {  
 protected override Type[] GetCustomDomainModelTypes()  
 {  
  List<Type> types = new List<Type>(base.GetCustomDomainModelTypes());  
  types.Add(typeof(CarShapeAddRule));  
  // If you add more rules, list them here.   
  return types.ToArray();  
 }  
 }  
}  
```



