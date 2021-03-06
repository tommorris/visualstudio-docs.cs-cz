---
title: Úprava izolovaného prostředí pomocí. Vsct soubor | Dokumentace Microsoftu
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
- Visual Studio shell, isolated mode%2C .vsct file
ms.assetid: 6d147c2d-10e9-400e-b8ce-5566287b41ba
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0606d28f151f0d9c85980121e3129bd9204c61b8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42676126"
---
# <a name="modifying-the-isolated-shell-by-using-the-vsct-file"></a>Úprava izolovaného prostředí pomocí. Soubor Vsct
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [úpravy izolované prostředí s použitím. Soubor Vsct](https://docs.microsoft.com/visualstudio/extensibility/modifying-the-isolated-shell-by-using-the-dot-vsct-file).  
  
Projekt uživatelského rozhraní pro projekt izolovaného prostředí sady Visual Studio obsahuje .vsct soubor, který umožňuje určit, které skupiny aplikací a jednotlivé příkazy jsou k dispozici v aplikaci. Následuje výňatek ze souboru .vsct bez úprav.  
  
```  
<!-- <Define name="No_WindowListCommand"/> -->  
<!-- <Define name="No_MoreWindowsCommand"/> -->  
<!-- <Define name="No_PaneNextPaneCommand"/> -->  
<!-- <Define name="No_PanePrevPaneCommand"/> -->  
```  
  
 Ve výchozím nastavení jsou zahrnuty většinu příkazů a pro skupinu příkazů. Vyloučit příkaz nebo skupinu příkazů, jednoduše zrušte komentář u tohoto příkazu nebo skupině.  
  
 Například odebrat další podokno nebo předchozí podokno příkazů, zrušte komentář `No_PaneNextPaneCommand` a `No_PanePrevPaneCommand` položky:  
  
```  
  
<Define name="No_PaneNextPaneCommand"/> <Define name="No_PanePrevPaneCommand"/>  
  
```  
  
 Podrobnější příklad tato přizpůsobení, najdete v části [návod: vytvoření základní aplikace izolovaného prostředí](../extensibility/walkthrough-creating-a-basic-isolated-shell-application.md).  
  
## <a name="referenced-files"></a>Odkazované soubory  
 Výchozí soubor .vsct aplikace odkazuje na následující soubory. Tyto soubory jsou umístěny v podadresáři \VisualStudioIntegration\Common\Inc\ adresáře instalace sady Visual Studio SDK.  
  
|Soubor|Popis|  
|----------|-----------------|  
|wbids.h|Identity uživatelského rozhraní pro webové procházení balíček.|  
|AppIDCmdUsed.vsct|Tabulky příkazů pro primární prvky uživatelského rozhraní Visual Studio.|  
|EmulatorCmdUsed.vsct|Tabulky příkazů (emacs) a Přehled prvků uživatelského rozhraní editoru emulace.|  
|Vsdebugguids.h|Definuje identifikátory GUID příkazy, možnosti a další funkce ladicího programu sady Visual Studio.|  
|VsDbgCmdUsed.vsct|Tabulky příkazů v ladicím programu.|  
  
 Soubor AppIDCmdUsed.vsct obsahuje prvky uživatelského rozhraní Visual Studio podle symboly definované v souboru .vsct aplikace.  
  
 Další informace najdete v tématu [návrh tabulky příkazů XML (. Vsct) soubory](../extensibility/internals/designing-xml-command-table-dot-vsct-files.md) a [– referenční dokumentace schématu VSCT XML](../extensibility/vsct-xml-schema-reference.md).  
  
## <a name="see-also"></a>Viz také  
 [Izolované prostředí sady Visual Studio](../extensibility/visual-studio-isolated-shell.md)

