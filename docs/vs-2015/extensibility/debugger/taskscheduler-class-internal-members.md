---
title: Třída TaskScheduler – vnitřní členy | Dokumentace Microsoftu
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
- TaskScheduler class [.NET Framework debug engines]
- debug engines, TaskScheduler class [.NET Framework]
ms.assetid: 87f1c969-0217-4464-8907-7609c1bf61d3
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 80aa2cf0278a9d0ee6197126f6517d40d265b8ca
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42667851"
---
# <a name="taskscheduler-class---internal-members"></a>Třída TaskScheduler – vnitřní členy
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [třída TaskScheduler – vnitřní členy](https://docs.microsoft.com/visualstudio/extensibility/debugger/taskscheduler-class-internal-members).  
  
Toto téma popisuje interní členy <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName> třída, která vám pomůže implementovat vlastní ladicího programu. Obecné informace o této třídy, najdete v článku <xref:System.Threading.Tasks.TaskScheduler> téma referenčních informací.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Sestavení:** mscorlib (v knihovně mscorlib.dll)  
  
 Protože tyto vnitřní členy nemůže získat přístup z rozhraní .NET Framework, je k dispozici v Common Intermediate Language (CIL) následující syntaxi.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
.class public abstract auto ansi beforefieldinit System.Threading.Tasks.TaskScheduler  
       extends System.Object  
```  
  
## <a name="members"></a>Členové  
  
### <a name="methods"></a>Metody  
  
|Název|Popis|  
|----------|-----------------|  
|[Getscheduledtasksfordebugger –](../../extensibility/debugger/getscheduledtasksfordebugger-method.md)|Načte pole všech naplánovaných úloh.|  
|[Gettaskschedulersfordebugger –](../../extensibility/debugger/gettaskschedulersfordebugger-method.md)|Pole všech <xref:System.Threading.Tasks.TaskScheduler> objekty, které jsou momentálně aktivní.|  
  
## <a name="remarks"></a>Poznámky  
  
## <a name="see-also"></a>Viz také  
 <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName>   
 [Interní informace o paralelním rozšíření pro rozhraní .NET Framework](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)

