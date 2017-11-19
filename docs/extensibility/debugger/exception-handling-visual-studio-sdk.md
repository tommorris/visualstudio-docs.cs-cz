---
title: "Výjimka zpracování (Visual Studio SDK) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: debugging [Debugging SDK], exception handling
ms.assetid: 7279dc16-db14-482c-86b8-7b3da5a581d2
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4a0d950de8e9f91232e3526064561a7508c133b4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="exception-handling-visual-studio-sdk"></a>(Visual Studio SDK) zpracování výjimek
Následující část popisuje proces, který nastane, když nastanou výjimky.  
  
## <a name="exception-handling-process"></a>Proces zpracování výjimek  
  
1.  Pokud je vyvolána výjimka, nejprve, ale předtím, než je zpracována obslužná rutina výjimky v programu laděné, modul ladění (DE) odešle [IDebugExceptionEvent2](../../extensibility/debugger/reference/idebugexceptionevent2.md) pro relaci ladění správce (SDM) jako událost zastavit. `IDebugExceptionEvent2` Se odesílají-li jen nastavení pro výjimky (zadané v dialogovém okně výjimky v balíčku ladění) určují, že uživatel chce zastavit v první odpovídající výjimce oznámení.  
  
2.  Volání SDM [IDebugExceptionEvent2::GetException](../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) GET pro vlastnost výjimky.  
  
3.  Volání balíček ladění [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) určit, jaké možnosti k dispozici pro uživatele.  
  
4.  Balíček ladění požádá uživatele, jak zpracovat výjimku otevřením dialogového okna první odpovídající výjimce.  
  
5.  Pokud uživatel vybere možnost pokračovat, zavolá SDM [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md).  
  
    -   Pokud metoda vrátí S_OK, zavolá [IDebugExceptionEvent2::PassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-passtodebuggee.md).  
  
         -nebo-  
  
         Pokud metoda vrátí S_FALSE, program laděné dostane druhou možnost ošetření výjimky.  
  
6.  Má-li program laděné žádná obslužná rutina pro sekundu odpovídající výjimce, DE odešle `IDebugExceptionEvent2` k SDM jako **EVENT_SYNC_STOP**.  
  
7.  Balíček ladění požádá uživatele, jak zpracovat výjimku otevřením dialogového okna první odpovídající výjimce.  
  
8.  Volání balíček ladění [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) určit, jaké možnosti k dispozici pro uživatele.  
  
9. Balíček ladění požádá uživatele, jak zpracovat výjimku otevřením dialogového okna sekundu odpovídající výjimce.  
  
10. Pokud metoda vrátí S_OK, zavolá `IDebugExceptionEvent2::PassToDebuggee`.  
  
## <a name="see-also"></a>Viz také  
 [Události volání ladicí program](../../extensibility/debugger/calling-debugger-events.md)