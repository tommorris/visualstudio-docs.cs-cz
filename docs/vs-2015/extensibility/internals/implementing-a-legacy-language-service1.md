---
title: Implementace starší verze jazyka1 | Dokumentace Microsoftu
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
- language services, managed
ms.assetid: df638f24-166d-4b80-be82-c9c39ca7a556
caps.latest.revision: 19
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6c77e935946d06dd2448c1f9bda85fd8b6b69aa2
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42696118"
---
# <a name="implementing-a-legacy-language-service"></a>Implementace služby starší verze jazyka
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [implementace starší verze jazyka1](https://docs.microsoft.com/visualstudio/extensibility/internals/implementing-a-legacy-language-service1).  
  
Můžete použít třídy v rámci spravovaného balíčku (MPF) implementace služby starší verze jazyka, který podporuje širokou škálu funkcí, jako jsou zvýraznění syntaxe, párování složených závorek a dokončování IntelliSense.  
  
 Služby starší verze jazyka jsou implementovány jako součást sady VSPackage, ale novější způsob implementace funkce služba jazyka je pro použití rozšíření MEF. Další informace o nový způsob implementace služby jazyka najdete v tématu [Editor a rozšíření služeb jazyka](../../extensibility/editor-and-language-service-extensions.md).  
  
> [!NOTE]
>  Doporučujeme vám, že začnete používat nový editor API co nejdříve. Tím vylepšíme výkonu vaší služby jazyka a umožňují využívat nové funkce editoru.  
  
## <a name="in-this-section"></a>V tomto oddílu  
 [Přehled služby starší verze jazyka](../../extensibility/internals/legacy-language-service-overview.md)  
 Přehled funkcí služby jazyka, které jsou podporovány v MPF.  
  
 [Implementace služby starší verze jazyka](../../extensibility/internals/implementing-a-legacy-language-service2.md)  
 Popisuje, co je potřeba implementovat služba jazyka pomocí MPF.  
  
 [Registrace služby starší verze jazyka](../../extensibility/internals/registering-a-legacy-language-service1.md)  
 Popisuje kroky, které jsou nutné k registraci služby jazyka založeného na MPF s [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 [Analyzátor a skener služby starší verze jazyka](../../extensibility/internals/legacy-language-service-parser-and-scanner.md)  
 Popisuje dva analyzátory, které jsou nutné k implementaci pomocí MPF všechny funkce služby jazyka.  
  
 [Návod: Vytvoření služby starší verze jazyka](../../extensibility/internals/walkthrough-creating-a-legacy-language-service.md)  
 Popisuje základní kroky, které jsou nutné k implementaci služby MPF jazyk v sadě VSPackage.  
  
 [Návod: Získání seznamu nainstalovaných fragmentů kódu (implementace starší verze)](../../extensibility/internals/walkthrough-getting-a-list-of-installed-code-snippets-legacy-implementation.md)  
 Ukazuje techniky získání seznamu nainstalovaných fragmentů kódu.  
  
 [Funkce služby starší verze jazyka](../../extensibility/internals/legacy-language-service-features1.md)  
 Obsahuje odkazy na témata této podrobné informace, co je třeba provést k implementaci pomocí MPF všechny funkce služby jazyka.

