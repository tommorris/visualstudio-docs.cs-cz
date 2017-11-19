---
title: "Idialinenumber::get_columnnumberend – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaLineNumber::get_columnNumberEnd method
ms.assetid: 02fa56c1-87b6-405a-adee-3bb6bc62de2d
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b87233f3d63c896ea70c7efef9a65b0ce6693251
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idialinenumbergetcolumnnumberend"></a>IDiaLineNumber::get_columnNumberEnd
Načte číslo na základě jedné zdrojové sloupce, které končí výraz nebo příkaz.  
  
## <a name="syntax"></a>Syntaxe  
  
```C++  
HRESULT get_columnNumberEnd (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Vrátí číslo sloupce, které končí výraz nebo příkaz. Pokud je hodnota nula, pak informace o sloupci koncoví neexistuje.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`. Vrátí `S_FALSE` -li tato vlastnost není podporována. Jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda vrátí hodnotu sloupce je bajt posun na řádek na pozici za poslední znak příkaz na řádek.  
  
## <a name="see-also"></a>Viz také  
 [Idialinenumber –](../../debugger/debug-interface-access/idialinenumber.md)