---
title: IDiaSymbol::getSrcLineOnTypeDefn | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
ms.assetid: ad554d18-9988-4b64-ad71-e7594c266e94
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c5972c89d545cc0b8394b425e91cecf6aa2532bd
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674141"
---
# <a name="idiasymbolgetsrclineontypedefn"></a>IDiaSymbol::getSrcLineOnTypeDefn
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDiaSymbol::getSrcLineOnTypeDefn](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/idiasymbol-getsrclineontypedefn).  
  
Načte zdrojový soubor a číslo řádku, která označuje, kde je definován zadaný uživatelem definovaného typu.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT getSrcLineOnTypeDefn(  
   IDiaLineNumber **ppResult);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppResult`  
 [out] A `IDiaLineNumber` objekt, který obsahuje číslo zdrojového souboru a řádku kde definovaný uživatelem.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí `S_FALSE` nebo kód chyby.  
  
## <a name="see-also"></a>Viz také  
 [Idiasymbol –](../../debugger/debug-interface-access/idiasymbol.md)   
 [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)



