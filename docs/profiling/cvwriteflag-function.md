---
title: Cvwriteflag – funkce | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvWriteFlagExVA
- cvmarkers/CvWriteFlagExW
- cvmarkers/CvWriteFlagExVW
- cvmarkers/CvWriteFlagExA
helpviewer_keywords:
- CvWriteFlagExW method
- CvWriteFlagExVA method
- CvWriteFlagExA method
- CvWriteFlagExVW method
ms.assetid: ee9da1e2-7b34-4cba-81e2-215d25d32e4d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 417d901504eb20894b3bd3e83d286dac4e66b072
ms.sourcegitcommit: 58052c29fc61c9a1ca55a64a63a7fdcde34668a4
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2018
ms.locfileid: "34749369"
---
# <a name="cvwriteflag-function"></a>Cvwriteflag – funkce
Zapíše příznak vizualizér souběžnosti trasovacího souboru.  
  
## <a name="syntax"></a>Syntaxe  
  
```C  
HRESULT CvWriteFlagExW(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCWSTR pMessage,  
    ...  
    );  
  
HRESULT CvWriteFlagExA(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCSTR pMessage,  
    ...  
    );  
  
HRESULT CvWriteFlagExVW(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCWSTR pMessage,  
    _In_ va_list argList);  
  
HRESULT CvWriteFlagExVA(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCSTR pMessage,  
    _In_ va_list argList);  
```  
  
#### <a name="parameters"></a>Parametry  
 `argList`  
 Seznam argumentů.  
  
 `category`  
 Kategorie.  
  
 `level`  
 Úroveň význam.  
  
 `pMarkerSeries`  
 Kontext řady platný značky. Nemůže mít hodnotu NULL.  
  
 `pMessage`  
 Řetězec formátu zpráv. Nemůže mít hodnotu NULL.  
  
## <a name="return-value"></a>Návratová hodnota  
 S_OK, pokud zpráva je úspěšně zapsána. Kód chyby v případě, že byly všechny chyby. Makra úspěšné nebo NEÚSPĚŠNÉ použijte ke kontrole chybový stav.  
  
## <a name="requirements"></a>Požadavky  
 **Záhlaví:** *cvmarkers.h*  
  
 **Unicode:** cvwriteflagexw –, cvwriteflagexvw –  
  
 **ANSI:** cvwriteflagexa –, cvwriteflagexva –  
  
## <a name="see-also"></a>Viz také:  
 [Referenční dokumentace knihoven jazyka C++](../profiling/cpp-library-reference.md)