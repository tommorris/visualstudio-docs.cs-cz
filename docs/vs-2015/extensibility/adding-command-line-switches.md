---
title: Přidání přepínačů příkazového řádku | Dokumentace Microsoftu
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
- command-line switches, adding
- command-line switches, retrieving
- IVsAppCommandLine::GetOption method
- command line, switches
ms.assetid: 8bbbd87e-76fe-4fb5-8ef9-65f5e31967cf
caps.latest.revision: 22
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d4a9b9041183b22612c36e98f502d01ee3b62e36
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42671198"
---
# <a name="adding-command-line-switches"></a>Přidání přepínačů příkazového řádku
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [přidáním přepínače příkazového řádku](https://docs.microsoft.com/visualstudio/extensibility/adding-command-line-switches).  
  
Můžete přidat přepínače příkazového řádku, které se vztahují k vaší VSPackage při spuštění devenv.exe. Použití <xref:Microsoft.VisualStudio.Shell.ProvideAppCommandLineAttribute> deklarovat název přepínače a její vlastnosti. V tomto příkladu se přidá MySwitch přepínač pro podtřídou třídy s názvem balíčku VSPackage **AddCommandSwitchPackage** bez argumentů a s VSPackage načteny automaticky.  
  
```csharp  
[ProvideAppCommandLine("MySwitch", typeof(AddCommandSwitchPackage), Arguments = "0", DemandLoad = 1)]  
```  
  
 V následující tabulce jsou uvedeny pojmenované parametry  
  
 Arguments  
 Počet argumentů pro přepínač. Může být "*", nebo seznam argumentů.  
  
 DemandLoad  
 Automaticky načte sady VSPackage, pokud je nastavené na hodnotu 1, v opačném případě nastavte na hodnotu 0.  
  
 HelpString  
 Řetězec nebo prostředek ID nápovědy řetězce k zobrazení s **devenv /?**.  
  
 Název  
 Přepínač.  
  
 Packageguid došlo k chybě  
 Identifikátor GUID balíčku.  
  
 První hodnota argumentů je obvykle 0 nebo 1. Zvláštní hodnota "*" lze použít k označení, že celý zbytek příkazového řádku je argumentem. To může být užitečné pro ladění scénářů, kdy uživatel musí předat řetězec příkazu ladicího programu.  
  
 Hodnota DemandLoad je buď `true` (1) nebo `false` (0) označuje, že sady VSPackage by měly být načteny automaticky.  
  
 HelpString hodnotu ID prostředku řetězce, který se zobrazí devenv /? Zobrazení nápovědy. Tato hodnota by měla být ve tvaru "#nnn" kde nnn je celé číslo. Hodnota řetězce v souboru prostředků by měly končit znak nového řádku.  
  
 Hodnota Name je název přepínače.  
  
 Hodnota packageguid došlo k chybě je identifikátor GUID balíčku, který implementuje tento přepínač. Integrované vývojové prostředí používá tento identifikátor GUID k nalezení sady VSPackage v registru, ke kterému se vztahuje přepínač příkazového řádku.  
  
## <a name="retrieving-command-line-switches"></a>Načítání přepínače příkazového řádku  
 Při načítání vašeho balíčku můžete načíst přepínače příkazového řádku pomocí následujících kroků.  
  
1.  Ve vaší VSPackage <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A> implementace, volání `QueryService` na <xref:Microsoft.VisualStudio.Shell.Interop.SVsAppCommandLine> zobrazíte <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine> rozhraní.  
  
2.  Volání <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine.GetOption%2A> načíst přepínače příkazového řádku, které zadal uživatel.  
  
 Následující kód ukazuje, jak zjistit, zda byl zadán přepínač příkazového řádku MySwitch uživatelem:  
  
```csharp  
IVsAppCommandLine cmdline = (IVsAppCommandLine)GetService(typeof(SVsAppCommandLine));  
  
int isPresent = 0;  
string optionValue = "";  
  
cmdline.GetOption("MySwitch", out isPresent, out optionValue);  
```  
  
 Je vaší odpovědností, abyste pro vaše přepínače příkazového řádku zkontrolujte pokaždé, když je načten do balíčku.  
  
## <a name="see-also"></a>Viz také  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A>   
 [Přepínače příkazového řádku nástroje devenv](../ide/reference/devenv-command-line-switches.md)   
 [Nástroj CreatePkgDef](../extensibility/internals/createpkgdef-utility.md)   
 [. Soubory Pkgdef](../extensibility/modifying-the-isolated-shell-by-using-the-dot-pkgdef-file.md)

