---
title: Použití knihovny ladění CRT | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- c.debug.runtime
dev_langs:
- FSharp
- VB
- CSharp
- C++
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
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 87b0923153d5e4d0a3c5e4eb33a97e31fd3b2802
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666455"
---
# <a name="crt-debug-library-use"></a>Použití knihovny ladění CRT
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [použití knihovny ladění CRT](https://docs.microsoft.com/visualstudio/debugger/crt-debug-library-use).  
  
Knihovny run-time jazyka C poskytuje rozsáhlou podporu ladění. Chcete-li použít jeden z knihovny ladění CRT, je nutné propojit s [/DEBUG](http://msdn.microsoft.com/library/1af389ae-3f8b-4d76-a087-1cdf861e9103) a proveďte kompilaci s **/MDd**, **/MTD**, nebo **/LDd**.  
  
## <a name="remarks"></a>Poznámky  
 Hlavní definice a makra pro ladění CRT naleznete v hlavičkovém souboru CRTDBG.h.  
  
 Funkce knihovny ladění CRT jsou kompilovány s ladicími informacemi ([/Z7, / Zd, / zi, /ZI (formát informací o ladění)](http://msdn.microsoft.com/library/ce9fa7e1-0c9b-47e3-98ea-26d1a16257c8)) a bez optimalizace. Některé funkce obsahovat výrazy ověřte parametry, které jsou předány na ně a zdrojový kód je k dispozici. Se tento zdrojový kód můžete krokovat s vnořením funkce CRT, funkce fungují podle očekávání a vyhledejte chybné parametry nebo paměti stavů potvrďte. (Některé technologie CRT je proprietární a neposkytuje zdrojový kód pro zpracování výjimek s plovoucí desetinnou čárkou a několik jiných rutin.)  
  
 Když instalujete Visual C++, máte možnost instalace zdrojový kód knihovny run-time jazyka C na pevném disku. Pokud nenainstalujete zdrojový kód, budete potřebovat disk CD-ROM krokovat do funkce CRT.  
  
 Další informace o různých běhových knihoven, které můžete použít, najdete v části [C Run-Time Libraries](http://msdn.microsoft.com/library/a889fd39-807d-48f2-807f-81492612463f).  
  
## <a name="see-also"></a>Viz také  
 [Techniky ladění CRT](../debugger/crt-debugging-techniques.md)   
 [/MD, /MT, /LD (použití knihovny run-time)](http://msdn.microsoft.com/library/cf7ed652-dc3a-49b3-aab9-ad60e5395579)



