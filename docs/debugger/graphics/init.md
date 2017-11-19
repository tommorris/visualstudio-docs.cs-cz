---
title: "Init – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c55ddec8-9101-4673-979b-4109caca9146
caps.latest.revision: "5"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f32e2e4c5c57359acdc4348f0a83399096383ff2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="init"></a>Init
Připraví komponenta diagnostiky grafiky k aktivně zachycení a zaznamenání grafických informací do souboru protokolu grafiky v aplikaci.  
  
## <a name="syntax"></a>Syntaxe  
  
```C++  
void Init(  
  std::function<void (int len, wchar_t * pszBuffer)> vsgLogGetter  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `vsgLogGetter`  
 S entity – například funkce, – ukazatel na funkci, lambda nebo objekt funkce –, která má jako parametry Délka vyrovnávací paměti tvořený `wchar_t` a ukazatel na tento vyrovnávací paměti a vrátí `void`. Po vyvolání s entity Určuje název souboru, který se použije k zaznamenání grafických informací a zapíše ho do zadané vyrovnávací paměti před vrácením.  
  
## <a name="remarks"></a>Poznámky  
 `Init` Funkce je volána automaticky, když instance `VsgDbg` třída je vytvořený tak, že zadáte `bDefaultInit` parametr jeho konstruktoru jako `true`, jinak hodnota `Init` musí být explicitně volána před můžete zaznamenat aktivně a zaznamenání grafických informací.  
  
 Můžete dokončit a zavřete aktivní grafiky soubor protokolu voláním `UnInit`a pak zachytíte a zaznamenejte další grafických informací do nového souboru protokolu grafiky voláním `Init` znovu. To můžete opakovat tolikrát, kolikrát chcete vytvořit několik nezávislých grafiky soubory protokolů pomocí stejné `VsgDbg` instance.  
  
## <a name="see-also"></a>Viz také  
 [UnInit](init.md)