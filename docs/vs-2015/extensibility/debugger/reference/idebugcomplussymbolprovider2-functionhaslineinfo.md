---
title: IDebugComPlusSymbolProvider2::FunctionHasLineInfo | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- FunctionHasLineInfo
- IDebugComPlusSymbolProvider2::FunctionHasLineInfo
ms.assetid: e1b508f1-6521-492f-b110-ab957744a037
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b760f9f2f80fefb9c3dbbe092cf2da9ac565ba61
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670877"
---
# <a name="idebugcomplussymbolprovider2functionhaslineinfo"></a>IDebugComPlusSymbolProvider2::FunctionHasLineInfo
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [IDebugComPlusSymbolProvider2::FunctionHasLineInfo](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugcomplussymbolprovider2-functionhaslineinfo).  
  
Určuje, zda má zadanou metodu informace řádku.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp#  
HRESULT FunctionHasLineInfo(  
   IDebugAddress* pAddress  
);  
```  
  
```csharp  
int FunctionHasLineInfo(  
   IDebugAddress pAddress  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pAddress`  
 [in] Adresa pro ladění, která je reprezentována [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) rozhraní. Tato adresa musí být METHOD_ADDRESS.  
  
## <a name="return-value"></a>Návratová hodnota  
 Pokud je úspěšná, vrátí `S_OK`; v opačném případě vrátí `S_FALSE`.  
  
## <a name="example"></a>Příklad  
 Následující příklad ukazuje, jak pro tuto metodu implementovat **CDebugSymbolProvider** objekt, který zveřejňuje [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md) rozhraní.  
  
```cpp#  
HRESULT CDebugSymbolProvider::FunctionHasLineInfo(  
    IDebugAddress* pAddress  
)  
{  
    HRESULT hr = S_OK;  
    CDEBUG_ADDRESS address;  
    CComPtr<CModule> pModule;  
  
    METHOD_ENTRY( CDebugSymbolProvider::LoadSymbol );  
  
    IfFalseGo( pAddress, E_INVALIDARG );  
  
    IfFailGo( pAddress->GetAddress( &address ) );  
  
    ASSERT(address.addr.dwKind == ADDRESS_KIND_METADATA_METHOD);  
    IfFalseGo( address.addr.dwKind == ADDRESS_KIND_METADATA_METHOD, S_FALSE );  
  
    IfFailGo( GetModule( address.GetModule(), &pModule) );  
  
    if (!pModule->FunctionHasLineInfo( address.addr.addr.addrMethod.tokMethod,  
                                       address.addr.addr.addrMethod.dwVersion))  
    {  
  
        // S_FALSE indicates this method does not have line info  
  
        hr = S_FALSE;  
    }  
  
Error:  
  
    METHOD_EXIT( CDebugSymbolProvider::LoadSymbol, hr );  
  
    return hr;  
}  
```  
  
## <a name="see-also"></a>Viz také  
 [IDebugComPlusSymbolProvider2](../../../extensibility/debugger/reference/idebugcomplussymbolprovider2.md)

