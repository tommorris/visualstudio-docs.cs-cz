---
title: Referenční dokumentace rozhraní API (Visual Studio ladění) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], API reference
ms.assetid: e4e429da-3667-41f7-9158-a8207d13e91a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3c9007d679e36e2aa6dbab41074338395434be42
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31103237"
---
# <a name="api-reference-visual-studio-debugging"></a>Referenční dokumentace rozhraní API (Visual Studio ladění)
V části odkaz zahrnuje koncepční přehled rozhraní API, průvodce, který ukazuje syntaxi a použití pro všechny prvky rozhraní API a širokou příklady kódu. Všechny odkazy jsou abecedně uvedené podle kategorie.  
  
 Následující tabulka uvádí nejběžnější `HRESULT` hodnot vrácených metody.  
  
|Název|Popis|Hodnota|  
|----------|-----------------|-----------|  
|S_OK|Úspěch.|0x00000000|  
|E_UNEXPECTED|Neočekávaná chyba.|0x8000FFFF|  
|E_NOTIMPL|Není implementováno.|0x80004001|  
|E_OUTOFMEMORY|K dokončení operace není dostatek paměti.|0x8007000E|  
|E_INVALIDARG|Jeden nebo více argumenty nejsou platné.|0x80070057|  
|E_NOINTERFACE|Neznámé rozhraní.|0x80004002|  
|E_POINTER|Neplatný ukazatel.|0x80004003|  
|E_HANDLE|Neplatný popisovač.|0x80070006|  
|E_ABORT|Operace byla přerušena.|0x80004004|  
|E_FAIL|Neočekávaná chyba.|0x80004005|  
|E_ACCESSDENIED|Obecná chyba odepření přístupu.|0x80070005|  
  
> [!NOTE]
>  Když [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] ladění metoda vrátí `S_OK`, se předpokládá, že všechny odhlašování jsou platná parametr ukazatele, tedy provádějí žádné ověření v out parametr ukazatele při `S_OK` je vrácen.  
  
> [!NOTE]
>  Neplatný nebo `NULL` [parametry out] může způsobit chyby rozhraní IDE.  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní](../../../extensibility/debugger/reference/interfaces-visual-studio-debugging.md)   
 [Výčty](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Struktury a sjednocení](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [Pomocníci SDK pro ladění](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)   
 [Rozšiřitelnost programu Visual Studio Debugger](../../../extensibility/debugger/visual-studio-debugger-extensibility.md)