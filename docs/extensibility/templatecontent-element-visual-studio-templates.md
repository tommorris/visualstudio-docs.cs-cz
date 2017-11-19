---
title: "TemplateContent – Element (šablony sady Visual Studio) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/vstemplate/2005#TemplateContent
helpviewer_keywords: TemplateContent element [Visual Studio project templates]
ms.assetid: 90ae401c-b294-49ac-98da-e0d274f5bebb
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1f083097ae79d045891b64d806820a58686b4c95
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="templatecontent-element-visual-studio-templates"></a>TemplateContent – element (šablony sady Visual Studio)
Určuje obsah šablony.  
  
 \<VSTemplate >  
 \<TemplateContent >  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<TemplateContent>  
    ...  
</TemplateContent>  
```  
  
## <a name="attributes-and-elements"></a>Atributy a elementy  
 Následující části popisují atributy, podřízené prvky a nadřazené prvky.  
  
### <a name="attributes"></a>Atributy  
  
|Atribut|Popis|  
|---------------|-----------------|  
|[Buildonload –](../extensibility/buildprojectonload-visual-studio-templates.md)|Určuje, jestli při vytvoření projektu ze šablony vytvořit řešení.|  
  
### <a name="child-elements"></a>Podřízené elementy  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[Projectcollection –](../extensibility/projectcollection-element-visual-studio-templates.md)|Volitelný element.<br /><br /> Určuje uspořádání a obsah víceprojektových šablon.|  
|[Projekt](../extensibility/project-element-visual-studio-templates.md)|Volitelný element.<br /><br /> Určuje soubory nebo adresáře, které chcete přidat do projektu.|  
|[Odkazy](../extensibility/references-element-visual-studio-templates.md)|Volitelný element.<br /><br /> Určuje odkazy na sestavení, které jsou potřebné pro šablony položky.|  
|[ProjectItem –](../extensibility/projectitem-element-visual-studio-item-templates.md)|Volitelný element.<br /><br /> Určuje soubor v šabloně.|  
|[CustomParameters](../extensibility/customparameters-element-visual-studio-templates.md)|Volitelný element.<br /><br /> Určuje žádné vlastní parametry, které mají být použita při projekt nebo položku ze šablony.|  
  
### <a name="parent-elements"></a>Nadřazené elementy  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[VSTemplate](../extensibility/vstemplate-element-visual-studio-templates.md)|Požadovaný element.<br /><br /> Obsahuje všechna metadata pro šablony projektu, šablony položky nebo starter kit.|  
  
## <a name="remarks"></a>Poznámky  
 `TemplateContent`je požadovaný element.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje metadata pro šablona projektu pro [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] aplikace.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic starter kit</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="MyStarterKit.csproj">  
            <ProjectItem>Form1.cs<ProjectItem>  
            <ProjectItem>Form1.Designer.cs</ProjectItem>  
            <ProjectItem>Program.cs</ProjectItem>  
            <ProjectItem>Properties\AssemblyInfo.cs</ProjectItem>  
            <ProjectItem>Properties\Resources.resx</ProjectItem>  
            <ProjectItem>Properties\Resources.Designer.cs</ProjectItem>  
            <ProjectItem>Properties\Settings.settings</ProjectItem>  
            <ProjectItem>Properties\Settings.Designer.cs</ProjectItem>  
        </Project>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Viz také  
 [Odkaz na schéma šablon sady Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Vytváření šablon projektů a položek](../ide/creating-project-and-item-templates.md)