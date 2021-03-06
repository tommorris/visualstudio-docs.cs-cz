---
title: Enumerátor kódu stavu souboru | Dokumentace Microsoftu
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
- named constants, SccStatus enumerator
- source control plug-ins, file status enumeration
- SccStatus enumerator
- file status code enumerator
ms.assetid: 5c37876b-c83c-4ca1-837b-57cd465a879a
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e41a0181c22f8b760156ec41e1e450aa0f3cf740
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674047"
---
# <a name="file-status-code-enumerator"></a>Enumerátor kódu stavu souboru
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [enumerátor kódu stavu souboru](https://docs.microsoft.com/visualstudio/extensibility/file-status-code-enumerator).  
  
`SccStatus` Obsahuje čítače výčtu s názvem konstantní hodnoty, které určují stav souboru v systému správy zdrojového kódu. Tento výčet je používán [sccqueryinfo –](../extensibility/sccqueryinfo-function.md) a `POPLISTFUNC` funkce zpětného volání (viz [POPLISTFUNC](../extensibility/poplistfunc.md) podrobnosti).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
enum SccStatus {  
   SCC_STATUS_INVALID          = -1L,  
   SCC_STATUS_NOTCONTROLLED    = 0x0000L,  
   SCC_STATUS_CONTROLLED       = 0x0001L,  
   SCC_STATUS_CHECKEDOUT       = 0x0002L,  
   SCC_STATUS_OUTOTHER         = 0x0004L,  
   SCC_STATUS_OUTEXCLUSIVE     = 0x0008L,  
   SCC_STATUS_OUTMULTIPLE      = 0x0010L,  
   SCC_STATUS_OUTOFDATE        = 0x0020L,  
   SCC_STATUS_DELETED          = 0x0040L,  
   SCC_STATUS_LOCKED           = 0x0080L,  
   SCC_STATUS_MERGED           = 0x0100L,  
   SCC_STATUS_SHARED           = 0x0200L,  
   SCC_STATUS_PINNED           = 0x0400L,  
   SCC_STATUS_MODIFIED         = 0x0800L,  
   SCC_STATUS_OUTBYUSER        = 0x1000L  
   SCC_STATUS_NOMERGE          = 0x2000L  
   SCC_STATUS_RESERVED_1       = 0x4000L  
   SCC_STATUS_RESERVED_2       = 0x8000L  
};  
```  
  
## <a name="members"></a>Členové  
 SCC_STATUS_INVALID  
 Nebylo možné získat stav; Nespoléhejte na to.  
  
 SCC_STATUS_NOTCONTROLLED  
 Soubor není pod správou zdrojových kódů.  
  
 SCC_STATUS_CONTROLLED  
 Soubor je pod správou zdrojových kódů.  
  
 SCC_STATUS_CHECKEDOUT  
 Rezervována aktuálního uživatele na místním disku.  
  
 SCC_STATUS_OUTOTHER  
 Soubor je rezervována jiným uživatelem.  
  
 SCC_STATUS_OUTEXCLUSIVE  
 Soubor je exkluzivně zaregistrován.  
  
 SCC_STATUS_OUTMULTIPLE  
 Soubor je rezervována více než jeden uživatel.  
  
 SCC_STATUS_OUTOFDATE  
 Soubor není nejnovější.  
  
 SCC_STATUS_DELETED  
 Soubor byl odstraněn z projektu.  
  
 SCC_STATUS_LOCKED  
 Soubor je uzamčen; žádné další verze povolené.  
  
 SCC_STATUS_MERGED  
 Souboru byla sloučit, ale dosud opraveno/ověření.  
  
 SCC_STATUS_SHARED  
 Soubor je sdílen mezi projekty.  
  
 SCC_STATUS_PINNED  
 Sdílení souboru na explicitní verzi.  
  
 SCC_STATUS_MODIFIED  
 Soubor byl změněn nebo nefunkční/došlo k porušení.  
  
 SCC_STATUS_OUTBYUSER  
 Soubor je rezervována aktuálního uživatele.  
  
 SCC_STATUS_NOMERGE  
 Soubor může být nikdy sloučeny s a před GET nemusí být uložen.  
  
 SCC_STATUS_RESERVED_1  
 Vyhrazeno pro interní použití.  
  
 SCC_STATUS_RESERVED_2  
 Vyhrazeno pro interní použití.  
  
## <a name="see-also"></a>Viz také  
 [Ovládací prvek moduly plug-in zdrojového kódu](../extensibility/source-control-plug-ins.md)   
 [Sccqueryinfo –](../extensibility/sccqueryinfo-function.md)   
 [POPLISTFUNC](../extensibility/poplistfunc.md)

