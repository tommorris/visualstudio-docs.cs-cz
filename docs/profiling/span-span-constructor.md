---
title: "span::span – konstruktor | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: cvmarkersobj/Concurrency::diagnostic::span::span
helpviewer_keywords: Concurrency::diagnostic::span constructor
ms.assetid: 8b5578aa-5e5c-4ac7-87c7-ce87c4246e2c
caps.latest.revision: "5"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6811f4f176bd59db0e1b934c32daf58820304349
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="spanspan-constructor"></a>span::span – konstruktor
Inicializuje novou instanci třídy `span` třídy.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
span(  
   const marker_series& _Series,  
   _In_ LPCTSTR _Format,  
   ...  
);  
span(  
   const marker_series& _Series,  
   marker_importance _Importance,  
   _In_ LPCTSTR _Format,  
   ...  
);  
span(  
   const marker_series& _Series,  
   int _Category,  
   _In_ LPCTSTR _Format,  
   ...  
);  
span(  
   const marker_series& _Series,  
   marker_importance _Importance,  
   int _Category,  
   _In_ LPCTSTR _Format,  
   ...  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `_Series`  
 Kontext řady platný značky.  
  
 `_Format`  
 Složený formátovací řetězec, který obsahuje text smíšeného s nula nebo více položek formátu, odpovídajících objektů v seznamu argumentů.  
  
 `_Importance`  
 Úroveň význam.  
  
 `_Category`  
 Kategorie.  
  
## <a name="requirements"></a>Požadavky  
 **Záhlaví:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::Diagnostic –
 
 ## <a name="see-also"></a>Viz také
 [span – třída](../profiling/span-class.md)