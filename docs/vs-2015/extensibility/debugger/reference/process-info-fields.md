---
title: PROCESS_INFO_FIELDS | Dokumentace Microsoftu
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
- PROCESS_INFO_FIELDS
helpviewer_keywords:
- PROCESS_INFO_FIELDS enumeration
ms.assetid: 0d9cc345-3d3a-44d8-ae15-a67acb97a828
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8b272fba2e05c25e60b2db1f11be16b97d261101
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672702"
---
# <a name="processinfofields"></a>PROCESS_INFO_FIELDS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [PROCESS_INFO_FIELDS](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/process-info-fields).  
  
Zadaný druh informací k načtení procesu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
enum enum_PROCESS_INFO_FIELDS {   
   PIF_FILE_NAME             = 0x00000001,  
   PIF_BASE_NAME             = 0x00000002,  
   PIF_TITLE                 = 0x00000004,  
   PIF_PROCESS_ID            = 0x00000008,  
   PIF_SESSION_ID            = 0x00000010,  
   PIF_ATTACHED_SESSION_NAME = 0x00000020,  
   PIF_CREATION_TIME         = 0x00000040,  
   PIF_FLAGS                 = 0x00000080,  
   PIF_ALL                   = 0x000000ff  
};  
typedef DWORD PROCESS_INFO_FIELDS;  
```  
  
```csharp  
public enum enum_PROCESS_INFO_FIELDS {   
   PIF_FILE_NAME             = 0x00000001,  
   PIF_BASE_NAME             = 0x00000002,  
   PIF_TITLE                 = 0x00000004,  
   PIF_PROCESS_ID            = 0x00000008,  
   PIF_SESSION_ID            = 0x00000010,  
   PIF_ATTACHED_SESSION_NAME = 0x00000020,  
   PIF_CREATION_TIME         = 0x00000040,  
   PIF_FLAGS                 = 0x00000080,  
   PIF_ALL                   = 0x000000ff  
};  
```  
  
## <a name="members"></a>Členové  
 PIF_FILE_NAME  
 Inicializace/použít `bstrFileName` pole [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) struktury.  
  
 PIF_BASE_NAME  
 Inicializace/použít `bstrBaseName` pole `PROCESS_INFO` struktury.  
  
 PIF_TITLE  
 Inicializace/použít `bstrTitle` pole `PROCESS_INFO` struktury.  
  
 PIF_PROCESS_ID  
 Inicializace/použít `ProcessId` pole `PROCESS_INFO` struktury.  
  
 PIF_SESSION_ID  
 Inicializace/použít `dwSessionId` pole `PROCESS_INFO` struktury.  
  
 PIF_ATTACHED_SESSION_NAME  
 Inicializace/použít `bstrAttachedSessionName` pole `PROCESS_INFO` struktury.  
  
 PIF_CREATION_TIME  
 Inicializace/použít `CreationTime` pole `PROCESS_INFO` struktury.  
  
 PIF_FLAGS  
 Inicializace/použít `Flags` pole `PROCESS_INFO` struktury.  
  
 PIF_ALL  
 Vyplní všechna pole.  
  
## <a name="remarks"></a>Poznámky  
 Předány [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) indikace polí s [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) struktury mají být inicializovány.  
  
 Používá se také v `Fields` pole `PROCESS_INFO` struktury k označení pole, která se používá a je platný.  
  
 Tyto příznaky lze kombinovat pomocí logické bitové `OR`.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)

