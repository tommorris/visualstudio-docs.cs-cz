---
title: Registrace do programu | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- programs, registration
- debugging [Debugging SDK], program registration
ms.assetid: d726a161-7db3-4ef4-b258-9f6a5be68418
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e0b0c883293cd01e21facfcc2e4483d2c5bbf164
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="registering-the-program"></a>Registrace do programu
Po modul ladění získal port, reprezentována [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md) rozhraní, je dalším krokem při povolování program, který chcete ladit a zaregistrujte ho pomocí portu. Po registraci programu je k dispozici pro ladění pomocí jedné z těchto způsobů:  
  
-   Proces připojení, který umožňuje získat ladění kontrolu spuštěné aplikace ladicího programu.  
  
-   V běhu (JIT) ladění, která umožňuje za fakt ladění programu, který spouští nezávisle na ladicí program. Při běhu architektura zachytí chybu, ladicího programu upozornění před operačního systému nebo prostředí runtime uvolní paměť a prostředky chybující programu.  
  
## <a name="registering-procedure"></a>Postup registrace  
  
#### <a name="to-register-your-program"></a>K registraci vašeho programu  
  
1.  Volání [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md) metoda implementované port.  
  
     `IDebugPortNotify2::AddProgramNode`ukazatel na vyžaduje [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md) rozhraní.  
  
     Obvykle když operační systém nebo běhové prostředí načte program, vytvoří uzlu programu. Pokud modul ladění (DE) se zobrazí výzva k načtení program DE vytvoří a zaregistruje uzlu programu.  
  
     Následující příklad ukazuje modul ladění spuštěním programu a její registrací s portem.  
  
    > [!NOTE]
    >  Toto není jediný způsob, jak spustit a pokračovat v procesu; Toto je především Příklad registrace program s portem.  
  
    ```cpp  
    // This is an IDebugEngineLaunch2 method.  
    HRESULT CDebugEngine::LaunchSuspended(/* omitted parameters */,  
                                          IDebugPort2 *pPort,  
                                          /* omitted parameters */,  
                                          IDebugProcess2**ppDebugProcess)  
    {  
        // do stuff here to set up for a launch (such as handling the other parameters)  
        ...  
  
        // Now get the IPortNotify2 interface so we can register a program node  
        // in CDebugEngine::ResumeProcess.  
        CComPtr<IDebugDefaultPort2> spDefaultPort;  
        HRESULT hr = pPort->QueryInterface(&spDefaultPort);  
        if (SUCCEEDED(hr))  
        {  
            CComPtr<IDebugPortNotify2> spPortNotify;  
            hr = spDefaultPort->GetPortNotify(&spPortNotify);  
            if (SUCCEEDED(hr))  
            {  
                // Remember the port notify so we can use it in ResumeProcess.  
                m_spPortNotify = spPortNotify;  
  
                // Now launch the process in a suspended state and return the  
                // IDebugProcess2 interface  
                CComPtr<IDebugPortEx2> spPortEx;  
                hr = pPort->QueryInterface(&spPortEx);  
                if (SUCCEEDED(hr))  
                {  
                    // pass on the parameters we were given (omitted here)  
                    hr = spPortEx->LaunchSuspended(/* omitted paramters */,ppDebugProcess)  
                }  
            }  
        }  
        return(hr);  
    }  
  
    HRESULT CDebugEngine::ResumeProcess(IDebugProcess2 *pDebugProcess)  
    {  
        // Make a program node for this process  
        HRESULT hr;  
        CComPtr<IDebugProgramNode2> spProgramNode;  
        hr = this->GetProgramNodeForProcess(pProcess, &spProgramNode);  
        if (SUCCEEDED(hr))  
        {  
            hr = m_spPortNotify->AddProgramNode(spProgramNode);  
            if (SUCCEEDED(hr))  
            {  
                // resume execution of the process using the port given to us earlier.  
               // (Querying for the IDebugPortEx2 interface is valid here since  
               // that's how we got the IDebugPortNotify2 interface in the first place.)  
                CComPtr<IDebugPortEx2> spPortEx;  
                hr = m_spPortNotify->QueryInterface(&spPortEx);  
                if (SUCCEEDED(hr))  
                {  
                    hr  = spPortEx->ResumeProcess(pDebugProcess);  
                }  
            }  
        }  
        return(hr);  
    }  
  
    ```  
  
## <a name="see-also"></a>Viz také  
 [Získávání Port](../../extensibility/debugger/getting-a-port.md)   
 [Povolení Program chcete ladit](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)