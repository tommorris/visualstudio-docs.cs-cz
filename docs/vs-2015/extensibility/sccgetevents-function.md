---
title: Sccgetevents – funkce | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SccGetEvents
helpviewer_keywords:
- SccGetEvents function
ms.assetid: 32f8147d-6dcc-465e-b07b-42da5824f9b0
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1e73fea52d207d4f9834d5c3eabb15bf733c7e23
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674103"
---
# <a name="sccgetevents-function"></a>SccGetEvents – funkce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [sccgetevents – funkce](https://docs.microsoft.com/visualstudio/extensibility/sccgetevents-function).  
  
Tato funkce načítá události ve frontě stav.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
SCCRTN SccGetEvents (  
   LPVOID pvContext,  
   LPSTR  lpFileName,  
   LPLONG lpStatus,  
   LPLONG pnEventsRemaining  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pvContext  
 [in] Struktura kontext modulu plug-in zdroje ovládacího prvku.  
  
 lpFileName  
 [out v] Vyrovnávací paměti, kde modul plug-in správy zdrojového kódu vloží název vrácený souboru (maximálně _MAX_PATH znaků).  
  
 lpStatus  
 [out v] Vrátí stavový kód (viz [souboru stavový kód](../extensibility/file-status-code-enumerator.md) možných hodnot).  
  
 pnEventsRemaining  
 [out v] Vrátí počet položek vlevo ve frontě po tomto volání. Pokud toto číslo je velká, volající může rozhodnout pro volání [sccqueryinfo –](../extensibility/sccqueryinfo-function.md) získat všechny informace o najednou.  
  
## <a name="return-value"></a>Návratová hodnota  
 Modul plug-in implementaci ovládacího prvku zdroje této funkce má vracet instanci jednoho z následujících hodnot:  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|SCC_OK|Získáte události bylo úspěšné.|  
|SCC_E_OPNOTSUPPORTED|Tato funkce není podporována.|  
|SCC_E_NONSPECIFICERROR|K nespecifikované chybě.|  
  
## <a name="remarks"></a>Poznámky  
 Tato funkce je volána při nečinnosti zpracování zobrazíte, pokud byly všechny aktualizace stavu souborů pod správou zdrojových kódů. Modul plug-in správy zdrojového kódu udržuje všechny soubory, které ví o stavu a pokaždé, když změny stavu je třeba poznamenat, pomocí modulu plug-in, stav a přidružený soubor jsou uložené ve frontě. Když `SccGetEvents` nazývá horní prvek fronty se načte a vrátí. Tato funkce je omezen na vrací pouze informace uložené v mezipaměti a musí mít velmi rychlé vyřízení (to znamená bez čtení disku nebo systém správy zdrojového kódu s žádostí o stav); jinak výkonu rozhraní IDE může začít snížit.  
  
 Pokud není žádná aktualizace stavu do sestavy, modul plug-in správy zdrojového kódu ukládá prázdný řetězec ve vyrovnávací paměti, na které odkazuje `lpFileName`. V opačném případě modul plug-in ukládá úplnou cestu název souboru pro které informace o stavu se změní a vrátí odpovídající stavový kód (jedna z hodnot, které jsou podrobně popsané v [souboru stavový kód](../extensibility/file-status-code-enumerator.md)).  
  
## <a name="see-also"></a>Viz také  
 [Funkce rozhraní API modulu Plug-in zdroje ovládacího prvku](../extensibility/source-control-plug-in-api-functions.md)   
 [Kód stavu souboru](../extensibility/file-status-code-enumerator.md)

