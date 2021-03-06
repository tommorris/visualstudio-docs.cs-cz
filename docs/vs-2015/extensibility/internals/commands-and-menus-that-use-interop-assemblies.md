---
title: Příkazy a nabídky, které používají spolupracující sestavení | Dokumentace Microsoftu
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
- menus, using interop assemblies
- interop assemblies, using in commands and menus
- commands, handling using interop assemblies
- command handling with interop assemblies
ms.assetid: 8f4af525-39e5-4e69-92c8-d3efabe80bb2
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d050f2e96eb78462f9e5e77504a365d17ed01d6d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633342"
---
# <a name="commands-and-menus-that-use-interop-assemblies"></a>Příkazy a nabídky, které používají definiční sestavení
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [příkazů a nabídek, že použití zprostředkovatele komunikace s objekty sestavení](https://docs.microsoft.com/visualstudio/extensibility/internals/commands-and-menus-that-use-interop-assemblies).  
  
Musí se VSPackage, která implementuje příkazy nabídek a panelů nástrojů pomocí spolupracujícího sestavení:  
  
-   Informujte [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] integrované vývojové prostředí (IDE) o příkazech podporuje a určuje, zda jsou aktuálně povoleny.  
  
-   Proto zavázala dodržovat pravidla (smlouvy) pro zpracování příkazů.  
  
-   Explicitní implementace manipulaci s použitím buď <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> nebo <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> rozhraní.  
  
 Následující popisuje, jak k provádění těchto úkolů.  
  
## <a name="in-this-section"></a>V tomto oddílu  
 [Určení stavu příkazu pomocí spolupracujícího sestavení](../../extensibility/internals/determining-command-status-by-using-interop-assemblies.md)  
 Popisuje, jak VSPackage upozorní rozhraní IDE o příkazech, které podporuje, a určuje, zda jsou aktuálně povoleny.  
  
 [Kontrakty příkazů ve spolupracujícím sestavení](../../extensibility/internals/command-contracts-in-interop-assemblies.md)  
 Poskytuje definici kontraktu základní příkaz používá všechna rozšíření VSPackages provádění příkazů pomocí sestavení vzájemné spolupráce  
  
 [Implementace](../../extensibility/internals/command-implementation.md)  
 Poskytuje přehled o způsob VSPackage implementace příkazu.  
  
 [Registrace obslužných rutin příkazů spolupracujícího sestavení](../../extensibility/internals/registering-interop-assembly-command-handlers.md)  
 Popisuje položky registru, který je potřeba upozornit integrované vývojové prostředí, že poskytuje VSPackage obslužná rutina příkazu.  
  
## <a name="related-sections"></a>Související oddíly  
 [Dostupnost](../../extensibility/internals/command-availability.md)  
 Popisuje kritéria, která se používají integrovaným vývojovým prostředím určíte, které VSPackage příkazy jsou k dispozici a objekt je zpracovává.  
  
 [Jak balíčky VSPackages přidávají prvky uživatelského rozhraní](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)  
 Obsahuje podrobné informace o tom, jak vytvořit uživatelské rozhraní, která používá [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] příkaz podpory.  
  
 [Směrování příkazů v balíčcích VSPackage](../../extensibility/internals/command-routing-in-vspackages.md)  
 Přehled procesu je používán k propojení objektu s žádostí o správný příkaz.

