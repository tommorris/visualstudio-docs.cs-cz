---
title: "Pomocí modelu automatizace | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: automation [Visual Studio SDK], automation model
ms.assetid: 0c7f7889-fbfb-4b19-804f-b742138baecd
caps.latest.revision: "15"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a6251a0d79b28b169e75d1dca3401231a7a30f22
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="using-the-automation-model"></a>Pomocí modelu automatizace
Po připojení vaší VSPackage automatizace, můžete získat vlastnosti a metody voláním <xref:EnvDTE.DTEClass.GetObject%2A> metodu <xref:EnvDTE._DTE> objekt, předávání řetězec představující objekt, který chcete načíst.  
  
## <a name="obtaining-project-objects"></a>Získání projektu objekty  
 Následují dva příklady kódu, které ukazují, jak příjemce automatizace získává projektu objekty automatizace. Informace o tom, jak získat objekt DTE najdete v tématu [postupy: získání odkazy na prostředí DTE a objekty DTE2](http://msdn.microsoft.com/Library/c92e3c8e-82e6-4a67-85da-e43c50ffd8e4).  
  
```vb  
Sub DoAutomation()  
    Dim MyProjects As Projects  
    MyProjects = DTE.GetObject("AcmeProject")  
End Sub  
```  
  
```cpp  
void DoAutomation(void)  
{  
  CComQIPtr<Projects> pMyPkg; // Use an IDispatch-derived object type.  
    pMyPkg = pDTE->GetObject("AcmeProjects");   
  
   // The '=' performs a Query Interface.  
   // Assumes pDTE is already available as a global.  
   // Use pMyPkg to access your projects object's properties and methods.  
}  
  
```  
  
 V tomto okamžiku můžete použít standardní projektu objekty, které jsou součástí konkrétní VSPackage přesunout dolů model hierarchie.  
  
 Následující příklad kódu ukazuje, jak získat vlastní objekt, který je vlastnost typu vlastních projektů.:  
  
```vb  
Dim MyPrj As Project  
Dim MyPrjItem As ProjectItem  
Dim objMyObject as MyExtendedObject  
  
MyPrj = MyProjects.Item(1) 'use the Projects collection to get a project  
objMyObject = MyPrj.Object 'You call .Object to get to special Project  
                           'implementation  
objMyObject.MySpecialMethodOrProperty  
```  
  
 Následující kód obsahuje názvy všech vlastností v [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] prostředí **Obecné** možnost **nástroje** nabídky:  
  
```vb  
dim objDTE  
dim objEnv  
set objDTE = CreateObject("VisualStudio.DTE")  
set objEnv = objDTE.Properties("Environment", "General")  
for each obj in ObjEnv  
MsgBox obj.Name  
Next  
  
```  
  
## <a name="see-also"></a>Viz také  
 <xref:EnvDTE.DTEClass.GetObject%2A>