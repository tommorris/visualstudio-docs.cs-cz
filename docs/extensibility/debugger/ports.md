---
title: Porty | Dokumentace Microsoftu
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- ports
- debugging [Debugging SDK], ports
ms.assetid: 1d7f3aa7-7eff-4cab-bc53-0a566b1a9363
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d6a73aef5151b12360d1e227d440223df4ff3298
ms.sourcegitcommit: 71b307ce86c4079cc7ad686d8d5f96a6a123aadd
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/25/2018
ms.locfileid: "39251046"
---
# <a name="ports"></a>Porty
V architektuře ladicího programu *port*:  
  
-   Je kontejner pro sadu procesy běží na serveru. Port může například představovat připojení k zařízení sériový kabel systémem Windows CE nebo k počítači připojenému bez – model DCOM. Jeden speciální port, volá se na místní port, obsahuje všechny procesy spuštěné na místním počítači.  
  
-   Můžete identifikovat podle názvu nebo identifikátor.  
  
-   Můžete vytvořit výčet všech procesů spuštěných na portu a spuštění a ukončení tyto procesy.  
  
-   Je reprezentován [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md) rozhraní, která je vytvořena předáním [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md) argument [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md).  
  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] poskytuje výchozí port, který zpracovává všechny založené na Windows procesy, nativní a spravované. Port. Tento vlastní port musí být nastaveny pro připojení se externí zařízení, které nejsou založené na Windows. Slouží k poskytování těchto vlastní porty, musíte také nastavit vlastní port dodavatele.  
  
## <a name="see-also"></a>Viz také:  
 [Servery](../../extensibility/debugger/servers-visual-studio-sdk.md)   
 [Procesy](../../extensibility/debugger/processes.md)   
 [Koncepty ladicího programu](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md)   
 [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md)   
 [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md)