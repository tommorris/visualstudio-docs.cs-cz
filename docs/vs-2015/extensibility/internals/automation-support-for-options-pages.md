---
title: Podpora automatizace pro stránky Možnosti | Dokumentace Microsoftu
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
- Tools Options pages [Visual Studio SDK], automation support
- automation [Visual Studio SDK], creating Tools Options pages
ms.assetid: 0b25b82c-7432-4e0a-9e84-350269ba8260
caps.latest.revision: 30
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9f7a9a9cf13a50cf13817b4c3b12bd1da1e8370b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42667123"
---
# <a name="automation-support-for-options-pages"></a>Podpora automatizace pro stránky Možnosti
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [podporu automatizace pro stránky možnosti](https://docs.microsoft.com/visualstudio/extensibility/internals/automation-support-for-options-pages).  
  
Rozšíření VSPackages můžete zadat vlastní **možnosti** dialogová okna pro **nástroje** v nabídce (stránek možnosti nástrojů) [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] a můžete zpřístupnit modelu automatizace.  
  
## <a name="tools-options-pages"></a>Stránky Možnosti nástrojů  
 Chcete-li vytvořit **možnosti nástrojů** stránce VSPackage musí poskytnout implementaci ovládacího prvku uživatel vrátí do prostředí prostřednictvím sady VSPackage provádění <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> metoda, (nebo pro spravovaný kód <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> Metoda).  
  
 Je volitelný, ale důrazně doporučujeme, pokud chcete povolit přístup na tuto novou stránku prostřednictvím modelu automatizace. Můžete provést pomocí následujících kroků:  
  
1.  Rozšíření <xref:EnvDTE._DTE.Properties%2A> objektu prostřednictvím implementace objektu odvozené rozhraní IDispatch.  
  
2.  Vrátila implementace rozhraní <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetAutomationObject%2A> – metoda (nebo pro spravovaný kód <xref:Microsoft.VisualStudio.Shell.Package.GetAutomationObject%2A> metoda) na objekt odvozené rozhraní IDispatch.  
  
3.  Když příjemci automatizace zavolá <xref:EnvDTE._DTE.Properties%2A> metodu na vlastní **možnost** stránka vlastností prostředí používá <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetAutomationObject%2A> metoda získat vlastní **možnosti nástrojů** automation na stránce implementace.  
  
4.  Objekt automatizace sady VSPackage je pak sloužit ke každé <xref:EnvDTE.Property> vrácený <xref:EnvDTE._DTE.Properties%2A>.  
  
 Ukázková implementace vlastní stránky Možnosti nástrojů, naleznete v tématu [VSSDK ukázky](../../misc/vssdk-samples.md).  
  
## <a name="see-also"></a>Viz také  
 [Zveřejňování objektů projektu](../../extensibility/internals/exposing-project-objects.md)

