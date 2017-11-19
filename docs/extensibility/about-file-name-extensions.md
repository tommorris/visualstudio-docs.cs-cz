---
title: "O přípony názvů souborů | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- file extensions
- file name extensions
ms.assetid: 99f4f9ff-fb84-4258-9787-6890f308a57f
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4aba03fd68fc5e0e68dbf13887de0c25094fa951
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="about-file-name-extensions"></a>O přípony názvů souborů
Při registraci příponu VSPackage přidružit verzi [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. To je důležité v případě více než jednu verzi [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] je nainstalován v počítači.  
  
 Přípony souborů pro VSPackages je zaregistrovaný pod klíčem HKEY_CLASSES_ROOT výchozí hodnotu, která odkazuje na související programový identifikátor (ProgID).  
  
 Následuje příklad registrační informace pro tuto příponu .vcproj:  
  
```  
HKEY_CLASSES_ROOT\  
   .vcproj\  
      (default)=" VisualStudio.vcproj.8.0"   
```  
  
 Soubory spojené s [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] musí mít verzí ProgID, jako například `VisualStudio.vcproj.8.0`, aby souběžně sdílená instalací produktu udržovat souboru rozšíření přidružení mezi verze produktu. Specifické pro verzi ProgID také umožňuje používat standardní příkazy, jako třeba otevřít, upravit a tak dále, bez obav přepsání nebo přepsáním pomocí jiných aplikací nebo verze [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
 V některých případech neměli byste ji měnit ProgID spojené s příponou souboru. Například ProgID pro příponu souboru .htm (progid = htmlfile) je pevný programového v počet míst v operačním systému a je známý a používá v přidružení se soubory .htm a .html.  
  
## <a name="see-also"></a>Viz také  
 [Registrace přípony názvů souborů pro nasazení vedle sebe](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md)   
 [Určení souboru obslužné rutiny pro přípony názvu souboru](../extensibility/specifying-file-handlers-for-file-name-extensions.md)