---
title: "Generatetrustinfo – úloha | Microsoft Docs"
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
- MSBuild, GenerateTrustInfo task
- GenerateTrustInfo task [MSBuild]
ms.assetid: 3ca60816-4bb0-4fef-ae43-ca0bfb63def3
caps.latest.revision: "4"
author: kempb
ms.author: kempb
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 614ace0800393b6c584da4cf4d85edfa7ea11b33
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/22/2017
---
# <a name="generatetrustinfo-task"></a>GenerateTrustInfo – úloha
Generuje důvěryhodnosti aplikace od základní manifest a od `TargetZone` a `ExcludedPermissions` parametry.  
  
## <a name="parameters"></a>Parametry  
 Následující tabulka popisuje parametry `GenerateTrustInfo` úloh.  
  
|Parametr|Popis|  
|---------------|-----------------|  
|`ApplicationDependencies`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametr.<br /><br /> Určuje závislá sestavení.|  
|`BaseManifest`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> parametr.<br /><br /> Určuje základní manifest pro generování důvěryhodnosti aplikace z.|  
|`ExcludedPermissions`|Volitelné `String` parametr.<br /><br /> Určuje jeden nebo více hodnot identity oddělených středníkem oprávnění mají být vyloučeny ze sady zóny výchozí oprávnění.|  
|`TargetZone`|Volitelné `String` parametr.<br /><br /> Určuje sadu oprávnění výchozí zóny, které se získávají z zásady počítače.|  
|`TrustInfoFile`|Požadované <xref:Microsoft.Build.Framework.ITaskItem> výstupní parametr.<br /><br /> Určuje soubor, který obsahuje informace o vztahu důvěryhodnosti zabezpečení aplikace.|  
  
## <a name="remarks"></a>Poznámky  
 Kromě s parametry, které jsou uvedené v tabulce, zdědí tento úkol parametry z <xref:Microsoft.Build.Tasks.TaskExtension> třída, které dědí z <xref:Microsoft.Build.Utilities.Task> třídy. Seznam těchto dalších parametrech a jejich popisy najdete v tématu [taskextension – základní třída](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Viz také  
 [Úlohy](../msbuild/msbuild-tasks.md)   
 [Referenční dokumentace úlohy](../msbuild/msbuild-task-reference.md)