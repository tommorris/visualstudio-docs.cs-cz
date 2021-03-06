---
title: Scchistory – funkce | Dokumentace Microsoftu
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
- SccHistory
helpviewer_keywords:
- SccHistory function
ms.assetid: a636d9d3-47c1-4b48-ac6b-bcfde19d6cf9
caps.latest.revision: 17
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f3a01e3d854b2527a38595509699aa94a222a9ca
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670122"
---
# <a name="scchistory-function"></a>SccHistory – funkce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [scchistory – funkce](https://docs.microsoft.com/visualstudio/extensibility/scchistory-function).  
  
Tato funkce zobrazí historie zadané soubory.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
SCCRTN SccHistory(  
   LPVOID    pvContext,  
   HWND      hWnd,  
   LONG      nFiles,  
   LPCSTR*   lpFileNames,  
   LONG      fOptions,  
   LPCMDOPTS pvOptions  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pvContext`  
 [in] Struktura kontext modulu plug-in zdroje ovládacího prvku.  
  
 `hWnd`  
 [in] Popisovač okna integrovaného vývojového prostředí, které modul plug-in správy zdrojového kódu můžete použít jako nadřazený pro všechna dialogová okna, které poskytuje.  
  
 `nFiles`  
 [in] Počet souborů podle `lpFileName` pole.  
  
 `lpFileName`  
 [in] Pole plně kvalifikované názvy souborů.  
  
 `fOptions`  
 [in] Příkaz příznaky (aktuálně nepoužívá).  
  
 `pvOptions`  
 [in] Možností správy zdrojového kódu plug-konkrétní.  
  
## <a name="return-value"></a>Návratová hodnota  
 Modul plug-in implementaci ovládacího prvku zdroje této funkce má vracet instanci jednoho z následujících hodnot:  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|SCC_OK|Historie verzí byl úspěšně získán.|  
|SCC_I_RELOADFILE|Systém správy zdrojového kódu ve skutečnosti změny souboru na disku při načítání historie (například tím, že získáme starou verzi), takže rozhraní IDE byste znovu načíst tento soubor.|  
|SCC_E_FILENOTCONTROLLED|Soubor není pod správou zdrojových kódů.|  
|SCC_E_OPNOTSUPPORTED|Systém správy zdrojového kódu nepodporuje tuto operaci.|  
|SCC_E_NOTAUTHORIZED|Uživatel nemůže k provedení této operace.|  
|SCC_E_ACCESSFAILURE|Došlo k problému, přístup k systému správy zdrojového kódu, pravděpodobně kvůli problémům se síti nebo kolize. Doporučuje se zkuste to znovu.|  
|SCC_E_PROJNOTOPEN|Projekt nebyl otevřen.|  
|SCC_E_NONSPECIFICERROR|K nespecifikované chybě. Historie souborů nebylo možné získat.|  
  
## <a name="remarks"></a>Poznámky  
 Modul plug-in správy zdrojového kódu může zobrazit svůj vlastní dialogové okno k zobrazení historie každého souboru pomocí `hWnd` jako nadřazeného okna. Můžete také volitelné textový výstup zpětného volání funkce předány [sccopenproject –](../extensibility/sccopenproject-function.md) lze použít, pokud je podporována.  
  
 Všimněte si, že za určitých okolností, soubor zkoumají může změnit během provádění tohoto volání. Například [!INCLUDE[vsvss](../includes/vsvss-md.md)] historie příkaz umožňuje uživateli příležitost získat původní verzi souboru. V takovém případě se řídí zdroj modulu plug-in vrátí `SCC_I_RELOAD` upozornit rozhraní IDE, že je nutné znovu načíst soubor.  
  
> [!NOTE]
>  Pokud modul plug-in správy zdrojového kódu nepodporuje tuto funkci pro celou řadu soubory, lze zobrazit pouze historie souborů pro první soubor.  
  
## <a name="see-also"></a>Viz také  
 [Funkce rozhraní API modulu Plug-in zdroje ovládacího prvku](../extensibility/source-control-plug-in-api-functions.md)   
 [Sccopenproject –](../extensibility/sccopenproject-function.md)

