---
title: "Ověřování systému během vývoje | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-techdebt
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: dependency diagrams
ms.assetid: c9dafb47-7b1d-4c72-9432-d43be3db1799
caps.latest.revision: "37"
author: alexhomer1
ms.author: ahomer
manager: douge
ms.openlocfilehash: 56d67aff89c7f0cf58911cebfdaf5bfdb1464796
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="validate-your-system-during-development"></a>Ověřování systému během vývoje
Visual Studio může pomoct Udržujte software konzistentní s požadavky na uživatele a architektuře systému.  
  
 Jaké verze sady Visual Studio podporovat každé z těchto funkcí najdete v tématu [verze podpora architektura a modelování nástroje](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).  
  
## <a name="key-tasks"></a>Klíčové úlohy  
 Pomocí následujících úloh ověření vašeho softwaru.  
  
|**Úlohy**|**Související témata**|  
|---------------|---------------------------|  
|**Zajistěte, aby váš software splňuje požadavky uživatelů**:<br /><br /> Požadavky a architektury modely můžete uspořádat testy systému a jeho součástí. Tento postup pomáhá, zajistěte, aby test požadavky, které jsou důležité pro uživatele a dalších zúčastněných osob a pomůže vám rychle aktualizovat testy při změně požadavky.|-   [Vývoj testů z modelu](../modeling/develop-tests-from-a-model.md)|  
|**Ujistěte se, že váš software konzistentní s určený návrh vašeho systému:**<br /><br /> Diagramy závislostí popisují určený závislostí mezi součástmi aplikace. Během vývoje můžete ověřit, že skutečné závislosti v kódu odpovídají zamýšlené.|-   [Vytváření diagramů závislost z vašeho kódu](../modeling/create-layer-diagrams-from-your-code.md)<br />-   [Ověřování kódu pomocí diagramů závislostí](../modeling/validate-code-with-layer-diagrams.md)|  
  
## <a name="external-resources"></a>Externí zdroje  
  
|**Kategorie**|**Odkazy**|  
|------------------|---------------|  
|**Videa**|![odkaz na video](../data-tools/media/playvideo.gif "PlayVideo") [Channel 9: Doug sedm: pochopení kódu a návrhu systému sadou Visual Studio 2010](http://go.microsoft.com/fwlink/?LinkId=216100)<br /><br /> ![odkaz na video](../data-tools/media/playvideo.gif "PlayVideo") [Channel 9: architektury aplikace pomocí Diagram závislostí](http://go.microsoft.com/fwlink/?LinkID=201117)<br /><br /> ![odkaz na video](../data-tools/media/playvideo.gif "PlayVideo") [MSDN How do I řady: postup ověření kódu pomocí diagramů závislostí](http://go.microsoft.com/fwlink/?LinkID=214405)|  
|**Fóra**|-   [Visual Studio vizualizace a modelování nástroje](http://go.microsoft.com/fwlink/?LinkId=184720)<br />-   [Visual Studio vizualizace a modelování SDK (nástroje DSL)](http://go.microsoft.com/fwlink/?LinkId=184721)|  
|**Blogy**|-   [Visual Studio ALM a Team Foundation Server blogu](http://go.microsoft.com/fwlink/?LinkID=201340)|  
|**Technické články a deníků**|[Architektura softwaru MSDN](http://go.microsoft.com/fwlink/?LinkId=201343)|  
  
## <a name="see-also"></a>Viz také  
 [Testování aplikace](https://www.visualstudio.com/en-gb/docs/test/overview)   
 [Modelování uživatelských požadavků](../modeling/model-user-requirements.md)   
 [Analýza a modelování vaší architektury](../modeling/analyze-and-model-your-architecture.md)

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]