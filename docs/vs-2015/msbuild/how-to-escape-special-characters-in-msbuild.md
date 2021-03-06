---
title: 'Postupy: řídicí speciální znaky v nástroji MSBuild | Dokumentace Microsoftu'
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
- special characters, escaping
- characters, escapes
- escape characters
- MSBuild, escaping special characters
ms.assetid: 1aa3669c-1647-4960-b770-752e2532102f
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a900ebe49e95b512c0f53a5542f0ba8ee238a83f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669927"
---
# <a name="how-to-escape-special-characters-in-msbuild"></a>Postupy: Zápis speciálních znaků pomocí escape sekvence v nástroji MSBuild
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postup: speciální řídicí znaky v nástroji MSBuild](https://docs.microsoft.com/visualstudio/msbuild/how-to-escape-special-characters-in-msbuild).  
  
  
Některé znaky mají speciální význam v [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] soubory projektu. Příklady znaků: středníkem (;) a hvězdičky (*). Úplný seznam těchto speciálních znaků, naleznete v tématu [speciální znaky nástroje MSBuild](../msbuild/msbuild-special-characters.md).  
  
 Chcete-li použít tyto speciální znaky jako literály v souboru projektu, se musí zadat pomocí syntaxe %*xx*, kde *xx* představuje znak šestnáctkové hodnoty ASCII.  
  
## <a name="msbuild-special-characters"></a>Speciální znaky nástroje MSBuild  
 Jedna je například použití speciálních znaků v `Include` atribut položky seznamů. Například následující seznam položek deklaruje dvě položky: `MyFile.cs` a `MyClass.cs`.  
  
```  
<Compile Include="MyFile.cs;MyClass.cs"/>  
```  
  
 Pokud chcete deklarovat, který obsahuje středníkem v názvu položky, je nutné použít %*xx* syntaxe řídicí středník a zabránit [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] z deklarace dvou samostatných položek. Například následující položka řídicí sekvence středník a deklaruje jednu položku s názvem `MyFile.cs;MyClass.cs`.  
  
```  
<Compile Include="MyFile.cs%3BMyClass.cs"/>  
```  
  
#### <a name="to-use-an-msbuild-special-character-as-a-literal-character"></a>Chcete-li použít speciální znak MSBuild jako literální znak  
  
-   Použití notace %*xx* místo speciální znaky, kde *xx* představuje šestnáctkovou hodnotu znaku standardu ASCII. Například pokud chcete použít hvězdičku (*) jako literální znak, použijte hodnotu `%2A`.  
  
## <a name="see-also"></a>Viz také  
 [Koncepty nástroje MSBuild](../msbuild/msbuild-concepts.md)   
 [Nástroj MSBuild](msbuild.md) [položky](../msbuild/msbuild-items.md)


