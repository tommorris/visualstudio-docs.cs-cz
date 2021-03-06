---
title: -Out (devenv.exe)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- errors [Visual Studio], builds
- Devenv, /out switch
- builds [Visual Studio], logs
- error logs [Visual Studio], command-line build errors
- error logs [Visual Studio]
- /out Devenv switch
- out Devenv switch
- builds [Visual Studio], errors
- output files, build errors
ms.assetid: 9002d8c2-36d4-451c-b489-8f01932f31f7
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 623f4e8a8a2f6e275c42507aa3839106f3a1dd2f
ms.sourcegitcommit: fe5a72bc4c291500f0bf4d6e0778107eb8c905f5
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2018
ms.locfileid: "33704483"
---
# <a name="out-devenvexe"></a>/Out (devenv.exe)
Určuje soubor pro uložení a zobrazení chyb při spouštění, sestavení, znovu sestavit nebo nasazení řešení.

## <a name="syntax"></a>Syntaxe

```cmd
devenv /out FileName
```

## <a name="arguments"></a>Arguments
 `FileName`

 Požadováno. Cesta a název souboru, který se zobrazí chyby při sestavování spustitelný soubor.

## <a name="remarks"></a>Poznámky
 Pokud je zadán název souboru, který ještě neexistuje, vytvoří se automaticky soubor. Pokud soubor již existuje, výsledky jsou připojena k existující obsah souboru.

 Chyby sestavení příkazového řádku se zobrazí v **příkaz** okno a řešení Tvůrce zobrazení **výstup** okno. Tato možnost je užitečná, pokud běží bezobslužné sestavení a musí zobrazit výsledky.

## <a name="example"></a>Příklad
 Tento příklad spustí `MySolution` a zapíše chyby do souboru `MyErrorLog.txt`.

```cmd
devenv /run "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln" /out "C:\MyErrorLog.txt"
```

## <a name="see-also"></a>Viz také

- [Devenv – přepínače příkazového řádku](../../ide/reference/devenv-command-line-switches.md)
- [Nebo spusťte (devenv.exe)](../../ide/reference/run-devenv-exe.md)
- [/ Sestavení (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ Nasadit (devenv.exe)](../../ide/reference/deploy-devenv-exe.md)