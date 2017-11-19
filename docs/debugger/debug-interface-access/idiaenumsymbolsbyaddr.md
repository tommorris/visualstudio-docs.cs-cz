---
title: "Idiaenumsymbolsbyaddr – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumSymbolsbyAddr interface
ms.assetid: 37d3dcdf-e4fa-4354-b5e1-8843566b52ac
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4efdd5297b1a4b995ba7d3e45edc9b2c982f6ecd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumsymbolsbyaddr"></a>IDiaEnumSymbolsByAddr
Vytvoří výčet podle adresy různé symboly obsažené v datovém zdroji.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDiaEnumSymbolsByAddr : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Následující tabulka uvádí metody `IDiaEnumSymbolsByAddr`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Idiaenumsymbolsbyaddr::symbolbyaddr –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr-symbolbyaddr.md)|Umisťuje enumerátor provedením vyhledávání podle části a posun.|  
|[Idiaenumsymbolsbyaddr::symbolbyrva –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr-symbolbyrva.md)|Umisťuje enumerátor provedením vyhledávání podle relativní virtuální adresy (RVA).|  
|[Idiaenumsymbolsbyaddr::symbolbyva –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr-symbolbyva.md)|Umisťuje enumerátor provedením vyhledávání pomocí virtuální adresy (VA).|  
|[Idiaenumsymbolsbyaddr::Next –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr-next.md)|Načte další symboly v pořadí podle adresy. Aktualizuje pozice enumerátor tak počet načtených elementů.|  
|[Idiaenumsymbolsbyaddr::prev –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr-prev.md)|Načte předchozí symboly v pořadí podle adresy. Aktualizuje pozice enumerátor tak počet načtených elementů.|  
|[Idiaenumsymbolsbyaddr::clone –](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr-clone.md)|Vytvoří kopii objektu.|  
  
## <a name="remarks"></a>Poznámky  
 Toto rozhraní poskytuje symboly seskupené podle adres. Pro práci s symboly seskupená podle typu, například `SymTagUDT` (uživatelem definovaný typ) nebo `SymTagBaseClass`, použijte [idiaenumsymbols –](../../debugger/debug-interface-access/idiaenumsymbols.md) rozhraní.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Získat voláním toto rozhraní [idiasession::getsymbolsbyaddr –](../../debugger/debug-interface-access/idiasession-getsymbolsbyaddr.md) metoda.  
  
## <a name="example"></a>Příklad  
 Tato funkce zobrazí název a adresu všechny symboly seřazené podle relativní virtuální adresy.  
  
```C++  
void ShowSymbolsByAddress(IDiaSession *pSession)  
{  
    CComPtr<IDiaEnumSymbolsByAddr> pEnumByAddr;  
    if ( FAILED( psession->getSymbolsByAddr( &pEnumByAddr ) ) )  
    {  
        Fatal( "getSymbolsByAddr" );  
    }  
    CComPtr<IDiaSymbol> pSym;  
    if ( FAILED( pEnumByAddr->symbolByAddr( 1, 0, &pSym ) ) )  
    {  
        Fatal( "symbolByAddr" );  
    }  
    DWORD rvaLast = 0;  
    if ( pSym->get_relativeVirtualAddress( &rvaLast ) == S_OK )  
    {  
        pSym = 0;  
        if ( FAILED( pEnumByAddr->symbolByRVA( rvaLast, &pSym ) ) )  
        {  
            Fatal( "symbolByAddr" );  
        }  
        printf( "Symbols in order\n" );  
        do  
        {   
            CDiaBSTR name;  
            if ( pSym->get_name( &name ) != S_OK )  
            {  
                printf( "\t0x%08X (%ws) <no name>\n", rvaLast );  
            }  
            else  
            {  
               printf( "\t0x%08X %ws\n", rvaLast, name );  
            }  
            pSym = 0;  
            celt = 0;  
            if ( FAILED( hr = pEnumByAddr->Next( 1, &pSym, &celt ) ) )  
            {  
                break;  
            }  
        } while ( celt == 1 );  
    }  
}  
```  
  
## <a name="requirements"></a>Požadavky  
 Záhlaví: Dia2.h  
  
 Knihovna: diaguids.lib  
  
 Knihovny DLL: msdia80.dll  
  
## <a name="see-also"></a>Viz také  
 [Rozhraní (přístup k rozhraní SDK ladění)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiasession::getsymbolsbyaddr –](../../debugger/debug-interface-access/idiasession-getsymbolsbyaddr.md)   
 [Idiaenumsymbols –](../../debugger/debug-interface-access/idiaenumsymbols.md)