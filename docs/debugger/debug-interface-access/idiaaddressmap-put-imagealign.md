---
title: "Idiaaddressmap::put_imagealign – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaAddressMap::put_imageAlign method
ms.assetid: f9ce875d-c263-43e5-a534-f34c37f9866f
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 38856520641ff2ea191e3f712a1f355e841e1aff
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idiaaddressmapputimagealign"></a>IDiaAddressMap::put_imageAlign
Nastaví zarovnání obrázku.  
  
## <a name="syntax"></a>Syntaxe  
  
```C++  
HRESULT put_imageAlign (   
   DWORD NewVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 NewVal  
 [v] Nová hodnota zarovnání obrázku pro spustitelný soubor.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Zadaná paměťová hranice je zarovnán bitové kopie (načíst spustitelné soubory). Tato zarovnání může mít vliv podle aktuální architektura systému a podle možností v době kompilace a odkaz. Zarovnání obrázku je vždy v rozsahu bajtů. Jsou platné tyto hodnoty zarovnání obrázku: 1, 2, 4, 8, 16, 32 a 64 bajtů hranice.  
  
 Aktuální zarovnání obrázku se dá načíst pomocí volání [idiaaddressmap::get_imagealign –](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md) metoda.  
  
> [!NOTE]
>  Obrázek je již načten o dobu, kterou lze volat tuto metodu. `put_imageAlign` Metoda se typicky používá při bitovou kopii byl přesunut nebo změnit, a nové zarovnání se vyžaduje.  
  
## <a name="see-also"></a>Viz také  
 [Idiaaddressmap –](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [Idiaaddressmap::get_imagealign –](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md)