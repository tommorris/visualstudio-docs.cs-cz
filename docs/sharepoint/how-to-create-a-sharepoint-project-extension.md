---
title: 'Postupy: vytváření rozšíření projektu služby SharePoint | Microsoft Docs'
ms.custom: ''
ms.date: 04/28/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- projects [SharePoint development in Visual Studio], extending
- SharePoint development in Visual Studio, extending projects
- SharePoint projects, extending
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 25644a11ddbef3f8d493b64f8ca288dbaa87a14c
ms.sourcegitcommit: d9e4ea95d0ea70827de281754067309a517205a1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2018
ms.locfileid: "37120178"
---
# <a name="how-to-create-a-sharepoint-project-extension"></a>Postupy: vytváření rozšíření projektu SharePoint
  Vytváření rozšíření projektu, pokud chcete přidat další funkce žádné projektu služby SharePoint, který je otevřen v sadě Visual Studio. Další informace najdete v tématu [rozšíření systému projektu služby SharePoint](../sharepoint/extending-the-sharepoint-project-system.md).  

### <a name="to-create-a-project-extension"></a>K vytváření rozšíření projektu  

1.  Vytvoření projektu knihovny tříd.  

2.  Přidejte odkazy na následující sestavení:  

    -   Microsoft.VisualStudio.SharePoint  

    -   System.ComponentModel.Composition  

3.  Vytvořte třídu, která implementuje <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> rozhraní.  

4.  Přidat <xref:System.ComponentModel.Composition.ExportAttribute> k třídě. Tento atribut umožňuje sadě Visual Studio zjišťovat a načíst vaše <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> implementace. Předat <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> typ do konstruktoru atributu.  

5.  V implementaci <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension.Initialize%2A> metoda, použijte členy *projectService* parametr pro definování chování rozšíření. Tento parametr je <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService> objekt, který poskytuje přístup k událostí definovaných v <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents> rozhraní.  

## <a name="example"></a>Příklad  
 Následující příklad kódu ukazuje, jak vytvořit jednoduchý projekt rozšíření, která zpracovává většinu události projektu služby SharePoint, které jsou definovány <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents> rozhraní. K testování kódu, vytvoření projektu služby SharePoint v [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] a potom přidejte další projekty k řešení, změňte hodnoty vlastností projektu, nebo odstranit nebo vyloučit projektu. Rozšíření vás upozorní na události napsáním zprávy a pokuste se **výstup** okno a **seznam chyb** okno.  

  ```vb  
    Imports Microsoft.VisualStudio.SharePoint
    Imports System.ComponentModel
    Imports System.ComponentModel.Composition

    Namespace Contoso.ExampleProjectExtension
      <Export(GetType(ISharePointProjectExtension))> _
      Class ExampleProjectExtension
        Implements ISharePointProjectExtension

        Private WithEvents projectService As ISharePointProjectService

        Public Sub Initialize(ByVal projectService As ISharePointProjectService) _
            Implements ISharePointProjectExtension.Initialize
            Me.projectService = projectService
        End Sub

        ' A project was added.
        Private Sub projectService_ProjectAdded(ByVal sender As Object, ByVal e As SharePointProjectEventArgs) _
            Handles projectService.ProjectAdded
            Dim project As ISharePointProject = CType(sender, ISharePointProject)
            Dim message As String = String.Format("The following project was added: {0}", e.Project.Name)
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message)
        End Sub

        ' A project was loaded in the IDE.
        Private Sub projectService_ProjectInitialized(ByVal sender As Object, ByVal e As SharePointProjectEventArgs) _
            Handles projectService.ProjectInitialized
            Dim project As ISharePointProject = CType(sender, ISharePointProject)
            Dim message As String = String.Format("The following project is being initialized: {0}", e.Project.Name)
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message)
        End Sub

        ' The name of a property was changed.
        Private Sub projectService_ProjectNameChanged(ByVal sender As Object, ByVal e As NameChangedEventArgs) _
            Handles projectService.ProjectNameChanged
            Dim project As ISharePointProject = CType(sender, ISharePointProject)
            Dim message As String = String.Format("The project named {0} was changed to {1}.", e.OldName, project.Name)
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message)
        End Sub

        ' A project property value was changed.
        Private Sub ProjectPropertyChanged(ByVal sender As Object, ByVal e As PropertyChangedEventArgs) _
            Handles projectService.ProjectPropertyChanged
            Dim project As ISharePointProject = CType(sender, ISharePointProject)
            Dim message As String = String.Format("The following property of the {0} project was changed: {1}",
                project.Name, e.PropertyName)
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message)
        End Sub

        ' A project is being removed or unloaded.
        Private Sub projectService_ProjectRemoved(ByVal sender As Object, ByVal e As SharePointProjectEventArgs) _
            Handles projectService.ProjectRemoved
            Dim project As ISharePointProject = CType(sender, ISharePointProject)
            Dim message As String = String.Format("The following project is being removed or unloaded: {0}", e.Project.Name)
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message)
        End Sub

        ' A project was removed or unloaded.
        Private Sub projectService_ProjectDisposing(ByVal sender As Object, ByVal e As SharePointProjectEventArgs) _
            Handles projectService.ProjectDisposing
            Dim project As ISharePointProject = CType(sender, ISharePointProject)
            Dim message As String = String.Format("The following project was removed or unloaded: {0}", e.Project.Name)
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message)
        End Sub
      End Class
    End Namespace  
    ```  

    ```csharp  
    using Microsoft.VisualStudio.SharePoint;
    using System;
    using System.ComponentModel;
    using System.ComponentModel.Composition;

    namespace Contoso.ExampleProjectExtension
    {
      [Export(typeof(ISharePointProjectExtension))]
      internal class ExampleProjectExtension : ISharePointProjectExtension
      {
        public void Initialize(ISharePointProjectService projectService)
        {
            projectService.ProjectAdded += projectService_ProjectAdded;
            projectService.ProjectInitialized += projectService_ProjectInitialized;
            projectService.ProjectNameChanged += projectService_ProjectNameChanged;
            projectService.ProjectPropertyChanged += projectService_ProjectPropertyChanged;
            projectService.ProjectRemoved += projectService_ProjectRemoved;
            projectService.ProjectDisposing += projectService_ProjectDisposing;
        }

        // A project was added.
        void projectService_ProjectAdded(object sender, SharePointProjectEventArgs e)
        {
            ISharePointProject project = (ISharePointProject)sender;
            string message = String.Format("The following project was added: {0}", e.Project.Name);
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message);
        }

        // A project is loaded in the IDE.
        void projectService_ProjectInitialized(object sender, SharePointProjectEventArgs e)
        {
            ISharePointProject project = (ISharePointProject)sender;
            string message = String.Format("The following project is being initialized: {0}", e.Project.Name);
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message);
        }

        // The name of a project was changed.
        void projectService_ProjectNameChanged(object sender, NameChangedEventArgs e)
        {
            ISharePointProject project = (ISharePointProject)sender;
            string message = String.Format("The project named {0} was changed to {1}.", e.OldName, project.Name);
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message);
        }

        // A project property value was changed.
        private void projectService_ProjectPropertyChanged(object sender, PropertyChangedEventArgs e)
        {
            ISharePointProject project = (ISharePointProject)sender;
            string message = String.Format("The following property of the {0} project was changed: {1}",
                project.Name, e.PropertyName);
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message);
        }

        // A project is being removed or unloaded.
        void projectService_ProjectRemoved(object sender, SharePointProjectEventArgs e)
        {
            ISharePointProject project = (ISharePointProject)sender;
            string message = String.Format("The following project is being removed or unloaded: {0}", e.Project.Name);
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message);
        }

        // A project was removed or unloaded.
        void projectService_ProjectDisposing(object sender, SharePointProjectEventArgs e)
        {
            ISharePointProject project = (ISharePointProject)sender;
            string message = String.Format("The following project was removed or unloaded: {0}", e.Project.Name);
            project.ProjectService.Logger.WriteLine(message, LogCategory.Message);
        }
     }
  }  
  ```  

Tento příklad používá zapsat zprávu do projektu služby SharePoint **výstup** okno a **seznam chyb** okno. Další informace najdete v tématu [použití služby projektu služby SharePoint](../sharepoint/using-the-sharepoint-project-service.md).  

 Příklady, které ukazují, jak zpracovat <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectMenuItemsRequested> a <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectPropertiesRequested> události, viz [postupy: Přidání položky místní nabídky do projektů služby SharePoint](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md) a [postupy: Přidání vlastnosti do projektů služby SharePoint](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md).  

## <a name="compile-the-code"></a>Kompilace kódu  
 Tento příklad vyžaduje odkazy na následující:  

-   Microsoft.VisualStudio.SharePoint  

-   System.ComponentModel.Composition  

## <a name="deploy-the-extension"></a>Nasazení rozšíření  
 Chcete-li nasadit rozšíření, vytvořte [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] balíček rozšíření (VSIX) pro sestavení a všechny další soubory, které chcete distribuovat s rozšířením. Další informace najdete v tématu [nástroje pro nasazení rozšíření pro SharePoint v sadě Visual Studio](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  

## <a name="see-also"></a>Viz také:
 [Rozšíření systému projektu služby SharePoint](../sharepoint/extending-the-sharepoint-project-system.md)   
 [Postupy: Přidání položky místní nabídky do projektů služby SharePoint](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md)   
 [Postupy: Přidání vlastnosti do projektů služby SharePoint](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md)   
 [Návod: Vytváření rozšíření projektu SharePoint](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md)  
