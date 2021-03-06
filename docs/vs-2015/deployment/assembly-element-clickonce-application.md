---
title: '&lt;sestavení&gt; – Element (aplikace ClickOnce) | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#assembly
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <assembly> element [ClickOnce application manifest]
ms.assetid: 51410569-10f9-4c0a-96b5-d39185edbefc
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: edd968ffb6f2b0422e54bc6d456c1090d189fcc0
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42671602"
---
# <a name="ltassemblygt-element-clickonce-application"></a>&lt;sestavení&gt; – Element (aplikace ClickOnce)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [ &lt;sestavení&gt; – Element (aplikace ClickOnce)](https://docs.microsoft.com/visualstudio/deployment/assembly-element-clickonce-application).  
  
Element nejvyšší úrovně pro manifest aplikace.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
      <assembly  
   manifestVersion  
/>  
```  
  
## <a name="elements-and-attributes"></a>Elementy a atributy  
 `assembly` Prvek je kořenovým elementem a je povinný. Musí být jeho první prvek `assemblyIdentity` elementu. Manifestu elementy musí být v jednom z následujících oborů názvů:  
  
 `urn:schemas-microsoft-com:asm.v1`  
  
 `urn:schemas-microsoft-com:asm.v2`  
  
 `http://www.w3.org/2000/09/xmldsig#`  
  
 Podřízené prvky prvku sestavení musí být také v těchto oborech názvů, dědičnosti nebo označování.  
  
 `assembly` Element má tento atribut.  
  
|Atribut|Popis|  
|---------------|-----------------|  
|`manifestVersion`|Požadováno. `manifestVersion` Atribut musí být nastaven na `1.0`.|  
  
## <a name="example"></a>Příklad  
 Následující příklad kódu ukazuje `assembly` elementu v manifestu aplikace pro [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikace. Tento příklad kódu je součástí většího příkladu určeného v [Manifest aplikace ClickOnce](../deployment/clickonce-application-manifest.md).  
  
```  
<asmv1:assembly   
  xsi:schemaLocation="urn:schemas-microsoft-com:asm.v1 assembly.adaptive.xsd"   
  manifestVersion="1.0"   
  xmlns:asmv3="urn:schemas-microsoft-com:asm.v3"  
  xmlns:dsig=http://www.w3.org/2000/09/xmldsig#  
  xmlns:co.v2="urn:schemas-microsoft-com:clickonce.v2"  
  xmlns="urn:schemas-microsoft-com:asm.v2"  
  xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"  
  xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"  
  xmlns:xsi=http://www.w3.org/2001/XMLSchema-instance  
  xmlns:co.v1="urn:schemas-microsoft-com:clickonce.v1">  
```  
  
## <a name="see-also"></a>Viz také  
 [ClickOnce – Manifest aplikace](../deployment/clickonce-application-manifest.md)   
 [\<sestavení > – Element](../deployment/assembly-element-clickonce-deployment.md)



