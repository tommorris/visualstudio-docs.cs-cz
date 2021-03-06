---
title: IDebugPortEx2::LaunchSuspended | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugPortEx2::LaunchSuspended
helpviewer_keywords:
- IDebugPortEx2::LaunchSuspended
ms.assetid: 34b2cf99-2e52-4757-8969-1d12ac517ec0
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2ee2a93f10aa912ba1619342d814817c8abd5307
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672595"
---
# <a name="idebugportex2launchsuspended"></a>IDebugPortEx2::LaunchSuspended
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugPortEx2::LaunchSuspended](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugportex2-launchsuspended).  
  
Spustí spustitelný soubor.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT LaunchSuspended(   
   LPCOLESTR        pszExe,  
   LPCOLESTR        pszArgs,  
   LPCOLESTR        pszDir,  
   BSTR             bstrEnv,  
   DWORD            hStdInput,  
   DWORD            hStdOutput,  
   DWORD            hStdError,  
   IDebugProcess2** ppPortProcess  
);  
```  
  
```csharp  
int LaunchSuspended(   
   string             pszExe,  
   string             pszArgs,  
   string             pszDir,  
   string             bstrEnv,  
   uint               hStdInput,  
   uint               hStdOutput,  
   uint               hStdError,  
   out IDebugProcess2 ppPortProcess  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pszExe`  
 [in] Název spustitelného souboru, která se má spustit. To může být úplná cesta nebo relativní vzhledem k zadaný v pracovní adresář `pszDir` parametru.  
  
 `pszArgs`  
 [in] Argumenty k předání do spustitelného souboru. Může mít hodnotu null, pokud nejsou žádné argumenty.  
  
 `pszDir`  
 [in] Název pracovní adresář, který používá spustitelný soubor. Může mít hodnotu null, pokud je potřeba žádné pracovní adresář.  
  
 `bstrEnv`  
 [in] Blok prostředí řetězec zakončený null, za nímž následuje další ukončovací znak NULL.  
  
 `hStdInput`  
 [in] Popisovač alternativní vstupní datový proud. Může být 0, pokud se nevyžaduje přesměrování.  
  
 `hStdOutput`  
 [in] Popisovač alternativní výstupní datový proud. Může být 0, pokud se nevyžaduje přesměrování.  
  
 `hStdError`  
 [in] Zpracování do výstupního datového proudu alternativní chyby. Může být 0, pokud se nevyžaduje přesměrování.  
  
 `ppPortProcess`  
 [out] Vrátí [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) objekt, který reprezentuje spuštěn proces.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda by měla spustit proces tak, že je pozastavený a neběží žádný kód. [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md) metoda je volána, aby se proces obnovil.  
  
 Program můžete také spustit z ladicího stroje. Podrobnosti najdete v tématu [spuštění programu](../../../extensibility/debugger/launching-a-program.md).  
  
## <a name="see-also"></a>Viz také  
 [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)   
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)   
 [Spuštění programu](../../../extensibility/debugger/launching-a-program.md)

