---
title: Move – úloha | Dokumentace Microsoftu
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
- MSBuild, Move task
- Move task [MSBuild]
ms.assetid: d1405347-1309-4f18-b565-905408093d59
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 46fd157a1b4425f7a6f3c2f3ec6e6ba9d4ee1083
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670572"
---
# <a name="move-task"></a>Move – úloha
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [přesunutí úloh](https://docs.microsoft.com/visualstudio/msbuild/move-task).  
  
  
Soubory přesunou do nového umístění.  
  
## <a name="parameters"></a>Parametry  
 Následující tabulka popisuje parametry `Move` úloh.  
  
|Parametr|Popis|  
|---------------|-----------------|  
|`DestinationFiles`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> `[]` výstupní parametr.<br /><br /> Určuje seznam souborů pro zdrojové soubory pro přesun. Tento seznam by měl být mapování 1: 1 v seznamu, který je zadán v `SourceFiles` parametru. To znamená, že první soubor zadaný v `SourceFiles` se přesune na první místo zadané v `DestinationFiles`a tak dále.|  
|`DestinationFolder`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> parametru.<br /><br /> Určuje adresář, do kterého chcete přesunout soubory.|  
|`MovedFiles`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> `[]` výstupní parametr.<br /><br /> Obsahuje položky, které byly úspěšně přesunuty.|  
|`OverwriteReadOnlyFiles`|Volitelné `Boolean` parametru.<br /><br /> Pokud `true`, přepíše soubory i v případě, že jsou označeny jako soubory jen pro čtení.|  
|`SourceFiles`|Požadovaný parametr <xref:Microsoft.Build.Framework.ITaskItem>`[]`.<br /><br /> Určuje soubory, které chcete přesunout.|  
  
## <a name="remarks"></a>Poznámky  
 Buď `DestinationFolder` parametr nebo `DestinationFiles` parametr musí být zadaný, ale ne obojí. Jsou-li zadány oba parametry, úloha se nezdaří a je zaznamenána chyba.  
  
 Kromě s parametry, které jsou uvedené v tabulce, zdědí tento úkol parametry ze <xref:Microsoft.Build.Tasks.TaskExtension> třída, která sama dědí z <xref:Microsoft.Build.Utilities.Task> třídy. Seznam těchto dalších parametrů a jejich popisy najdete v tématu [taskextension – základní třída](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Viz také  
 [Úlohy](../msbuild/msbuild-tasks.md)   
 [Referenční dokumentace úlohy](../msbuild/msbuild-task-reference.md)



