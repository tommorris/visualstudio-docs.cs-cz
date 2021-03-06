---
title: MODULE_INFO | Dokumentace Microsoftu
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
- MODULE_INFO
helpviewer_keywords:
- MODULE_INFO structure
ms.assetid: f2e06180-1ab3-4eb5-a428-7994cceb61b6
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 95972779db412ad87883fbb3ba5d4fbbc1ee1cc1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672908"
---
# <a name="moduleinfo"></a>MODULE_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [MODULE_INFO](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/module-info).  
  
Popisuje konkrétního modulu (knihovny DLL, EXE nebo sestavení).  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
typedef struct tagMODULE_INFO {   
   MODULE_INFO_FIELDS dwValidFields;  
   BSTR               m_bstrName;  
   BSTR               m_bstrUrl;  
   BSTR               m_bstrVersion;  
   BSTR               m_bstrDebugMessage;  
   UINT64             m_addrLoadAddress;  
   UINT64             m_addrPreferredLoadAddress;  
   DWORD              m_dwSize;  
   DWORD              m_dwLoadOrder;  
   FILETIME           m_TimeStamp;  
   BSTR               m_bstrUrlSymbolLocation;  
   MODULE_FLAGS       m_dwModuleFlags;  
} MODULE_INFO;  
```  
  
```csharp  
public struct MODULE_INFO {   
   public uint     dwValidFields;  
   public string   m_bstrName;  
   public string   m_bstrUrl;  
   public string   m_bstrVersion;  
   public string   m_bstrDebugMessage;  
   public ulong    m_addrLoadAddress;  
   public ulong    m_addrPreferredLoadAddress;  
   public uint     m_dwSize;  
   public uint     m_dwLoadOrder;  
   public FILETIME m_TimeStamp;  
   public string   m_bstrUrlSymbolLocation;  
   public uint     m_dwModuleFlags;  
};  
```  
  
## <a name="members"></a>Členové  
 dwValidFields  
 Kombinace příznaků z [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md) výčet, který určuje, která pole jsou vyplněna.  
  
 m_bstrName  
 Název modulu.  
  
 m_bstrUrl  
 Adresa URL modulu.  
  
 m_bstrVersion  
 Verze modulu.  
  
 m_bstrDebugMessage  
 Volitelnou zprávu o modulu, třeba "symboly nelze načíst."  
  
 m_addrLoadAddress  
 Adresa načtení modulu.  
  
 m_addrPreferredLoadAddress  
 Adresa upřednostňovaného zatížení modulu.  
  
 m_dwSize  
 Velikost modulu.  
  
 m_dwLoadOrder  
 Pořadí načítání modulu.  
  
 m_TimeStamp  
 Čas poslední změny souboru symbolů.  
  
 m_bstrUrlSymbolLocation  
 Umístění souboru symbolů (například ".\\") zadaný v modulu. Najít symboly pro modul se používá jako výchozí umístění.  
  
 m_dwModuleFlags  
 Kombinace příznaků z [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md) výčet, který popisuje modulu.  
  
## <a name="remarks"></a>Poznámky  
 Tato struktura je předán [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md) metody, kde je vyplněna.  
  
 Tato struktura odpovídá jednotlivých modulů uvedených v **moduly** okna.  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Viz také  
 [Struktury a sjednocení](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md)   
 [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)

