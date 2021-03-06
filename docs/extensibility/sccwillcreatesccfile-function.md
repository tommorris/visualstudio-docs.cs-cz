---
title: Funkce SccWillCreateSccFile | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- SccWillCreateSccFile
helpviewer_keywords:
- SccWillCreateSccFile function
ms.assetid: 0d7542f0-4351-41b3-b24c-960ab99c05a1
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: af6da09badf0ffea4846d35fe00b4ca146243d64
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31137051"
---
# <a name="sccwillcreatesccfile-function"></a>SccWillCreateSccFile – funkce
Tato funkce určí, zda modul plug-in zdrojového kódu podporuje vytváření MSSCCPRJ. SCC soubor pro každou z dané soubory.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
SCCRTN SccWillCreateSccFile(  
   LPVOID  pContext,  
   LONG    nFiles,  
   LPCSTR* lpFileNames,  
   LPBOOL  pbSccFiles  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [v] Ukazatel modulu plug-in kontextu zdroj ovládacího prvku.  
  
 : %{nfiles/  
 [v] Počet názvů souborů, které jsou součástí `lpFileNames` pole a také délka `pbSccFiles` pole.  
  
 lpFileNames  
 [v] Pole názvy souborů plně kvalifikovaný zkontrolujte (pole musí být přidělena volající).  
  
 pbSccFiles  
 [ve out] Pole, ve kterém můžete ukládat výsledky.  
  
## <a name="return-value"></a>Návratová hodnota  
 Očekává se, že modul plug-in implementace zdroje řízení této funkce vrátí jednu z následujících hodnot:  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|SCC_OK|Úspěch.|  
|SCC_E_INVALIDFILEPATH|Jedna z cest v poli je neplatný.|  
|SCC_E_NONSPECIFICERROR|Došlo k nespecifikované chybě.|  
  
## <a name="remarks"></a>Poznámky  
 Tato funkce je volána s seznam souborů k určení, pokud modul plug-in zdrojového kódu poskytuje podporu v MSSCCPRJ. SCC soubor pro každou z dané soubory (pro další informace o MSSCCPRJ. Soubor SCC, najdete v části [MSSCCPRJ. Soubor SCC](../extensibility/mssccprj-scc-file.md)). Zdroj ovládacího prvku zásuvné moduly můžou deklarovat, zda mají možnost vytváření MSSCCPRJ. Soubory SCC deklarováním `SCC_CAP_SCCFILE` během inicializace. Modul plug-in vrátí `TRUE` nebo `FALSE` na každý soubor `pbSccFiles` pole k určení, které daný soubory být MSSCCPRJ. Podpora SCC. Pokud modul plug-in vrátí kód úspěšnosti z funkce, jsou hodnoty v poli návratový dodržení. Při selhání se ignoruje pole.  
  
## <a name="see-also"></a>Viz také  
 [Funkce modulu Plug-in rozhraní API ovládacího prvku zdroje](../extensibility/source-control-plug-in-api-functions.md)   
 [Soubor MSSCCPRJ.SCC](../extensibility/mssccprj-scc-file.md)