---
title: 'Chyba: Microsoft Visual Studio Remote Debugging Monitor na vzdáleném počítači nemá oprávnění k připojení k tomuto počítači | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.error.access_denied_oncallback
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, Windows version error
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 266a301bca4953066621d759518c1754052dfeb2
ms.sourcegitcommit: eefffa7ebe339d1297cdc12f51a813e7849d7e95
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2018
ms.locfileid: "34177966"
---
# <a name="error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-does-not-have-permission-to-connect-to-this-computer"></a>Chyba: Microsoft Visual Studio Remote Debugging Monitor na vzdáleném počítači nemá oprávnění pro připojení k tomuto počítači.
K této chybě dojde, když uživatel, který se pokouší spustit Visual Studio Remote Debugging Monitor (msvsmon) nemá účet místního počítače.  
  
### <a name="to-fix-this-problem"></a>Chcete-li vyřešit tento problém  
  
-   Uživatelský účet přidat do počítače hostitele ladicího programu sady Visual Studio, s stejné jméno a heslo jako uživatelský účet spouštějící msvsmon ve vzdáleném počítači  
  
     \- nebo –  
  
-   Spusťte msvsmon jako uživatel, který má oprávnění k volání do místního počítače. To znamená, že uživatel musí být uživatel domény a správce v počítači msvsmon. Můžete určit uživatelský účet pro spouštění msvsmon v jednom ze dvou způsobů:  
  
    -   Klikněte pravým tlačítkem na ikonu msvsmon a zvolte **spustit jako** v místní nabídce  
  
     \- nebo –  
  
    -   Na příkazovém řádku spusťte `runas.exe`.  
  
## <a name="see-also"></a>Viz také  
 [Vzdálené ladění chyby a řešení potíží](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Vzdálené ladění](../debugger/remote-debugging.md)