---
title: Třída VsgDbg | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6722263c-ccef-40c7-a0ae-87a863fbab00
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 927990cb8fb21dfeaf25a681cfb0a222ecc3c8ed
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42632382"
---
# <a name="vsgdbg-class"></a>VsgDbg – třída
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [třída VsgDbg](https://docs.microsoft.com/visualstudio/debugger/graphics/vsgdbg-class).  
  
Reprezentuje rozhraní pro programovací řízení součásti diagnostiky grafiky v aplikaci.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
class VsgDbg;  
```  
  
## <a name="members"></a>Členové  
 `VsgDbg` Třída podporuje následující členy.  
  
### <a name="public-constructors"></a>Veřejné konstruktory  
  
|Název|Popis|  
|----------|-----------------|  
|[VsgDbg::VsgDbg (konstruktor)](../debugger/vsgdbg-vsgdbg-constructor.md)|Vytvoří instanci objektu `VsgDbg` třídy a volitelně připraví komponentu v aplikaci diagnostiky grafiky k aktivně zachycení a zaznamenání grafických informací.|  
|[VsgDbg::~VsgDbg (destruktor)](../debugger/vsgdbg-tilde-vsgdbg-destructor.md)|Odstraní instanci `VsgDbg` třídy.|  
  
### <a name="public-methods"></a>Veřejné metody  
  
|Název|Popis|  
|----------|-----------------|  
|[AddMessage](../debugger/addmessage.md)|Přidá vlastní zprávu pro diagnostiku grafiky HUD (zobrazení vedoucí nahoru).|  
|[BeginCapture](../debugger/begincapture.md)|Začne sběr intervalu, který bude končit `EndCapture`.|  
|[CaptureCurrentFrame](../debugger/capturecurrentframe.md)|Zaznamená zbytek aktuálního snímku do souboru protokolu grafiky.|  
|[Copy (zachytávání prostřednictvím kódu programu)](../debugger/copy-programmatic-capture.md)|Zkopíruje obsah aktivní grafiky (.vsglog) protokolu do nového souboru.|  
|[EndCapture](../debugger/endcapture.md)|Končí zachycení interval, který byl spuštěn s `BeginCapture`.|  
|[Init](../debugger/init.md)|Připraví komponentu v aplikaci diagnostiky grafiky k aktivně zachycení a zaznamenání grafických informací.|  
|[ToggleHUD](../debugger/togglehud.md)|Přepíná překrytí HUD diagnostiky grafiky, nebo vypnout.|  
|[UnInit](../debugger/uninit.md)|Soubor protokolu grafiky dokončí, zavře a uvolní prostředky, které byly použity při aplikaci se aktivně zaznamenávání informací grafiky.|  
  
## <a name="remarks"></a>Poznámky  
 `VsgDbg` Třída představuje rozhraní, které můžete použít k ovládání funkcí diagnostiky grafiky prostřednictvím kódu programu. Některé funkce můžete použít i v případě, že nejsou aktivně zachytávání a zaznamenávání informací grafiky; Jedná se o `AddMessage` členské funkce a `ToggleHUD` členskou funkci. Členské funkce Příprava součást diagnostiky grafiky, spuštění nebo zastavení aktivní zachycení informací grafiky v aplikaci, nebo musí být volána, zatímco tato aplikace je aktivně zachytávání a zaznamenání grafických informací do souboru protokolu grafiky.



