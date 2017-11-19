---
title: IDebugProperty3::CreateObjectID | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugProperty3::CreateObjectID
helpviewer_keywords: IDebugProperty3::CreateObjectID
ms.assetid: f2fa81e7-822f-456e-8729-a96a18eea771
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 363a43c71a6812ee69e1fda5778eb992579e9c76
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="idebugproperty3createobjectid"></a>IDebugProperty3::CreateObjectID
Vytvoří jedinečné ID pro tuto vlastnost k zajištění, že je jedinečný mezi všechny ostatní vlastnosti.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT CreateObjectID(  
   void  
);  
```  
  
```csharp  
int CreateObjectID();  
```  
  
## <a name="return-value"></a>Návratová hodnota  
 V případě úspěchu vrátí `S_OK`, jinak vrátí kód chyby.  
  
## <a name="remarks"></a>Poznámky  
 Tato metoda je volána, když správce ladicí relace chce zajistit, že tato vlastnost je jedinečně identifikovat mezi všechny ostatní vlastnosti. Modul ladění (DE) podporuje tuto metodu, pokud jsou vlastnosti, které se zabývá již jednoznačně identifikuje. Pokud je DE nepodporuje tuto metodu, vrátí `E_NOTIMPL`.  
  
 Všechny jedinečné ID vytvořené pomocí `CreateObjectID` je zničený, když [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md) metoda je volána; to také označuje konec potřebu jednoznačné identifikaci této vlastnosti.  
  
> [!NOTE]
>  Neexistuje žádná metoda načte tento jedinečný Identifikátor, takže je DE provést, ať chce pro jedinečné ID. při `CreateObjectID` metoda je volána.  
  
## <a name="see-also"></a>Viz také  
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md)