---
title: Vlastnosti dekorátorů | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Domain-Specific Language, decorators
ms.assetid: f6322fe5-dc08-4d32-a6b3-0bd18879136d
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: dc111cf868d2136a4d274889d96d50d2c9500a9a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42677314"
---
# <a name="properties-of-decorators"></a>Vlastnosti dekorátorů
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [vlastnosti Dekorátorů](https://docs.microsoft.com/visualstudio/modeling/properties-of-decorators).  
  
Dekorátory jsou ikony, text nebo Rozbalit/sbalit dvojité šipky, které se mohou objevit na obrazců a konektorů v diagramu. Následující tabulky popisují vlastnosti pro tři druhy dekoratér. Některé vlastnosti se zobrazí pouze na obrazec dekoratéry nebo pouze na konektor dekorátory.  
  
 Další informace najdete v tématu [jak se definuje jazyk specifický pro doménu](../modeling/how-to-define-a-domain-specific-language.md). Další informace o tom, jak pomocí těchto vlastností najdete v tématu [přizpůsobení a rozšíření jazyka specifického pro doménu](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
## <a name="expandcollapse-decorator"></a>Dekoratér rozbalení/sbalení  
  
|Vlastnost|Popis|Výchozí|  
|--------------|-----------------|-------------|  
|displayName|Název, který se zobrazí ve vygenerovaném návrháři dekoratér.|Rozbalte sbalit Dekoratér|  
|Název|Název dekoratéru|Dekoratér rozbalení a sbalení|  
|Poznámky|Neformální poznámky, které jsou spojeny s tohoto dekoratéru|\<žádné >|  
|HorizontalOffset|Vodorovný posun vzhledem k výchozí pozici dekoratéru, v palcích. (Ve tvarech pouze.)|0|  
|VerticalOffset|Svislý posun vzhledem k výchozí pozici dekoratéru, v palcích. (Ve tvarech pouze.)|0|  
|OffsetFromLine|Posun dekoratéru v řádku vzhledem k jeho výchozí pozici v palcích. (Na konektory pouze.)|0|  
|OffsetFromShape|Posun dekoratéru od obrazce vzhledem k jeho výchozí pozici v palcích. (Na konektory pouze.)|0|  
|Pozice|Výchozí pozici dekoratéru.|SourceTop|  
  
## <a name="icon-decorator"></a>Dekoratér ikony  
  
|Vlastnost|Popis|Výchozí|  
|--------------|-----------------|-------------|  
|DefaultIcon|Cesta souboru ikony nebo obrázku, který se má zobrazit.|\<žádné >|  
|displayName|Název dekoratér, který se zobrazí ve vygenerovaném návrháři.|Dekoratér ikony|  
|Název|Název dekoratéru|Dekoratér ikony|  
|Poznámky|Neformální poznámky, které jsou spojeny s dekoratér.|\<žádné >|  
|HorizontalOffset|Vodorovný posun vzhledem k výchozí pozici dekoratéru, v palcích. (Ve tvarech pouze.)|0|  
|VerticalOffset|Svislý posun vzhledem k výchozí pozici dekoratéru, v palcích. (Ve tvarech pouze.)|0|  
|OffsetFromLine|Posun dekoratéru v řádku vzhledem k jeho výchozí pozici v palcích. (Na konektory pouze.)|0|  
|OffsetFromShape|Posun dekoratéru od obrazce vzhledem k jeho výchozí pozici v palcích. (Na konektory pouze.)|0|  
|Pozice|Výchozí pozici dekoratéru.|SourceTop|  
  
## <a name="textdecorator"></a>TextDecorator  
  
|Vlastnost|Popis|Výchozí|  
|--------------|-----------------|-------------|  
|DefaultText|Výchozí text, který se má zobrazit.|Popisek|  
|displayName|Název dekoratér, který se zobrazí ve vygenerovaném návrháři.|Popisek|  
|Velikost písma|Velikost písma textu zobrazeného v dekoratéru.|8|  
|fontStyle|Styl písma textu zobrazeného v dekoratéru.|Pravidelné|  
|Název|Název dekoratéru|Popisek|  
|Poznámky|Neformální poznámky, které jsou spojeny s dekoratér.|\<žádné >|  
|HorizontalOffset|Vodorovný posun vzhledem k výchozí pozici dekoratéru, v palcích. (Ve tvarech pouze.)|0|  
|VerticalOffset|Svislý posun vzhledem k výchozí pozici dekoratéru, v palcích. (Ve tvarech pouze.)|0|  
|OffsetFromLine|Posun dekoratéru v řádku vzhledem k jeho výchozí pozici v palcích. (Na konektory pouze.)|0|  
|OffsetFromShape|Posun dekoratéru od obrazce vzhledem k jeho výchozí pozici v palcích. (Na konektory pouze.)|0|  
|Pozice|Výchozí pozici dekoratéru.|TargetBottom|  
  
## <a name="see-also"></a>Viz také  
 [Glosář nástrojů jazyka specifického pro doménu](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)



