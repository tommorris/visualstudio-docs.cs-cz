---
title: Fullclassname – Element (rozšíření Průvodce pro šablony sady Visual Studio) | Dokumentace Microsoftu
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
- http://schemas.microsoft.com/developer/vstemplate/2005#FullClassName
helpviewer_keywords:
- FullClassName element [Visual Studio project template]
ms.assetid: 651e1010-d529-4856-85ff-c77ceca5d2ed
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 25f291d787a6efe03c6b8cf8dff27157f48d1596
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42680774"
---
# <a name="fullclassname-element-visual-studio-template-wizard-extension"></a>FullClassName – element (rozšíření průvodce pro šablony sady Visual Studio)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [fullclassname – Element (Visual Studio rozšíření Průvodce pro šablony)](https://docs.microsoft.com/visualstudio/extensibility/fullclassname-element-visual-studio-template-wizard-extension).  
  
Plně kvalifikovaný název třídy, která implementuje `IWizard` rozhraní.  
  
 \<Vstemplate – >  
 \<WizardExtension – >  
 ...  
 \<Fullclassname – >  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<FullClassName>ClassName</FullClassName>  
```  
  
## <a name="attributes-and-elements"></a>Atributy a elementy  
 Následující oddíly popisují atributy a podřízené a nadřazené elementy.  
  
### <a name="attributes"></a>Atributy  
 Žádné  
  
### <a name="child-elements"></a>Podřízené elementy  
 Žádné  
  
### <a name="parent-elements"></a>Nadřazené elementy  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[WizardExtension –](../extensibility/wizardextension-element-visual-studio-templates.md)|Obsahuje elementy registrace pro přizpůsobení Průvodce šablonou.|  
  
## <a name="text-value"></a>Textová hodnota  
 Je vyžadována textová hodnota.  
  
 Tento text určuje třídu, která implementuje `IWizard` rozhraní. Zadaná třída musí existovat v sestavení určeném parametrem [sestavení](../extensibility/assembly-element-visual-studio-template-wizard-extension.md) elementu.  
  
## <a name="remarks"></a>Poznámky  
 `FullClassName` je vyžadovaný podřízený prvek `WizardExtension`.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje metadata pro šablony standardní projektu pro [!INCLUDE[csprcs](../includes/csprcs-md.md)] aplikace Windows.  
  
```  
<VSTemplate Version="3.0.0" Type="Item"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyTemplate</Name>  
        <Description>Template using IWizard extension</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
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
    <WizardExtension>  
        <Assembly>MyWizard, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a, Custom=null</Assembly>  
        <FullClassName>MyWizard.CustomWizard</FullClassName>  
    </WizardExtension>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Viz také  
 [Odkaz na schéma šablon sady Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Vytváření šablon projektů a položek](../ide/creating-project-and-item-templates.md)   
 [Postupy: Použití průvodců se šablonami projektů](../extensibility/how-to-use-wizards-with-project-templates.md)

