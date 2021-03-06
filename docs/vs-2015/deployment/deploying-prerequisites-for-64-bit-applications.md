---
title: Nasazení nezbytných součástí pro 64bitové aplikace | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [Visual Studio], 64-bit
- 64-bit [Visual Studio]
- 64-bit programming [Visual Studio]
- 64-bit applications [Visual Studio]
ms.assetid: 87399e20-5510-41e4-b5b7-4a87c5773f21
caps.latest.revision: 25
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 0f98a611b382f3884ede2e1e239944b9e584ab77
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669436"
---
# <a name="deploying-prerequisites-for-64-bit-applications"></a>Nasazení nezbytných součástí pro 64bitové aplikace
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [nasazení nezbytných součástí pro 64bitové aplikace](https://docs.microsoft.com/visualstudio/deployment/deploying-prerequisites-for-64-bit-applications).  
  
ClickOnce – nasazení podporuje instalaci aplikací na 64bitových platformách. Cílové platformy jsou **x86** pro 32bitové platformy, **x64** pro počítače podporuje AMD64 a podporou technologie EM64T instrukční sadu, a **Itanium** pro procesor Itanium 64-bit.  
  
## <a name="prerequisites"></a>Požadavky  
 V následující tabulce jsou uvedeny distribuovatelné součásti, které můžete použít jako požadavky na instalaci 64bitové aplikace.  
  
 Pokud vyberete požadovanou součást, která se nevyznačuje 64bitové komponenty, může se zobrazit upozornění oznamující, že vybrané balíčky nejsou k dispozici pro 64bitovou platformu.  
  
|Distribuovatelné součásti|Podpora x64|Podpora IA64|  
|---------------------|-----------------|------------------|  
|[!INCLUDE[vsto_runtime](../includes/vsto-runtime-md.md)]|Ano|Ne|  
|Knihovny Visual C++ 2010 Runtime (IA64)|Ne|Ano|  
|Visual C++ 2010 Runtime knihovny (x64)|Ano|Ne|  
|Microsoft .NET Framework 4 (x86 a x64)|Ano||  
|Microsoft .NET Framework 4 Client Profile (x86 a x64)|Ano||  
  
## <a name="see-also"></a>Viz také  
 [Nasazení aplikací, služeb a komponent](../deployment/deploying-applications-services-and-components.md)   
 [Postupy: instalace předpokladů s aplikací ClickOnce](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)   
 [64bitové aplikace](http://msdn.microsoft.com/library/fd4026bc-2c3d-4b27-86dc-ec5e96018181)



