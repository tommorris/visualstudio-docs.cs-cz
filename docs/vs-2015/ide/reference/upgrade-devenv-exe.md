---
title: -Upgradu (devenv.exe) | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- /upgrade Devenv switch
- Devenv, /upgrade switch
- upgrade Devenv switch
ms.assetid: 3468045c-5cc9-4157-9a9d-622452145d27
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4dc3a9000056babd5a05577dfa95af42a824f538
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633343"
---
# <a name="upgrade-devenvexe"></a>/Upgrade (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [-upgradu (devenv.exe)](https://docs.microsoft.com/visualstudio/ide/reference/upgrade-devenv-exe).  
  
  
Aktualizuje soubor řešení a všechny jeho soubory projektu nebo zadaný pro aktuální soubor projektu [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] formáty pro tyto soubory.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
devenv SolutionFile | ProjectFile /upgrade  
```  
  
## <a name="arguments"></a>Arguments  
 `SolutionFile`  
 Povinné, pokud upgradujete celé řešení a jeho projekty. Cesta a název souboru řešení. Můžete zadat pouze název souboru řešení nebo úplnou cestu a název souboru řešení. Pokud složka nebo soubor s názvem ještě neexistuje, vytvoří se.  
  
 `ProjectFile`  
 Povinné, pokud upgradujete jeden projekt. Cesta a název souboru projektu v rámci řešení. Můžete zadat pouze název souboru projektu nebo úplnou cestu a název souboru projektu. Pokud složka nebo soubor s názvem ještě neexistuje, vytvoří se.  
  
## <a name="remarks"></a>Poznámky  
 Zálohy jsou automaticky vytvořeny a zkopírován do adresáře s názvem Zálohování, který je vytvořen v aktuálním adresáři.  
  
 Řešení se spravovanými zdroji nebo projekty musí být rezervován dříve, než je možné upgradovat.  
  
 Použití `/upgrade` přepínač nespustí [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. Výsledky upgradu lze zobrazit v sestavě upgradu pro vývojový jazyk řešení nebo projektu. Vrátí se žádné informace o chybě nebo použití. Další informace o upgradu projektů v [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], naleznete v tématu [postupy: řešení potíží s neúspěšné Visual Studio projekt upgrady](../../porting/how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades.md).  
  
## <a name="example"></a>Příklad  
 V tomto příkladu upgraduje soubor řešení s názvem "MyProject.sln" ve výchozí složce pro [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] řešení.  
  
```  
devenv "MyProject.sln" /upgrade  
```  
  
## <a name="see-also"></a>Viz také  
 [Postupy: řešení potíží s upgrady projektu úspěšné sady Visual Studio](../../porting/how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades.md)   
 [Devenv – přepínače příkazového řádku](../../ide/reference/devenv-command-line-switches.md)



