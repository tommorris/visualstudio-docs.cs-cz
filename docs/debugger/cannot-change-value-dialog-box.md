---
title: "Nelze změnit hodnotu – dialogové | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.variables.failededit
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Cannot Change Value dialog box
- variables [debugger], editing
ms.assetid: 19e930c2-5fbf-4c83-aae8-a1dc3f8fcae8
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b05c461d71f1fc1526114e8ae41ecf7f04d63885
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="cannot-change-value-dialog-box"></a>Dialogové okno Nelze změnit hodnotu
## <a name="error"></a>Chyba  
 `The value of this variable cannot be changed`&#124; `The name` *název* `does not exist in the current context` &#124; *různé další zprávy*  
  
 Při pokusu o změnu obsahu proměnné na neplatnou hodnotu v okně ladicí program (automobily, sledovat nebo místní hodnoty – windows) nebo v dialogovém okně QuickWatch, zobrazí se toto okno se zprávou. Například pokud se pokusíte nastavit hodnotu na celé číslo proměnnou na řetězec znaků, zobrazí se toto okno se zprávou.  
  
## <a name="solution"></a>Řešení  
 Zajistěte, aby vstupní zadáte do okna ladicího programu nebo QuickWatch – dialogové představuje platnou hodnotu pro proměnnou, kterou se pokoušíte nastavit.  
  
## <a name="see-also"></a>Viz také  
 [Výrazy v ladicím programu](../debugger/expressions-in-the-debugger.md)