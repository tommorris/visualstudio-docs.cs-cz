---
title: Implementace zpracování příkazů pro vnořené projekty | Dokumentace Microsoftu
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
- nested projects, implementing command handling
ms.assetid: 48a9d66e-d51c-4376-a95a-15796643a9f2
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ea27ea6f1b1ef49174b555fb9b1aae0d4c54dd23
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42678788"
---
# <a name="implementing-command-handling-for-nested-projects"></a>Implementace zpracování příkazů pro vnořené projekty
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [implementace zpracování příkazu pro vnořené projekty](https://docs.microsoft.com/visualstudio/extensibility/internals/implementing-command-handling-for-nested-projects).  
  
Rozhraní IDE lze předat příkazy, které se předají <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> a <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> rozhraní pro vnořené projekty nebo nadřazené projekty můžete filtrovat nebo přepište příkazy.  
  
> [!NOTE]
>  Dají se filtrovat jenom příkazy, které obvykle zpracovává nadřazený projekt. Příkazy, jako **sestavení** a **nasadit** , které jsou zpracovávány integrovaného vývojového prostředí se nedají filtrovat.  
  
 Následující kroky popisují proces pro implementaci zpracování příkazu.  
  
## <a name="procedures"></a>Procedury  
  
#### <a name="to-implement-command-handling"></a>K implementaci zpracování příkazu  
  
1.  Když uživatel vybere vnořený projekt nebo uzlu v vnořený projekt:  
  
    1.  Volání rozhraní IDE <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> metody.  
  
     – nebo –  
  
    1.  Pokud příkaz vytvoří se v okně hierarchie, například příkaz místní nabídky v Průzkumníku řešení, zavolá rozhraní IDE <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A> metodu na nadřazený objekt projektu.  
  
2.  Nadřazený projekt můžete prozkoumat parametry, které se mají předat `QueryStatus`, jako například `pguidCmdGroup` a `prgCmds`, chcete-li zjistit, zda by měl nadřazený projekt filtrování příkazů. Pokud nadřazený projekt je implementováno s cílem filtrovat příkazy, by měl nastavit:  
  
    ```  
    prgCmds[0].cmdf = OLECMDF_SUPPORTED;  
    // make sure it is disabled  
    prgCmds[0].cmdf &= ~MSOCMDF_ENABLED;  
    ```  
  
     Pak by měl vrátit nadřazený projekt `S_OK`.  
  
     Pokud nadřazený projekt nefiltruje příkazu, měla by jenom vrátit `S_OK`. V tomto případě rozhraní IDE automaticky směruje příkaz podřízený projekt.  
  
     Nadřazený projekt nebude muset příkaz směrovat podřízeného projektu. Integrované vývojové prostředí provádí tento úkol...  
  
## <a name="see-also"></a>Viz také  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy>   
 [Příkazy, nabídky a panely nástrojů](../../extensibility/internals/commands-menus-and-toolbars.md)   
 [Vnoření projektů](../../extensibility/internals/nesting-projects.md)

