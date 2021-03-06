---
title: Idialoadcallback::notifydebugdir – | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyDebugDir method
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 46621c667967f0b87d197839012e830207cc306a
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2018
ms.locfileid: "31462558"
---
# <a name="idialoadcallbacknotifydebugdir"></a>IDiaLoadCallback::NotifyDebugDir
Volá se při ladění adresář byl nalezen v souboru .exe.  
  
## <a name="syntax"></a>Syntaxe  
  
```C++  
HRESULT NotifyDebugDir (   
   BOOL  fExecutable,  
   DWORD cbData,  
   BYTE  data[]  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `fExecutable`  
 [v] `TRUE` adresáři ladění je přečtení z spustitelný soubor (nikoli soubor dbg).  
  
 `cbData`  
 [v] Počet bajtů dat v adresáři ladění.  
  
 `data[]`  
 [v] Pole, které obsahuje adresáři ladění.  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby. Návratový kód se obvykle ignoruje.  
  
## <a name="remarks"></a>Poznámky  
 [Idiadatasource::loaddataforexe –](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) metoda vyvolá tento zpětného volání, pokud najde adresář ladění během zpracování na spustitelný soubor.  
  
 Tato metoda eliminuje nutnost pro klienta pro zpětnou soubor spustitelný soubor nebo ladění pro podporu informace o ladění než tu, která v souboru PDB nalezen. S těmito daty klienta rozpoznat typ ladicí informace, které jsou k dispozici a zda se nachází v spustitelný soubor nebo soubor dbg.  
  
 Většina klientů nebude nutné tento zpětného volání, protože `IDiaDataSource::loadDataForExe` metoda transparentně otevře soubory PDB i dbg, pokud je to nezbytné k obsluze symboly.  
  
## <a name="see-also"></a>Viz také  
 [Idialoadcallback2 –](../../debugger/debug-interface-access/idialoadcallback2.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)