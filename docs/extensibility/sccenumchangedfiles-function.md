---
title: Funkce SccEnumChangedFiles | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SccEnumChangedFiles
helpviewer_keywords: SccEnumChangedFiles function
ms.assetid: 76cac510-107b-4c1a-ba60-9c39b6db2e71
caps.latest.revision: "12"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0ad62f14ea658e4af6e22d4beef410e6d9cf02df
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="sccenumchangedfiles-function"></a>SccEnumChangedFiles – funkce
Předložen seznam místních souborů, tato funkce určuje, které soubory se liší od odpovídající verze v databázi zdrojové kódu ovládacího prvku.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
SCCRTN SccEnumChangedFiles(  
   LPVOID  pContext,  
   HWND    hWnd,  
   LONG    cFiles,  
   LPCSTR* lpFileNames,  
   LONG*   plIsFileDifferent  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [v] Ukazatel modulu plug-in kontextu zdroj ovládacího prvku.  
  
 hWnd  
 [v] Obslužná rutina do okna IDE, modul plug-in správy zdroje můžete použít jako nadřazený objekt pro všechna dialogová okna poskytuje.  
  
 cFiles  
 [v] Číslo zadané v souboru názvy `lpFileNames` pole. Taky Určuje velikost `plIsFileDifferent` pole.  
  
 lpFileNames  
 [v] Pole názvy místních souborů ke kontrole.  
  
 plIsFileDifferent  
 [ve out] Pole hodnot, který ukazuje rozdíl stav každého souboru (pole musí obsahovat alespoň `cFiles` položky). Nenulové hodnoty znamená, že soubor se liší.  
  
## <a name="return-value"></a>Návratová hodnota  
 Očekává se, že modul plug-in implementace zdroje řízení této funkce vrátí jednu z následujících hodnot:  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|SCC_OK|Operace byla úspěšně dokončena.|  
|SCC_UNSPECIFIEDERROR|Obecná chyba.|  
  
## <a name="see-also"></a>Viz také  
 [Funkce modulu Plug-in rozhraní API ovládacího prvku zdroje](../extensibility/source-control-plug-in-api-functions.md)