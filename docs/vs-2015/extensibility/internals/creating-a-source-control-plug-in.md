---
title: Vytvoření modulu Plug-in správy zdrojového kódu | Dokumentace Microsoftu
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
- plug-ins, source control
- source control plug-ins
- source control [Visual Studio SDK], plug-ins
ms.assetid: c7e69fa4-150e-469a-a6fc-fa1260bdbb07
caps.latest.revision: 19
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d9e9687459759e6b04938adfc8695322288f48d8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666142"
---
# <a name="creating-a-source-control-plug-in"></a>Vytvoření modulu plug-in správy zdrojového kódu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [vytváření modulu Plug-in zdrojového ovládacího prvku](https://docs.microsoft.com/visualstudio/extensibility/internals/creating-a-source-control-plug-in).  
  
Visual Studio SDK poskytuje prostředky, které vám umožní přidat možnost zdrojového ovládacího prvku [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] integrované vývojové prostředí (IDE). To vám umožní používat jakékoli knihovnu DLL modulu plug-in, který splňuje pomocí rozhraní API modulu Plug-in zdroje ovládacího prvku uvedených v této dokumentaci.  
  
## <a name="in-this-section"></a>V tomto oddílu  
 [Začínáme](../../extensibility/internals/getting-started-with-source-control-plug-ins.md)  
 Popisuje postup instalace modulu plug-in správy zdrojového kódu a zvýrazní aktuálně k dispozici verze rozhraní API modulu Plug-in zdroje ovládacího prvku.  
  
 [Architektura](../../extensibility/internals/source-control-plug-in-architecture.md)  
 Pomocí diagramu architektury popisují integrace správy zdrojového kódu pomocí modulu plug-in [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] integrovaného vývojového prostředí.  
  
 [Testovací příručka pro moduly plug-in správy zdrojového kódu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)  
 Poskytuje pokyny o tom, jak otestovat instalaci a používání modulu plug-in správy zdrojového kódu.  
  
## <a name="related-sections"></a>Související oddíly  
 [Vytvoření balíčku VSPackage správy zdrojového kódu](../../extensibility/internals/creating-a-source-control-vspackage.md)  
 Popisuje, jak vytvořit ovládací prvek zdroje balíčku VSPackage, která nejen poskytuje funkce správy zdrojového kódu, ale nahrazuje [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] zdrojového ovládacího prvku uživatelského rozhraní.  
  
 [Moduly plug-in správy zdrojového kódu](../../extensibility/source-control-plug-ins.md)  
 Obsahuje úplný seznam všech prvků v rozhraní API modulu Plug-in zdroje ovládacího prvku.  
  
 [Správa zdrojového kódu](../../extensibility/internals/source-control.md)  
 Tento článek popisuje možnosti pro implementaci správy zdrojového kódu jako integrovaná funkce [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].

