---
title: 'Chyba: Microsoft Visual Studio Remote Debugging Monitor na vzdáleném počítači nemá oprávnění k připojení k tomuto počítači. | Dokumentace Microsoftu'
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
- vs.debug.error.access_denied_oncallback
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- remote debugging, Windows version error
ms.assetid: ba08a59b-6dbc-4bbc-9c52-379d3bf5241f
caps.latest.revision: 24
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1a62f20afc5ba57da64205491a3c5dfeabd75daf
ms.sourcegitcommit: d705e015cb525bfa87a0b93e93376c3956ec2707
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/29/2018
ms.locfileid: "43231115"
---
# <a name="error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-does-not-have-permission-to-connect-to-this-computer"></a>Chyba: Microsoft Visual Studio Remote Debugging Monitor na vzdáleném počítači nemá oprávnění pro připojení k tomuto počítači.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [Chyba: Microsoft Visual Studio Remote Debugging Monitor na vzdáleném počítači nemá oprávnění k připojení k tomuto počítači](https://docs.microsoft.com/visualstudio/debugger/error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-does-not-have-permission-to-connect-to-this-computer).  
  
K této chybě dochází, když uživatel, který se pokouší spustit Visual Studio Remote Debugging Monitor (msvsmon) nemá účet na místním počítači.  
  
### <a name="to-fix-this-problem"></a>Chcete-li vyřešit tento problém  
  
-   Přidat uživatelský účet k počítači hostitele ladicího programu sady Visual Studio, pomocí stejné jméno a heslo uživatelského účtu na vzdáleném počítači spuštěny msvsmon.  
  
     \- nebo –  
  
-   Spuštění msvsmon jako uživatel, který má oprávnění k volání do místního počítače. To znamená, že uživatel musí být uživatelem domény a správce v počítači msvsmon. Můžete zadat uživatelský účet pro spuštění msvsmon v jednom ze dvou způsobů:  
  
    -   Klikněte pravým tlačítkem na ikonu msvsmon a zvolte **spustit jako** v místní nabídce  
  
     \- nebo –  
  
    -   Na příkazovém řádku spusťte `runas.exe`.  
  
## <a name="see-also"></a>Viz také  
 [Vzdálené ladění napříč doménami](http://msdn.microsoft.com/library/8e697ce1-55e8-4ab0-a05f-f87225e2f29b)   
 [Vzdálené ladění chyby a řešení potíží](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Vzdálené ladění](../debugger/remote-debugging.md)



