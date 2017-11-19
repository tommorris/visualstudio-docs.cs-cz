---
title: "Speciální řídicí znaky | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- special characters to escape
- msbuild, special characters to escape
ms.assetid: 5b5172c3-41e4-4f38-a16f-2aeac831a5fc
caps.latest.revision: "8"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 6c236a86677dab4015f8a0dc234ed211def7b1f3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="special-characters-to-escape"></a>Speciální řídicí znaky
Speciální znaky, je nutné uvést pouze v případě, že mají zvláštní význam v kontextu, ve kterém se právě používají. Například se tedy hvězdička (*) je speciální znak pouze v atributech "Zahrnout" a "Vyloučit" definice položky, nebo volání <xref:Microsoft.Build.Tasks.CreateItem>. Ve všech ostatních případech se tedy hvězdička považován za literálu hvězdičky. Pokud nepotřebujete, abyste se vyhnuli hvězdičky everywhere v souborech projektu, to tak neškodí.  
  
 Použít zápis %*xx* místo speciální znak, kde *xx* představuje šestnáctkové hodnoty znaků ASCII. Například jako literál znak používat hvězdičku (*), použijte hodnotu `%2A`.  
  
 Úplný seznam speciální řídicí znaky takto:  
  
|Znak|Popis|  
|---------------|-----------------|  
|%|Symbol procent, slouží k odkazování metadat.|  
|$|Dolaru slouží k odkazování vlastnosti.|  
|@|Znak, slouží k odkazování položky seznamů.|  
|(|Otevřete závorky, použít v seznamech.|  
|)|Zavřete závorky, použít v seznamech.|  
|`|Apostrof (nebo značky), používají v podmínkách a jiné výrazy.|  
|;|Středník, oddělovač seznamu.|  
|?|Otazník, zástupný znak při popisu specifikaci souboru v části na položku vložit/vyloučit.|  
|*|Znak hvězdičky zástupný znak při popisu specifikaci souboru v části na položku vložit/vyloučit.|  
  
## <a name="see-also"></a>Viz také  
 [Postupy: vyhnuli speciální znaky v nástroji MSBuild](../msbuild/how-to-escape-special-characters-in-msbuild.md)   
 [MSBuild – Reference](../msbuild/msbuild-reference.md)