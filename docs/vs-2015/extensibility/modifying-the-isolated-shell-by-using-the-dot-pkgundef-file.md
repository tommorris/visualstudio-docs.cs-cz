---
title: Úprava izolovaného prostředí pomocí. Soubor Pkgundef | Dokumentace Microsoftu
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
- Visual Studio shell, isolated mode%2C .pkgundef file
ms.assetid: 9cee2a20-f8ac-4d9d-aef9-068fcd9f27a4
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3741fc9abdae6693670538c80288dfdefcefd84e
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42631465"
---
# <a name="modifying-the-isolated-shell-by-using-the-pkgundef-file"></a>Úprava izolovaného prostředí pomocí. Soubor Pkgundef
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [úpravy izolované prostředí s použitím. Soubor Pkgundef](https://docs.microsoft.com/visualstudio/extensibility/modifying-the-isolated-shell-by-using-the-dot-pkgundef-file).  
  
Úpravou souboru .pkgundef vyloučit položky registru z aplikací izolovaného prostředí. Obvykle při prvním spuštění aplikace na počítači, prostředí sady Visual Studio zkopíruje existující položky registru sady Visual Studio kořenový klíč registru pro aplikaci. To zahrnuje všechny odkazy na aktuálně nainstalované rozšíření VSPackages.  
  
 Vyloučit konkrétní registru z aplikací izolovaného prostředí, přidejte do souboru .pkgundef aplikace klíč balíčku a potom v položce. Klíče a položky jsou reprezentovány jako v případě souboru .pkgdef. To znamená jako [$RootKey$] nebo [$RootKey$\\*podklíč*] a "*položka*" =*hodnotu*, kde *podklíč* je podklíč chcete ovlivnit, *položka* položkou odebrat, a *hodnotu* je buď `""` nebo `dword:00000000`.  
  
 Pokud chcete vyloučit z klíče registru více položek, pouze seznamu klíč jednou, za nímž následuje řádek pro každou položku pro vyloučení.  
  
 Klíč registru celý vyloučit z aplikací izolovaného prostředí, přidejte klíč k souboru .pkgundef aplikace, ale ne všechny položky registru pro daný klíč.  
  
 Můžete přidat komentáře k souboru .pkgundef. Jednořádkový komentář musí mít dvě lomítka jako první dva znaky.  
  
 Například, chcete-li odebrat **připojit k databázi** a **připojit k poskytování r** příkazy na **nástroje** nabídky, zrušte komentář u řádku:  
  
```  
[$RootKey$\Packages\{8D8529D3-625D-4496-8354-3DAD630ECC1B}]  
```  
  
 a přidejte řádek:  
  
```  
[$RootKey$\Packages\{198E76C1-34C0-424D-9957-B3EBD80265FB}]  
```  
  
 do souboru .pkgundef vaší aplikace.  
  
## <a name="see-also"></a>Viz také  
 [Identifikátory GUID balíčků funkcí sady Visual Studio](../extensibility/package-guids-of-visual-studio-features.md)   
 [Přizpůsobení izolovaného prostředí](../extensibility/customizing-the-isolated-shell.md)

