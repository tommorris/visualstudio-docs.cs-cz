---
title: VsgDbg::VsgDbg (konstruktor) | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 670651e6-5e79-4845-b0c2-671beb7055a8
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f2a35443dbf4fc413908c61e989d2138122c0991
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42696243"
---
# <a name="vsgdbgvsgdbg-constructor"></a>VsgDbg::VsgDbg (konstruktor)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [VsgDbg::VsgDbg (konstruktor)](https://docs.microsoft.com/visualstudio/debugger/graphics/vsgdbg-vsgdbg-constructor).  
  
Vytvoří instanci objektu `VsgDbg` třídy s nebo bez přípravy komponentu v aplikaci diagnostiky grafiky k aktivně zachycení a zaznamenání grafických informací ve výchozím nastavení, založené na zadaný parametr logické hodnoty.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
VsgDbg(  
  bDefaultInit  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `bDefaultInit`  
 `true` Chcete-li určit, že má být připraveni aktivně zachycení a zaznamenání informací grafiky; součást diagnostiky grafiky v aplikaci `false` k určení, že aplikace by neměly být připravovány aktivně zachytit a zaznamenání grafických informací v tuto chvíli.  
  
## <a name="remarks"></a>Poznámky  
 Pokud je konstruktor volán s `bDefaultInit` nastavena na `true`, soubor název souboru protokolu grafiky je určen jak `DONT_SAVE_VSGLOG_TO_TEMP` a `VSG_DEFAULT_RUN_FILENAME` symboly preprocesoru jsou definovány před `vsgcapture.h` je součástí vaší aplikace.  
  
 Pokud je konstruktor volán s `bDefaultInit` nastavena na `false`, součást diagnostiky grafiky v aplikaci může být připraveni aktivně zachycení a zaznamenání informací grafiky později pomocí volání `Init` funkce.  
  
## <a name="see-also"></a>Viz také  
 [VsgDbg:: ~ VsgDbg (destruktor)](../debugger/vsgdbg-tilde-vsgdbg-destructor.md)   
 [Inicializace](../debugger/init.md)   
 [DONT_SAVE_VSGLOG_TO_TEMP](../debugger/dont-save-vsglog-to-temp.md)   
 [VSG_DEFAULT_RUN_FILENAME](../debugger/vsg-default-run-filename.md)



