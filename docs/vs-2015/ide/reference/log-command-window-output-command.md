---
title: Protokol příkazové okno výstup příkazu | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- tools.logcommandwindowoutput
helpviewer_keywords:
- log Command window output command
- View.LogCommandWindowOutput command
ms.assetid: d4ecec35-5af4-4954-8d60-2cd24583fbb4
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 9f6cdef31ec8988612815a76c30198e97ddf4c26
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42673864"
---
# <a name="log-command-window-output-command"></a>Protokolovat výstup příkazového okna – příkaz
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [protokolu příkaz okno výstupu příkazů](https://docs.microsoft.com/visualstudio/ide/reference/log-command-window-output-command).  
  
  
Zkopíruje všechny vstup a výstup z **příkaz** okna do souboru.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Tools.LogCommandWindowOutput [filename] [/on|/off] [/overwrite]  
```  
  
## <a name="arguments"></a>Arguments  
 `filename`  
 Volitelné. Název souboru protokolu. Ve výchozím nastavení je soubor vytvořen ve složce profilu uživatele. Pokud název souboru již existuje, protokol je připojen na konec existující soubor. Pokud není určen žádný soubor, poslední zadaný soubor se používá. Pokud neexistuje žádný předchozí soubor je vytvořen výchozí soubor protokolu, volá cmdline.log.  
  
> [!TIP]
>  Chcete-li změnit umístění pro uložení souboru protokolu, zadejte úplnou cestu souboru, ohraničená uvozovkami, pokud cesta obsahuje mezery.  
  
## <a name="switches"></a>Přepínače  
 parametrů /on  
 Volitelné. Spuštění protokolu **příkaz** okno v zadaném souboru a přidá soubor s novými informacemi.  
  
 / vypnuto  
 Volitelné. V protokolu se zastaví **příkaz** okna.  
  
 / overwrite  
 Volitelné. Pokud soubor zadaný v `filename` argument odpovídá existující soubor, soubor se přepíše.  
  
## <a name="remarks"></a>Poznámky  
 Pokud není určen žádný soubor, vytvoří se soubor cmdline.log ve výchozím nastavení. Ve výchozím nastavení je alias pro tento příkaz protokolu.  
  
## <a name="examples"></a>Příklady  
 Tento příklad vytvoří nový soubor protokolu, cmdlog a spustí příkaz protokolu.  
  
```  
>Tools.LogCommandWindowOutput cmdlog  
```  
  
 Tento příklad zastaví protokolování příkazy.  
  
```  
>Tools.LogCommandWindowOutput /off  
```  
  
 Tento příklad pokračuje v protokolování příkazy v předchozích souboru protokolu.  
  
```  
>Tools.LogCommandWindowOutput /on  
```  
  
## <a name="see-also"></a>Viz také  
 [Příkazy sady Visual Studio](../../ide/reference/visual-studio-commands.md)   
 [Okno příkazového řádku](../../ide/reference/command-window.md)   
 [Pole najít/příkaz](../../ide/find-command-box.md)   
 [Aliasy příkazů sady Visual Studio](../../ide/reference/visual-studio-command-aliases.md)



