---
title: 'Postupy: použití vyhrazených znaků XML v souborech projektu | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- MSBuild, using reserved XML characters
- MSBuild, reserved XML characters
ms.assetid: 1ae37275-96bf-4e6e-897b-6b048e5bbe93
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f045195a4e934fcb6e140da68528ca43f104136d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669386"
---
# <a name="how-to-use-reserved-xml-characters-in-project-files"></a>Postupy: Použití vyhrazených znaků XML v souborech projektu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: použití vyhrazených znaků jazyka XML v souborech projektu](https://docs.microsoft.com/visualstudio/msbuild/how-to-use-reserved-xml-characters-in-project-files).  
  
  
Při vytváření souborů projektu, můžete potřebovat použít vyhrazené znaky jazyka XML, třeba v hodnotách vlastnosti nebo hodnoty parametrů úloh. Nicméně některé znaky vyhrazené musí nahradit odpovídajícími pojmenovaná entita, tak, aby soubor projektu může být analyzován.  
  
## <a name="using-reserved-characters"></a>Použití vyhrazených znaků  
 Následující tabulka popisuje vyhrazených znaků jazyka XML, které se musí nahradit odpovídajícími odpovídající pojmenovaná entita tak, aby soubor projektu může být analyzován.  
  
|Vyhrazené znaky|Pojmenovaná entita|  
|------------------------|------------------|  
|\<|&lt;|  
|>|&gt;|  
|&|&amp;|  
|"|&quot;|  
|'|&apos;|  
  
#### <a name="to-use-double-quotes-in-a-project-file"></a>Použití dvojitých uvozovek v souboru projektu  
  
-   Nahraďte odpovídající entity s názvem dvojité uvozovky &quot;. Například umístit dvojitých uvozovek `EXEFile` seznam položek, zadejte:  
  
    ```  
    <Message Text="The output file is "@(EXEFile)"."/>  
    ```  
  
## <a name="example"></a>Příklad  
 V následujícím příkladu kódu dvojité uvozovky jsou používány zvýrazněte název souboru ve zprávě, která je výstupní soubor projektu.  
  
```  
<Project DefaultTargets="Compile"  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
    <!-- Set the application name as a property -->  
    <PropertyGroup>  
        <appname>"HelloWorldCS"</appname>  
    </PropertyGroup>  
    <!-- Specify the inputs -->  
    <ItemGroup>  
        <CSFile Include = "consolehwcs1.cs" />  
    </ItemGroup>  
    <Target Name = "Compile">  
        <!-- Run the Visual C# compilation using input  
        files of type CSFile -->  
        <Csc Sources = "@(CSFile)">  
            <!-- Set the OutputAssembly attribute of the CSC task  
            to the name of the executable file that is created -->  
            <Output  
                TaskParameter = "OutputAssembly"  
                ItemName = "EXEFile"/>  
        </Csc>  
        <!-- Log the file name of the output file -->  
        <Message Text="The output file is "@(EXEFile)"."/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Viz také  
 [Referenční dokumentace nástroje MSBuild](../msbuild/msbuild-reference.md) [MSBuild](msbuild.md)


