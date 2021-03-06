---
title: Distribuce aplikací izolovaného prostředí | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c503a985-d67a-4ef8-9123-7744a78f2f17
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7388a5b723b5346f1f653024215c16ba474fa48a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42678719"
---
# <a name="distributing-isolated-shell-applications"></a>Distribuce aplikací izolovaného prostředí
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [distribuce aplikací izolovaného prostředí](https://docs.microsoft.com/visualstudio/extensibility/distributing-isolated-shell-applications).  
  
Chcete-li vytvořit aplikací izolovaného prostředí musíte nainstalovat Visual Studio a Visual Studio SDK. K distribuci aplikace na počítače jiných uživatelů nebo zákazníků, musí obsahovat speciální distribuovatelných balíčků pro izolovaného prostředí.  
  
## <a name="prerequisites-for-distributing-isolated-shell-applications"></a>Požadavky distribuce aplikací izolovaného prostředí  
  
|Název|Popis|  
|----------|-----------------|  
|Visual Studio SDK|Sady SDK potřebujete pro vývoj a testování rozšíření [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Sady SDK můžete použít také k vytvoření vlastní instance sady Visual Studio izolované prostředí.<br /><br /> Visual Studio je předpokladem pro sadu SDK.|  
|Izolované prostředí distribuovatelné součásti Microsoft Visual Studio|Redistribuovatelný balíček při vytváření prostředí pro nástroje v sadě Visual Studio zahrnují ve vašem instalačním programu izolované prostředí. Distribuovatelný balíček rozhraní izolovaného prostředí zahrnuje rozhraní .NET Framework 4.5.|  
  
## <a name="creating-an-installation-program-for-the-application"></a>Vytváření instalačního programu pro aplikaci  
 Je nutné vytvořit zvláštní instalační program pro vaši aplikaci integrované nebo izolované prostředí. Další informace najdete v tématu [instalace izolované aplikační prostředí](../extensibility/installing-an-isolated-shell-application.md).  
  
## <a name="allowing-for-updates-to-your-application"></a>Povolení aktualizací do vaší aplikace  
 Instalační program musíte povolit možnost, že vaše aplikace bude aktualizován, aktualizace od Microsoftu nebo aktualizace vaší společnosti. Další informace o aktualizacích naleznete v tématu [pokyny údržbu aplikací izolovaného prostředí](../extensibility/servicing-guidelines-for-isolated-shell-applications.md).

