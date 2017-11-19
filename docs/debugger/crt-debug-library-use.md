---
title: "Použití knihovny ladění CRT | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: c.debug.runtime
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- /DEBUG linker option [C++]
- crtdbg.h file
- debug library
- MDd compiler option [C++]
- libraries, CRT debug library
- MTd compiler option [C++]
- LDd compiler function [C++]
- /MTd compiler option [C++]
- /MDd compiler option [C++]
- debugging [CRT], CRT debug library
- DEBUG linker option [C++]
- /LDd compiler function [C++]
ms.assetid: 464de16b-4215-4787-9bfa-921aaff9d9f4
caps.latest.revision: "16"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a2774eacfb0472145edb84d5c3becf77513ee986
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="crt-debug-library-use"></a>Použití knihovny ladění CRT
Běhové knihovny jazyka C poskytuje rozsáhlou podporu ladění. Pokud chcete používat jeden z knihovny ladění CRT, je nutné propojit s [/DEBUG](/cpp/build/reference/debug-generate-debug-info) a kompilaci s **/MDd**, **/MTd**, nebo **/LDd**.  
  
## <a name="remarks"></a>Poznámky  
 Hlavní definice a makra pro ladění CRT naleznete v crtdbg.h – soubor hlaviček.  
  
 Funkce knihovny ladění CRT jsou kompilovat s ladicími informacemi ([/Z7, /Zd, / zi, /ZI (formát informace ladění)](/cpp/build/reference/z7-zi-zi-debug-information-format)) a bez optimalizace. Kontrolní výrazy ověření parametry, které se předávají do nich obsahovat některé funkce a zdrojový kód je k dispozici. S tímto kódem zdroj může krok do funkcí CRT potvrďte, že funkce fungují jako očekávat a kontrolovat chybné parametry nebo paměti stavy. (Některé technologie, CRT je proprietární a neposkytuje zdrojový kód pro zpracování výjimek plovoucí desetinné čárky a několik dalších rutiny.)  
  
 Když instalujete Visual C++, máte možnost instalace zdrojový kód běhové knihovny jazyka C na pevném disku. Pokud nenainstalujete zdrojový kód, budete potřebovat pro krok do funkcí CRT disku CD-ROM.  
  
 Další informace o různých běhové knihovny můžete použít, najdete v části [běhové knihovny jazyka C](/cpp/c-runtime-library/crt-library-features).  
  
## <a name="see-also"></a>Viz také  
 [Techniky ladění CRT](../debugger/crt-debugging-techniques.md)   
 [/ MD, / MT, /LD (použít běhovou knihovnu)](/cpp/build/reference/md-mt-ld-use-run-time-library)