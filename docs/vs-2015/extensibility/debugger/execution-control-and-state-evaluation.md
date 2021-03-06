---
title: Řízení provádění a vyhodnocení stavu | Dokumentace Microsoftu
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
- debugging [Debugging SDK], execution control
- expression evaluation, control of execution
ms.assetid: 55adde38-1622-4b51-83cb-ce1b04c1ca7a
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 72b13fece6129c6b3996363bb0ec082330c9b686
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669539"
---
# <a name="execution-control-and-state-evaluation"></a>Řízení provádění a vyhodnocení stavu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [řízení provádění a vyhodnocení stavu](https://docs.microsoft.com/visualstudio/extensibility/debugger/execution-control-and-state-evaluation).  
  
Ladění aplikace vyžaduje implementaci funkce řízení provádění, jako krokování do funkce, zastavování na zarážkách a pokračování v provádění. Ladění základních tříd sady Visual Studio jeho řízení provádění na události se posílají mezi komponenty ladicího programu.  
  
## <a name="in-this-section"></a>V tomto oddílu  
 [Řízení programu](../../extensibility/debugger/program-control.md)  
 Obsahuje tyto rutiny, ke kterým dochází na úrovni programu: nastavení dalšího příkazu, provádění, krokování, budete pokračovat, pozastavení a obnovení.  
  
 [Metody související se zarážkou](../../extensibility/debugger/breakpoint-related-methods.md)  
 Definuje je mez a čeká se na typy zarážek, které podporuje Visual Studio.  
  
 [Vyhodnocení zásobníku volání](../../extensibility/debugger/call-stack-evaluation.md)  
 Tento článek popisuje implementaci metody, které umožňují zobrazení rámců zásobníku volání během režimu pozastavení.  
  
 [Vyhodnocení výrazu](../../extensibility/debugger/expression-evaluation-visual-studio-debugging-sdk.md)  
 Vysvětluje, jak ladicího stroje (DE) Správce výraz vyhodnocení (EE) a relace ladění se podílejí analýze a hodnocení výrazu zadali do jedné ze systému windows z integrovaného vývojového prostředí.  
  
 [Události ovládacích prvků](../../extensibility/debugger/control-events.md)  
 Tento článek popisuje rozhraní použité k odesílání událostí během řízené provádění programu.

