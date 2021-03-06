---
title: Sccquerychanges – funkce | Dokumentace Microsoftu
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
- SccQueryChanges
helpviewer_keywords:
- SccQueryChanges function
ms.assetid: 4cd58eb3-6952-49b1-9620-8682e3eaa604
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 95f1e5a21ba74779080c601acd42d5deedb75d7c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666823"
---
# <a name="sccquerychanges-function"></a>SccQueryChanges – funkce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [sccquerychanges – funkce](https://docs.microsoft.com/visualstudio/extensibility/sccquerychanges-function).  
  
Tato funkce vytvoří výčet daný seznam files a poskytuje informace o změnách název pro každý soubor prostřednictvím funkce zpětného volání.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
SCCRTN SccQueryChanges(  
   LPVOID           pContext,  
   LONG             nFiles,  
   LPCSTR*          lpFileNames,  
   QUERYCHANGESFUNC pfnCallback,  
   LPVOID           pvCallerData  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [in] Ukazatel kontext modulu plug-in zdroje ovládacího prvku.  
  
 %{nfiles/  
 [in] Počet souborů v `lpFileNames` pole.  
  
 lpFileNames  
 [in] Pole názvy souborů, chcete-li získat informace.  
  
 pfnCallback  
 [in] Funkce zpětného volání, která se zavolá k názvu každého souboru v seznamu (viz [QUERYCHANGESFUNC](../extensibility/querychangesfunc.md) podrobnosti).  
  
 pvCallerData  
 [in] Hodnota, která se předají beze změny funkci zpětného volání.  
  
## <a name="return-value"></a>Návratová hodnota  
 Modul plug-in implementaci ovládacího prvku zdroje této funkce má vracet instanci jednoho z následujících hodnot:  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|SCC_OK|Dotaz proces úspěšně dokončil.|  
|SCC_E_PROJNOTOPEN|Projekt nebyl otevřen ve správě zdrojového kódu.|  
|SCC_E_ACCESSFAILURE|Došlo k problému, přístup k systému správy zdrojového kódu, pravděpodobně kvůli problémům se síti nebo kolize.|  
|SCC_E_NONSPECIFICERROR|Došlo k neurčené nebo obecné chybě.|  
  
## <a name="remarks"></a>Poznámky  
 Změny, která je dotazována pro mají obor názvů: konkrétně, přejmenování, přidávání a odebírání souboru.  
  
## <a name="see-also"></a>Viz také  
 [Funkce rozhraní API modulu Plug-in zdroje ovládacího prvku](../extensibility/source-control-plug-in-api-functions.md)   
 [QUERYCHANGESFUNC](../extensibility/querychangesfunc.md)   
 [Chybové kódy](../extensibility/error-codes.md)

