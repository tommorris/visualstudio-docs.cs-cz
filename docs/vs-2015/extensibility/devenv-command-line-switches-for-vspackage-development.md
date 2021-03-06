---
title: Přepínače příkazového řádku nástroje DEVENV pro vývoj rozšíření VSPackage | Dokumentace Microsoftu
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
- /setup command line switch
- /resetskippkgs command line switch
- /noVSIP command line switch
- /rootsuffix command line switch
- command-line switches
- registry, Visual Studio SDK
- command line, switches
- Visual Studio SDK, command-line switches
ms.assetid: d65d2c04-dd84-42b0-b956-555b11f5a645
caps.latest.revision: 17
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7bb10653a784b6d481717965e68b445c24b3f3db
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42672583"
---
# <a name="devenv-command-line-switches-for-vspackage-development"></a>Přepínače příkazového řádku nástroje Devenv pro vývoj rozšíření VSPackage
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [přepínače příkazového řádku nástroje Devenv pro vývoj rozšíření VSPackage](https://docs.microsoft.com/visualstudio/extensibility/devenv-command-line-switches-for-vspackage-development).  
  
[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] umožňuje vývojářům pro automatizaci úloh z příkazového řádku při provádění devenv.exe, soubor, který spouští integrovaného vývojového prostředí (IDE) sady Visual Studio.  
  
 Mezi úlohy patří:  
  
-   Nasazení aplikací v předem navrženými konfigurace z mimo rozhraní IDE.  
  
-   Vytváření projektů pomocí přednastavených automaticky nastavení sestavení nebo konfiguraci ladění.  
  
-   Načítání integrovaného vývojového prostředí v konkrétní konfigurace, z mimo rozhraní IDE. Kromě toho můžete přizpůsobit IDE po spuštění.  
  
## <a name="guidelines-for-switches"></a>Pokyny pro přepínače  
 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] dokumentace popisuje přepínače příkazového řádku nástroje devenv uživatelské úrovni. Další informace najdete v tématu [přepínače příkazového řádku nástroje Devenv](../ide/reference/devenv-command-line-switches.md). DEVENV podporuje také další přepínače příkazového řádku, které jsou užitečné se VSPackage vývoje, nasazení a ladění.  
  
|Přepínač příkazového řádku|Popis|  
|--------------------------|-----------------|  
|/ safemode|Spustí [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] v nouzovém režimu, načítání výchozí integrovaného vývojového prostředí a služeb. Při načítání všech balíčků VSPackage třetích stran zabraňuje přepínač/safemode [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] se spustí, čímž zajišťuje stabilní spuštění.<br /><br /> Tento přepínač nepřijímá žádné argumenty.|  
|/ resetskippkgs|Vymaže všechny Přeskočit načítání možnosti, které byly přidány podle uživatelů, kteří chtějí předejít problematické rozšíření VSPackages, pak spustí [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Přítomnost značky SkipLoading zakáže načítání VSPackage. Vymazává se značka znovu povolí načítání sady VSPackage.<br /><br /> Tento přepínač nepřijímá žádné argumenty.|  
|/rootsuffix|Spustí [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] pomocí alternativního umístění. Následující příkaz spustí místní vytvořené [!INCLUDE[vsipsdk](../includes/vsipsdk-md.md)] instalačního programu:<br /><br /> exp /RootSuffix nástroje devenv<br /><br /> V takovém případě exp identifikuje umístění s konkrétní příponou, třeba 10.0Exp spíše než 10.0. Experimentální instanci umožňuje ladit VSPackage odděleně od instance [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] , že používáte psaní kódu.<br /><br /> Tento přepínač můžete využít libovolný řetězec, který identifikuje, kterou jste vytvořili pomocí VSRegEx.exe umístění. Další informace najdete v tématu [experimentální instanci](../extensibility/the-experimental-instance.md).|  
|/Splash|Ukazuje [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] obvyklým úvodní obrazovka a poté zobrazí okno se zprávou před zobrazením hlavní integrovaného vývojového prostředí. Okno se zprávou umožňuje zkoumat úvodní obrazovka Hledat ikona produktu VSPackage, třeba.<br /><br /> Tento přepínač nepřijímá žádné argumenty.|  
  
## <a name="see-also"></a>Viz také  
 [Přidání přepínačů příkazového řádku](../extensibility/adding-command-line-switches.md)   
 [Devenv – přepínače příkazového řádku](../ide/reference/devenv-command-line-switches.md)

