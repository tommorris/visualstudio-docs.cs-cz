---
title: Showwebbrowser – příkaz | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- view.showwebbrowser
helpviewer_keywords:
- ShowWebBrowser command
- View.ShowWebBrowser command
ms.assetid: c6a4fbd6-8e9d-45cc-8b2f-93990d065e78
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: de730650216f67d3f620fa85cad0a98148ce2ee3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666303"
---
# <a name="showwebbrowser-command"></a>ShowWebBrowser – příkaz
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [showwebbrowser – příkaz](https://docs.microsoft.com/visualstudio/ide/reference/showwebbrowser-command).  
  
  
Zobrazí adresu URL zadanou v okně webového prohlížeče buď v rámci integrovaného vývojového prostředí (IDE) nebo mimo prostředí IDE.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
View.ShowWebBrowser URL [/new][/ext]  
```  
  
## <a name="arguments"></a>Arguments  
 `URL`  
 Požadováno. Adresa URL (Uniform Resource Locator) pro webový server.  
  
## <a name="switches"></a>Přepínače  
 / Nový  
 Volitelné. Určuje, že se zobrazí v nové instanci webového prohlížeče.  
  
 /ext  
 Volitelné. Určuje, že se zobrazí ve webovém prohlížeči výchozí mimo rozhraní IDE.  
  
## <a name="remarks"></a>Poznámky  
 Alias **showwebbrowser –** příkaz je **přejděte** nebo **nav**.  
  
## <a name="example"></a>Příklad  
 Následující příklad zobrazí domovská stránka MSDN Online ve webovém prohlížeči mimo rozhraní IDE. Pokud instance webového prohlížeče je už otevřená, je použit. v opačném případě se spustí novou instanci.  
  
```  
>View.ShowWebBrowser http://msdn.microsoft.com /ext  
```  
  
## <a name="see-also"></a>Viz také  
 [Příkazy sady Visual Studio](../../ide/reference/visual-studio-commands.md)   
 [Okno příkazového řádku](../../ide/reference/command-window.md)   
 [Pole najít/příkaz](../../ide/find-command-box.md)   
 [Aliasy příkazů sady Visual Studio](../../ide/reference/visual-studio-command-aliases.md)



