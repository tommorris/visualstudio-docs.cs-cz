---
title: Porty | Dokumentace Microsoftu
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
- ports
- debugging [Debugging SDK], ports
ms.assetid: 1d7f3aa7-7eff-4cab-bc53-0a566b1a9363
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: dbc8778af1cbc82b4f9e7f577a95123a1c1f5843
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675508"
---
# <a name="ports"></a>Porty
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [porty](https://docs.microsoft.com/visualstudio/extensibility/debugger/ports).  
  
Z hlediska architektury ladicího programu **port**:  
  
-   Je kontejner pro sadu procesy běží na serveru. Port může například představovat připojení k zařízení sériový kabel systémem Windows CE nebo k počítači připojenému bez – model DCOM. Jeden speciální port, volá se na místní port, obsahuje všechny procesy spuštěné na místním počítači.  
  
-   Můžete identifikovat podle názvu nebo identifikátor.  
  
-   Můžete vytvořit výčet všech procesů spuštěných na portu a spuštění a ukončení tyto procesy.  
  
-   Je reprezentován [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md) rozhraní, která je vytvořena předáním [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md) argument [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md).  
  
 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] poskytuje výchozí port, který zpracovává všechny založené na Windows procesy, nativní a spravované. Port. Tento vlastní port musí být implementované připojení se externí zařízení, které nejsou založené na Windows. Slouží k poskytování těchto vlastní porty, dodavatel port. Tento vlastní port musí také být implementována.  
  
## <a name="see-also"></a>Viz také  
 [Servery](../../extensibility/debugger/servers-visual-studio-sdk.md)   
 [Procesy](../../extensibility/debugger/processes.md)   
 [Koncepty ladicího programu](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md)   
 [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md)   
 [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md)

