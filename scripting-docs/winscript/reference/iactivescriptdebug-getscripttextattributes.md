---
title: IActiveScriptDebug::GetScriptTextAttributes | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptDebug.GetScriptTextAttributes
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptDebug::GetScriptTextAttributes
ms.assetid: 2e8bda34-db0c-4b2e-a17f-82c4e0dbbc8c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c8e9cd76da3e754eabce836b386893043dcd0622
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
ms.locfileid: "24793347"
---
# <a name="iactivescriptdebuggetscripttextattributes"></a>IActiveScriptDebug::GetScriptTextAttributes
Vrátí text atributy bloku libovolný text skriptu.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetScriptTextAttributes(  
   LPCOLESTR          pstrCode,  
   ULONG              uNumCodeChars,  
   LPCOLESTR          pstrDelimiter,  
   DWORD              dwFlags,  
   SOURCE_TEXT_ATTR*  pattr  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pstrCode`  
 [v] Text, blok skriptu. Tento řetězec nemusí mít hodnotu null byla ukončena.  
  
 `uNumCodeChars`  
 [v] Počet znaků v textu blok skriptu.  
  
 `pstrDelimiter`  
 [v] Adresa koncového ze skriptu bloku oddělovač. Když `pstrCode` je analyzována z datového proudu textu, hostitel se většinou používá oddělovač, například dvě jednoduché uvozovky ("), na zjištění konce bloku skriptu. Tento parametr určuje oddělovač, který se používá hostitele, která umožňuje skriptovací stroj zajistit některé podmíněného primitivní předběžného zpracování (například nahrazení jednoduché uvozovky ['] dvě jednoduchých uvozovek pro použití jako oddělovač). Přesně jak (a pokud) skriptovací stroj používá tyto informace závisí na skriptovacího stroje. Tento parametr nastavte na hodnotu NULL, pokud hostitel nepoužili oddělovač konec bloku skriptu.  
  
 `dwFlags`  
 [v] Příznaky přidružené blok skriptu. Může být kombinací těchto hodnot:  
  
|Konstanta|Hodnota|Popis|  
|--------------|-----------|-----------------|  
|GETATTRTYPE_DEPSCAN|0x0001|Označuje, že identifikátory a tečka mělo by být určené SOURCETEXT_ATTR_IDENTIFIER a SOURCETEXT_ATTR_MEMBERLOOKUP příznaků, v uvedeném pořadí.|  
|GETATTRFLAG_THIS|0x0100|Označuje, že se mají s příznakem SOURCETEXT_ATTR_THIS identifikovat identifikátor pro aktuální objekt.|  
|GETATTRFLAG_HUMANTEXT|0x8000|Označuje, že obsah a komentář textový řetězec, mělo by být určené s příznakem SOURCETEXT_ATTR_HUMANTEXT.|  
  
 `pattr`  
 [ve out] Vyrovnávací paměť tak, aby obsahovala vrácený atributy.  
  
## <a name="return-value"></a>Návratová hodnota  
 Vrátí metodu `HRESULT`. Možné hodnoty zahrnují hodnoty v následující tabulce, ale nejsou na ně omezeny.  
  
|Hodnota|Popis|  
|-----------|-----------------|  
|`S_OK`|Metoda byla úspěšná.|  
  
## <a name="remarks"></a>Poznámky  
 Inteligentního hostitele, který implementuje `IDebugDocumentText` rozhraní tuto metodu můžete použít pro delegování volání `IDebugDocumentText::GetText` metoda.  
  
 Tuto metodu pro blocích skriptu; `GetScriptletTextAttributes` metoda je určená pro skriptlety.  
  
## <a name="see-also"></a>Viz také  
 [Iactivescriptdebug – rozhraní](../../winscript/reference/iactivescriptdebug-interface.md)   
 [IActiveScriptDebug::GetScriptletTextAttributes](../../winscript/reference/iactivescriptdebug-getscriptlettextattributes.md)   
 [Idebugdocumenttext – rozhraní](../../winscript/reference/idebugdocumenttext-interface.md)   
 [IDebugDocumentText::GetText](../../winscript/reference/idebugdocumenttext-gettext.md)   
 [SOURCE_TEXT_ATTR – výčet](../../winscript/reference/source-text-attr-enumeration.md)