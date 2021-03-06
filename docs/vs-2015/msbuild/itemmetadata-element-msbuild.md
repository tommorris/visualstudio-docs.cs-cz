---
title: Itemmetadata – Element (MSBuild) | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ItemMetadata Element [MSBuild]
- <ItemMetadata> Element [MSBuild]
ms.assetid: e3db5122-202d-43a9-b2f4-3e0ec4ed3d08
caps.latest.revision: 20
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0032b1798fea215169f801dd23beb8aa856effc5
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669233"
---
# <a name="itemmetadata-element-msbuild"></a>ItemMetadata – element (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [itemmetadata – Element (MSBuild)](https://docs.microsoft.com/visualstudio/msbuild/itemmetadata-element-msbuild).  
  
  
Obsahuje klíč metadat uživatelem definovanou položku katalogu, který obsahuje hodnotu metadat položky. Položka může mít libovolný počet párů klíč hodnota metadat.  
  
 \<Project>  
 \<ItemGroup >  
 \<Položka >  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<ItemMetadataName> Item Metadata value</ItemMetadataName>  
```  
  
## <a name="attributes-and-elements"></a>Atributy a elementy  
 Následující části popisují atributy, podřízené prvky a nadřazené prvky.  
  
### <a name="attributes"></a>Atributy  
  
|Atribut|Popis|  
|---------------|-----------------|  
|`Condition`|Nepovinný atribut.<br /><br /> Podmínku, která má být vyhodnocen. Další informace najdete v tématu [podmínky](../msbuild/msbuild-conditions.md).|  
  
### <a name="child-elements"></a>Podřízené elementy  
 Žádné  
  
### <a name="parent-elements"></a>Nadřazené elementy  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[Položka](../msbuild/item-element-msbuild.md)|Uživatelem definované prvek, který definuje vstupy pro proces sestavení.|  
  
## <a name="text-value"></a>Textová hodnota  
 Textová hodnota je volitelná.  
  
 Tento text určuje hodnotu položky metadat, který může být text nebo XML.  
  
## <a name="remarks"></a>Poznámky  
  
## <a name="example"></a>Příklad  
 Následující příklad kódu ukazuje, jak přidat `Culture` metadata s hodnotou `fr` k položce `CSFile`.  
  
```  
<ItemGroup>  
    <CSFile Include="main.cs" >  
        <Culture>fr</Culture>  
    </CSFile>  
</ItemGroup>  
```  
  
## <a name="see-also"></a>Viz také  
 [Referenční dokumentace schématu souboru projektu](../msbuild/msbuild-project-file-schema-reference.md)   
 [Položky](../msbuild/msbuild-items.md)



