---
title: Připojení přímo k programu | Dokumentace Microsoftu
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
- debug engines, attaching to programs
ms.assetid: ad2b7db8-821c-440c-ba07-c55c6a395e0f
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ab866d46e99c6cdee8300bc194468b115ab59e51
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42667478"
---
# <a name="attaching-directly-to-a-program"></a>Připojení přímo k programu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [připojení přímo k programu](https://docs.microsoft.com/visualstudio/extensibility/debugger/attaching-directly-to-a-program).  
  
Uživatelé, kteří chtějí ladit programy v procesu, který je již spuštěna obvykle postupujte takto:  
  
1.  V integrovaném vývojovém prostředí, zvolte **ladit procesy** příkaz **nástroje** nabídky.  
  
     **Procesy** zobrazí se dialogové okno.  
  
2.  Vybrat proces a klikněte na tlačítko **připojit** tlačítko.  
  
     **Připojit k procesu** zobrazí se dialogové okno se seznamem všech ladicí stroj (DEs) na počítači nainstalovaný.  
  
3.  Zadejte DEs používat k ladění procesu vybrané a potom klikněte na **OK**.  
  
 Ladit balíček spustí relaci ladění a předá seznam šifrování DEs. Relace ladění pak předá tento seznam, spolu s funkce zpětného volání, na vybraný proces a následně požádá procesu výčet jeho spuštěné programy.  
  
 V reakci na žádost uživatele prostřednictvím kódu programu, ladit balíček správce ladění relace (SDM) vytvoří instanci a předá seznam vybraných DEs. Společně se seznamem, předá ladit balíček SDM [IDebugEventCallback2](../../extensibility/debugger/reference/idebugeventcallback2.md) rozhraní. Ladění balíčku předá seznam DEs vybraný proces voláním [IDebugProcess2::Attach](../../extensibility/debugger/reference/idebugprocess2-attach.md). Pak zavolá SDM [IDebugProcess2::EnumPrograms](../../extensibility/debugger/reference/idebugprocess2-enumprograms.md) na portu k vytvoření výčtu programů spuštěných v rámci procesu.  
  
 Od tohoto okamžiku každý ladicí stroj připojení k programu přesně podle popisu v [připojení po spuštění](../../extensibility/debugger/attaching-after-a-launch.md), se dvěma výjimkami.  
  
 Z důvodu efektivity jsou seskupeny DEs, které jsou implementované sdílet adresní prostor s SDM tak, aby měl každý DE sadu programy, které se bude připojovat. V takovém případě [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md) volání [IDebugEngine2::Attach](../../extensibility/debugger/reference/idebugengine2-attach.md) a předává je pole programy se připojit k.  
  
 Druhou výjimkou je, že po spuštění události odeslané DE připojení k programu, který je již spuštěn, neobsahují obvykle událost vstupního bodu.  
  
## <a name="see-also"></a>Viz také  
 [Odesílání událostí spuštění po spuštění](../../extensibility/debugger/sending-startup-events-after-a-launch.md)   
 [Úlohy ladění](../../extensibility/debugger/debugging-tasks.md)

