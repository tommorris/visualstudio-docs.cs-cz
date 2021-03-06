---
title: Připojení referenčních řetězců k prvkům modelu UML | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- UML - extending, reference strings
ms.assetid: 15dbed99-efce-42fe-a768-714a5804e7d1
caps.latest.revision: 11
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 0d917bf0553fbea06c73d3f4ce57f01b3f99a36d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42629131"
---
# <a name="attach-reference-strings-to-uml-model-elements"></a>Připojení referenčních řetězců k prvkům modelu UML
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [připojení referenčních řetězců k UML model prvky](https://docs.microsoft.com/visualstudio/modeling/attach-reference-strings-to-uml-model-elements).  
  
Můžete napsat kód k připojení libovolného řetězců k prvkům modelu. Řetězec může být například identifikátor URI v mezipaměti výsledek výpočtu nebo ModelBus odkaz na prvek v jiného modelu. Každý řetězec je obsažený v objektu IReference. Pro každý prvek modelu lze připojit libovolný počet objektů IReference.  
  
 Každý objekt IReference má název. Můžete použít tento název označuje, jak by měl být interpretován hodnota odkazu. Můžete například nastavit název "URI" k označení, že hodnota by měl být interpretován jako identifikátor URI. Existují některé předdefinované referenční název hodnoty používají nástroje pro modelování.  
  
## <a name="attaching-a-reference-to-an-ielement"></a>Odkaz na IElement připojení  
 Chcete-li použít následující metody, musíte přidat odkaz na:  
  
 Microsoft.VisualStudio.ArchitectureTools.Extensibility.dll  
  
 Tato direktiva je vhodné vložit ve vašem kódu:  
  
 `using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml;`  
  
|Volání metody|Popis|  
|-----------------|-----------------|  
|`element.AddReference (nameString, valueString, duplicatesAllowed)`|Vytvoří `IReference` s daným názvem a hodnotou řetězce a odkazy na `element`. Vrátí `IReference`.<br /><br /> Vyvolá výjimku, pokud `duplicatesAllowed` má hodnotu false a není už `IReference` se stejným názvem připojené k `element`.|  
|`element.GetReferences(name)`|Vrátí všechny `IReference` objekty jsou propojeny s `element` , které mají daný `name`.|  
|`element.DeleteAllReferences(name)`|Odstraní všechny `IReference` objekty propojený prvek, který se zadaným názvem.|  
|`reference.Delete()`|To odstraní `IReference`.|  
|`ReferenceConstants.WorkItem`|Hodnota pro název odkazy na pracovní položku.|  
  
## <a name="see-also"></a>Viz také  
 [Definování obslužné rutiny odkazu pracovní položky](../modeling/define-a-work-item-link-handler.md)   
 [Definování a instalace rozšíření modelování](../modeling/define-and-install-a-modeling-extension.md)   
 [Programování s rozhraním API UML](../modeling/programming-with-the-uml-api.md)



