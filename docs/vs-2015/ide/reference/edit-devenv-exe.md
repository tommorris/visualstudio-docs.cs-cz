---
title: -Upravit (devenv.exe) | Dokumentace Microsoftu
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
- Devenv, /edit switch
- /Edit Devenv swtich
ms.assetid: 02b3d6e7-a2b1-4d83-a747-aa8c2fb758b7
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b61e79561d8bf2ae6bd456ad4ac91ea684491ed5
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42678795"
---
# <a name="edit-devenvexe"></a>/Edit (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [– upravit (devenv.exe)](https://docs.microsoft.com/visualstudio/ide/reference/edit-devenv-exe).  
  
  
Zadaný soubor se otevře v existující instanci [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Devenv /edit [file1[ file2]]  
```  
  
## <a name="arguments"></a>Arguments  
 `file1`  
 Volitelné. Soubor otevřete v existující instanci [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. Pokud žádná instance [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] existuje, se zjednodušeným rozložením okna, je vytvořena nová instance a `file1` se otevře v nové instanci.  
  
 `file2`  
 Volitelné. Nejméně jeden další soubor otevřete v existující instanci systému [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="remarks"></a>Poznámky  
 Pokud není určen žádný soubor, a existující instanci [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], existující instanci [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] získá fokus. Pokud není určen žádný soubor a neexistuje žádná existující instance [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], novou instanci třídy [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] vytvoření se zjednodušeným rozložením okna.  
  
 Pokud existující instanci systému [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] je v modálního stavu, například, pokud [dialogové okno Možnosti](../../ide/reference/options-dialog-box-visual-studio.md) je otevřete, bude soubor otevřít v existující instanci, kdy [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ukončí modální stav.  
  
## <a name="example"></a>Příklad  
 Tento příklad otevře soubor `MyFile.cs` v existující instanci [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] nebo otevře soubor v nové instanci [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Pokud ještě neexistuje.  
  
```  
devenv /edit MyFile.cs  
```  
  
## <a name="see-also"></a>Viz také  
 [Devenv – přepínače příkazového řádku](../../ide/reference/devenv-command-line-switches.md)



