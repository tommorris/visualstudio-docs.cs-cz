---
title: "Idiaimagedata – | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaImageData interface
ms.assetid: b696f350-fc08-4352-9287-a15e87512c1e
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c76a173f137ede589b870f5119153a4233bcd730
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idiaimagedata"></a>IDiaImageData
Zpřístupní podrobnosti o základní umístění a paměť posunutí modulu nebo image.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
IDiaImageData : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Metody v tabulce Vtable pořadí  
 Následující tabulka uvádí metody `IDiaImageData`.  
  
|Metoda|Popis|  
|------------|-----------------|  
|[Idiaimagedata::get_relativevirtualaddress –](../../debugger/debug-interface-access/idiaimagedata-get-relativevirtualaddress.md)|Načte umístění ve virtuální paměti modulu vzhledem k aplikaci.|  
|[Idiaimagedata::get_virtualaddress –](../../debugger/debug-interface-access/idiaimagedata-get-virtualaddress.md)|Načte umístění ve virtuální paměti bitové kopie.|  
|[Idiaimagedata::get_imagebase –](../../debugger/debug-interface-access/idiaimagedata-get-imagebase.md)|Načte paměti umístění, kde by měla být založena bitovou kopii.|  
  
## <a name="remarks"></a>Poznámky  
 Některé datové proudy debug (XDATA, PDATA) obsahovat kopií dat, které jsou také uloženy v bitové kopii. Tyto Streamovat data objektů může být dotázán na `IDiaImageData` rozhraní. Najdete v části "Poznámky pro volající" v tomto tématu podrobnosti.  
  
## <a name="notes-for-callers"></a>Poznámky pro volající  
 Získat toto rozhraní vyvoláním `QueryInterface` na [idiaenumdebugstreamdata –](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md) objektu. Všimněte si, že ne všechny ladění datové proudy podpory `IDiaImageData` rozhraní. Například aktuálně podporují pouze XDATA a PDATA datové proudy `IDiaImageData` rozhraní.  
  
## <a name="example"></a>Příklad  
 Tento příklad vyhledá všechny datové proudy debug pro jakýkoli proud, který podporuje `IDiaImageData` rozhraní. Pokud je nalezen datový proud, se zobrazí některé informace o tohoto datového proudu.  
  
```C++  
void ShowImageData(IDiaSession *pSession)  
{  
    if (pSession != NULL)  
    {  
        CComPtr<IDiaEnumDebugStreams> pStreamsList;  
        HRESULT hr;  
  
        hr = pSession->getEnumDebugStreams(&pStreamsList);  
        if (SUCCEEDED(hr))  
        {  
            LONG numStreams = 0;  
            hr = pStreamsList->get_Count(&numStreams);  
            if (SUCCEEDED(hr))  
            {  
                ULONG fetched = 0;  
                for (LONG i = 0; i < numStreams; i++)  
                {  
                    CComPtr<IDiaEnumDebugStreamData> pStream;  
                    hr = pStreamsList->Next(1,&pStream,&fetched);  
                    if (fetched == 1)  
                    {  
                        CComPtr<IDiaImageData> pImageData;  
                        hr = pStream->QueryInterface(__uuidof(IDiaImageData),  
                                                     (void **)&pImageData);  
                        if (SUCCEEDED(hr))  
                        {  
                            CComBSTR name;  
                            hr = pStream->get_name(&name);  
                            if (SUCCEEDED(hr))  
                            {  
                                wprintf(L"Stream %s:\n",(BSTR)name);  
                            }  
                            else  
                            {  
                                wprintf(L"Failed to get name of stream\n");  
                            }  
  
                            ULONGLONG imageBase = 0;  
                            if (pImageData->get_imageBase(&imageBase) == S_OK)  
                            {  
                                wprintf(L"  image base = 0x%0I64x\n",imageBase);  
                            }  
  
                            DWORD relVA = 0;  
                            if (pImageData->get_relativeVirtualAddress(&relVA) == S_OK)  
                            {  
                                wprintf(L"  relative virtual address = 0x%08lx\n",relVA);  
                            }  
  
                            ULONGLONG va = 0;  
                            if (pImageData->get_virtualAddress(&va) == S_OK)  
                            {  
                                wprintf(L"  virtual address = 0x%0I64x\n", va);  
                            }  
                        }  
                    }  
                }  
            }  
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
 [Idiaenumdebugstreamdata –](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)