---
title: "Idiaframedata::get_virtualaddress – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaFrameData::get_virtualAddress method
ms.assetid: de137bee-132f-4aae-a067-9578b7a3e6d4
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8387b7b5096f0efe5e05a560f5c76af03fa7d165
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idiaframedatagetvirtualaddress"></a>IDiaFrameData::get_virtualAddress
Načte virtuální adresy (VA) kód pro rámečku.  
  
## <a name="syntax"></a>Syntaxe  
  
```C++  
HRESULT get_virtualAddress (   
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Vrátí virtuální adresu kód pro rámečku.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`. Vrátí `S_FALSE` -li tato vlastnost není podporována. Jinak vrátí kód chyby.  
  
## <a name="see-also"></a>Viz také  
 [Idiaframedata –](../../debugger/debug-interface-access/idiaframedata.md)