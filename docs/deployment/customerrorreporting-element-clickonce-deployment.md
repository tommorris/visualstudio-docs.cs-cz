---
title: "&lt;customErrorReporting&gt; – Element (ClickOnce – nasazení) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-deployment
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords: <customErrorReporting> element [ClickOnce deployment manifest]
ms.assetid: 7d31816e-c692-46b5-9cc9-753284b3bcda
caps.latest.revision: "6"
author: stevehoag
ms.author: shoag
manager: wpickett
ms.openlocfilehash: 238e4c0c0fe9021424b48963eac7d21bf6f9a049
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="ltcustomerrorreportinggt-element-clickonce-deployment"></a>&lt;customErrorReporting&gt; – Element (ClickOnce – nasazení)
Určuje identifikátor URI zobrazíte, když dojde k chybě.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<customErrorReporting  
   uri  
/>  
```  
  
## <a name="remarks"></a>Poznámky  
 Tento element je volitelný. Bez toho [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] zobrazí dialogové okno chyby zobrazující zásobník výjimky. Pokud `customErrorReporting` nachází element [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] místo toho zobrazí identifikátor URI indikován `uri` parametr. Cílový identifikátor URI, bude obsahovat jako parametry vnější třídu výjimek, třídu informacích o vnitřní výjimce a zpráva o vnitřní výjimce.  
  
 Tento prvek slouží k přidání chybách funkce do vaší aplikace. Vzhledem k tomu, že generovaný identifikátor URI obsahuje informace o typu chyby, můžete analyzovat vašeho webu a zobrazit, například obrazovku řešení potíží tyto informace.  
  
## <a name="example"></a>Příklad  
 Následující fragment kódu ukazuje `customErrorReporting` element společně s generovaný identifikátor URI, může být.  
  
```  
<customErrorReporting uri=http://www.contoso.com/applications/error.asp />  
  
Example Generated Error:  
http://www.contoso.com/applications/error.asp? outer=System.Deployment.Application.InvalidDeploymentException&&inner=System.Deployment.Application.InvalidDeploymentException&&msg=The%20application%20manifest%20is%20signed,%20but%20the%20deployment%20manifest%20is%20unsigned.%20Both%20manifests%20must%20be%20either%20signed%20or%20unsigned.  
```  
  
## <a name="see-also"></a>Viz také  
 [ClickOnce – Manifest nasazení](../deployment/clickonce-deployment-manifest.md)