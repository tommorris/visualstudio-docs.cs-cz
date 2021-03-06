---
title: Assignprojectconfiguration – úloha | Dokumentace Microsoftu
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
ms.assetid: 09633a0b-8f6f-4aba-8058-7cb4d13ce2c0
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c812b74735720d11c5fc4662faff056073dc778d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42696566"
---
# <a name="assignprojectconfiguration-task"></a>AssignProjectConfiguration – úloha
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [assignprojectconfiguration – úloha](https://docs.microsoft.com/visualstudio/msbuild/assignprojectconfiguration-task).  
  
  
Tato úloha přijímá řetězec seznamu konfigurace a přiřadí ho k zadaným projektům.  
  
## <a name="task-parameters"></a>Parametry úlohy  
 Následující tabulka popisuje parametry `AssignProjectConfiguration` úloh.  
  
|Parametr|Popis|  
|---------------|-----------------|  
|`SolutionConfigurationContents`|Volitelné `string` výstupní parametr.<br /><br /> Obsahuje řetězec XML obsahující projekt konfigurace pro každý projekt. Konfigurace jsou přiřazeny k projektům s názvem.|  
|`DefaultToVcxPlatformMapping`|Volitelné `string` výstupní parametr.<br /><br /> Obsahuje seznam oddělený středníkem mapování názvů platforem používaných<br /><br /> ve většině typů používaných souborů VCXPROJ.<br /><br /> Příklad:<br /><br /> `"AnyCPU=Win32;X86=Win32;X64=X64"`|  
|`VcxToDefaultPlatformMapping`|Nepovinné<br /><br /> `string` Výstupní parametr.<br /><br /> Obsahuje seznam oddělený středníkem mapování názvů platforem .vcxproj na názvy platformy používané většinou typů.<br /><br /> Příklad:<br /><br /> `"Win32=AnyCPU;X64=X64"`|  
|`CurrentProjectConfiguration`|Volitelné `string` výstupní parametr.<br /><br /> Obsahuje konfiguraci pro aktuální projekt.|  
|`CurrentProjectPlatform`|Volitelné `string` výstupní parametr.<br /><br /> Obsahuje platformu pro aktuální projekt.|  
|`OnlyReferenceAndBuildProjectsEnabledInSolutionConfiguration`|Volitelné `bool` výstupní parametr.<br /><br /> Obsahuje příznak označující, že odkazy by měly být sestaveny, i když byly zakázány v konfiguraci projektu.|  
|`ShouldUnsetParentConfigurationAndPlatform`|Volitelné `bool` výstupní parametr.<br /><br /> Obsahuje příznak označující, pokud nadřazená konfigurace a platforma mají být zrušeny.|  
|`OutputType`|Volitelné `string` výstupní parametr.<br /><br /> Obsahuje typ výstupu projektu.|  
|`ResolveConfigurationPlatformUsingMappings`|Volitelné `bool` výstupní parametr.<br /><br /> Obsahuje příznak označující, pokud sestavení má použít výchozí mapování k řešení konfigurace a platformy předané v odkazech projektu.|  
|`AssignedProjects`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> `[]` výstupní parametr.<br /><br /> Obsahuje seznam cest vyřešených odkazů.|  
|`UnassignedProjects`|Volitelné <xref:Microsoft.Build.Framework.ITaskItem> `[]` výstupní parametr.<br /><br /> Obsahuje seznam referenčních položek projektu, které nelze vyřešit pomocí předem vyřešených seznamů výstupů.|  
  
## <a name="remarks"></a>Poznámky  
 Kromě výše uvedených parametrů zdědí tento úkol parametry ze <xref:Microsoft.Build.Tasks.TaskExtension> třída, která sama dědí z <xref:Microsoft.Build.Utilities.Task> třídy. Seznam těchto dalších parametrů a jejich popisy najdete v tématu [taskextension – základní třída](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Viz také  
 [Úlohy](../msbuild/msbuild-tasks.md)   
 [Referenční dokumentace úlohy](../msbuild/msbuild-task-reference.md)



