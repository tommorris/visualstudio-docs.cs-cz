---
title: Createnewfolder – Element (šablony sady Visual Studio) | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#CreateNewFolder
helpviewer_keywords:
- CreateNewFolder element [Visual Studio project templates]
ms.assetid: acef2016-4140-45d6-ace8-b8160eabd676
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 42b01012a6a15dbf31782ccf4dd4502338ce4595
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42632223"
---
# <a name="createnewfolder-element-visual-studio-templates"></a>CreateNewFolder – element (šablony sady Visual Studio)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [createnewfolder – Element (šablony sady Visual Studio)](https://docs.microsoft.com/visualstudio/extensibility/createnewfolder-element-visual-studio-templates).  
  
Určuje, jestli se má zkontrolovat, že cílový adresář, ve kterém se má vytvořit projekt neexistuje. Pokud adresář neexistuje, lze vytvořit nový adresář pro projekt. Toto nastavení je obvykle přepsat `NewProjectRequiresNewFolder(VsTemplate)` příznak registru (`HKEY_LOCAL_MACHINE/SOFTWARE(/Wow6432Node)/Microsoft/VisualStudio/<version number>/Projects/<project GUID>`), že všechny běžné typy projektů použít k určení, zda chcete vytvořit nový projekt v novém adresáři.  
  
 \<Vstemplate – >  
 \<TemplateData >  
 \<Createnewfolder – >  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<CreateNewFolder>  
    true/false  
</CreateNewFolder>  
```  
  
## <a name="type"></a>Typ  
 `Boolean`  
  
## <a name="attributes-and-elements"></a>Atributy a elementy  
 Následující části popisují atributy, podřízené prvky a nadřazené prvky.  
  
### <a name="attributes"></a>Atributy  
 Žádné  
  
### <a name="child-elements"></a>Podřízené elementy  
 Žádné  
  
### <a name="parent-elements"></a>Nadřazené elementy  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[TemplateData –](../extensibility/templatedata-element-visual-studio-templates.md)|Požadovaný element.<br /><br /> Rozděluje šablonu a definuje, jak se zobrazuje **nový projekt** nebo **přidat novou položku** dialogové okno.|  
  
## <a name="text-value"></a>Textová hodnota  
 Je vyžadována textová hodnota.  
  
 Text musí být buď `true` nebo `false`, která udává, zda je či není by měla být vytvořena nová složka kontejneru při vytvoření projektu ze šablony.  
  
## <a name="remarks"></a>Poznámky  
 `CreateNewFolder` je volitelný prvek. Výchozí hodnota je `true`.  
  
 Hodnota zadaná v `CreateNewFolder` element pouze kompilátorem respektovány [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Pokud podkladový systém projektu podporuje.  
  
## <a name="example"></a>Příklad  
 Následující příklad kódu určuje nechcete vytvořit novou složku, pokud je projekt vytvořen z šablony.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic template</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <CreateNewFolder>false</CreateNewFolder>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="MyTemplate.csproj">  
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

