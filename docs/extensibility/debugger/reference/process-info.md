---
title: PROCESS_INFO | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- PROCESS_INFO
helpviewer_keywords:
- PROCESS_INFO structure
ms.assetid: 260c33cc-a05e-4645-84b6-536d0b3b0537
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d35b94b6153b65672453ed8b4e7d2c0d9c2bd5eb
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31134380"
---
# <a name="processinfo"></a>PROCESS_INFO
Obsahuje informace o procesu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
typedef struct tagPROCESS_INFO {   
   PROCESS_INFO_FIELDS Fields;  
   BSTR                bstrFileName;  
   BSTR                bstrBaseName;  
   BSTR                bstrTitle;  
   AD_PROCESS_ID       ProcessId;  
   DWORD               dwSessionId;  
   BSTR                bstrAttachedSessionName;  
   FILETIME            CreationTime;  
   PROCESS_INFO_FLAGS  Flags;  
} PROCESS_INFO;  
```  
  
```csharp  
public struct PROCESS_INFO {   
   public uint          Fields;  
   public string        bstrFileName;  
   public string        bstrBaseName;  
   public string        bstrTitle;  
   public AD_PROCESS_ID ProcessId;  
   public uint          dwSessionId;  
   public string        bstrAttachedSessionName;  
   public FILETIME      CreationTime;  
   public uint          Flags;  
};  
```  
  
## <a name="members"></a>Členové  
 Pole  
 Kombinace příznaků z [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md) výčet, který zadejte pole, která jsou vyplněna.  
  
 bstrFileName  
 Úplná cesta a název procesu. Odpovídá volání [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md) metoda s parametrem `GN_FILENAME`.  
  
 bstrBaseName  
 Název souboru a rozšíření procesu. Odpovídá volání `IDebugProcess2::Getname` metoda s parametrem `GN_BASENAME`.  
  
 bstrTitle  
 Název procesu, pokud existuje. Odpovídá volání `IDebugProcess2::Getname` metoda s parametrem `GN_TITLE`.  
  
 ID procesu  
 [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) struktura, která identifikuje proces. Odpovídá volání [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md) metoda.  
  
 dwSessionId  
 Identifikátor relace ladění, který tento proces běží v.  
  
 bstrAttachedSessionName  
 Název připojené relace. Odpovídá volání [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md) metoda.  
  
 Čas vytvoření  
 Čas vytvoření procesu.  
  
 Příznaky  
 Kombinace příznaků z [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md) výčet, který zadat vlastnosti procesu.  
  
## <a name="remarks"></a>Poznámky  
 Tato struktura je předána [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) metoda, kde je vyplněna.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Struktury a sjednocení](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md)   
 [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md)   
 [GetName –](../../../extensibility/debugger/reference/idebugprocess2-getname.md)   
 [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)   
 [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md)