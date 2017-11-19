---
title: "Idiaenumsymbols – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumSymbols interface
ms.assetid: 649f7bfd-86ac-49a5-8533-aff77e1bc62e
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 372279d82f9f316edf0d1aed203be1ce4e48e236
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumsymbols"></a>IDiaEnumSymbols
Provede výčet různých symboly obsažené v datovém zdroji.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDiaEnumSymbols : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Následující tabulka uvádí metody `IDiaEnumSymbols`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Idiaenumsymbols::get__newenum –](../../debugger/debug-interface-access/idiaenumsymbols-get-newenum.md)|Načte `IEnumVARIANT Interface` verzi této enumerátor.|  
|[Idiaenumsymbols::get_count –](../../debugger/debug-interface-access/idiaenumsymbols-get-count.md)|Načte počet symbolů.|  
|[Idiaenumsymbols::Item –](../../debugger/debug-interface-access/idiaenumsymbols-item.md)|Načte symbol prostřednictvím indexu.|  
|[Idiaenumsymbols::Next –](../../debugger/debug-interface-access/idiaenumsymbols-next.md)|Načte zadaný počet symboly v pořadí výčtu.|  
|[Idiaenumsymbols::Skip –](../../debugger/debug-interface-access/idiaenumsymbols-skip.md)|Přeskočí zadaný počet symboly v posloupnosti výčtu.|  
|[Idiaenumsymbols::Reset –](../../debugger/debug-interface-access/idiaenumsymbols-reset.md)|Návrat na začátek v sekvenci výčtu.|  
|[Idiaenumsymbols::clone –](../../debugger/debug-interface-access/idiaenumsymbols-clone.md)|Vytvoří enumerátor, který obsahuje stav výčtu jako aktuální enumerátor.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní poskytuje symboly seskupené podle konkrétní typ symbolu, například `SymTagUDT` (uživatelem definované typy) nebo `SymTagBaseClass`. Chcete-li pracovat s symboly seskupené podle adresy, použijte [idiaenumsymbolsbyaddr –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr.md) rozhraní.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Získejte toto rozhraní při volání těchto metod:  
  
-   [Idiasession::findchildren –](../../debugger/debug-interface-access/idiasession-findchildren.md)  
  
-   [Idiasymbol::findchildren –](../../debugger/debug-interface-access/idiasymbol-findchildren.md)  
  
-   [Idiasourcefile::get_compilands –](../../debugger/debug-interface-access/idiasourcefile-get-compilands.md)  
  
## <a name="example"></a>Příklad  
 Tento příklad ukazuje, jak získat `IDiaEnumSymbols` rozhraní a pak používat tento výčet do seznamu uživatelem definované typy (UDT).  
  
> [!NOTE]
>  `CDiaBSTR`je třída, která zabalí `BSTR` a automaticky zpracovává uvolnění řetězec při vytváření instance ocitne mimo rozsah.  
  
```C++  
void ShowUDTs(IDiaSymbol *pGlobals)  
{  
    CComPtr<IDiaEnumSymbols> pEnum;  
    CComPtr<IDiaSymbol> pSymbol;  
    HRESULT hr;  
  
    hr = pGlobals->findChildren(SymTagUDT,  
                                NULL,  
                                nsfCaseInsensitive | nsfUndecoratedName,  
                                &pEnum);  
    if (hr == S_OK)  
    {  
        while ( SUCCEEDED( hr = pEnum->Next( 1, &pSymbol, &celt ) ) &&  
                celt == 1 )  
        {  
            CDiaBSTR name;  
            if ( pSymbol->get_name( &name ) != S_OK )  
                Fatal( "get_name" );  
            printf( "Found UDT: %ws\n", name );  
            pSymbol = 0;  
        }  
    }  
}  
```  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: Dia2.h  
  
 Knihovna: diaguids.lib  
  
 Knihovny DLL: msdia80.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní (přístup k rozhraní SDK ladění)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiasession::findchildren –](../../debugger/debug-interface-access/idiasession-findchildren.md)   
 [Idiasourcefile::get_compilands –](../../debugger/debug-interface-access/idiasourcefile-get-compilands.md)   
 [Idiasymbol::findchildren –](../../debugger/debug-interface-access/idiasymbol-findchildren.md)