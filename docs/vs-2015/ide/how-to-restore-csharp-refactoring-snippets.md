---
title: 'Postupy: obnovení fragmentů kódu refaktoringu jazyka C# | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- unsafe expansion
- expansions, unsafe
ms.assetid: 12114273-7f2f-43d0-abcb-2d4711a3a68d
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 13867274ace5582b25482868ddd3642426b1f295
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668796"
---
# <a name="how-to-restore-c-refactoring-snippets"></a>Postupy: Obnovení fragmentů kódu refaktoringu jazyka C#
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: obnovení fragmenty C# refaktoring](https://docs.microsoft.com/visualstudio/ide/how-to-restore-csharp-refactoring-snippets).  
  
Operace refaktoringu jazyka C# využívají fragmenty kódu v následujícím adresáři:  
  
 *Instalační adresář*\Microsoft Visual Studio 14.0\VC#\Snippets\\*ID jazyka*\Refactoring  
  
 Pokud tento adresář refaktoringu, nebo všechny soubory v tomto adresáři je odstraněn nebo poškozen, pak operací refaktoringu jazyka C# nemusí fungovat v integrovaném vývojovém prostředí. Následující postupy vám umožňují obnovení fragmentů kódu refaktoringu jazyka C#.  
  
### <a name="to-verify-c-refactoring-snippets-are-available-through-the-code-snippet-manager"></a>Ověření jazyka C# jsou k dispozici prostřednictvím Správce fragmentů kódu refaktoringu fragmenty kódu  
  
1.  V **nástroje** nabídce vyberte možnost **Správce fragmentů kódů**.  
  
2.  V **Správce fragmentů kódů** dialogu **Visual C#** z **jazyk** rozevíracího seznamu.  
  
     A **refaktoringu** složky by se měla zobrazit v seznamu stromu zobrazení složek.  
  
### <a name="to-restore-refactoring-see-comment-in-code-snippet-manager"></a>K obnovení refaktoring viz komentář ve Správci fragmentů kódu  
  
1.  Pokud **refaktoringu** složka není se zobrazí v seznamu složek zobrazení stromu Správce fragmentů kódů a pak pomocí tohoto postupu můžete přidat fragmentů kódu refaktoringu zpět do Správce fragmentů kódů.  
  
2.  V **nástroje** nabídce vyberte možnost **Správce fragmentů kódů**.  
  
3.  V **Správce fragmentů kódů** dialogu **Visual C#** z **jazyk** rozevíracího seznamu.  
  
4.  Klikněte na tlačítko **přidat**. **Složka fragmentů kódů** zobrazí se dialogové okno, které vám pomůže najít a zadejte adresář, který chcete přidat zpět do Správce fragmentů kódů,.  
  
5.  Vyhledejte **refaktoringu** složku, jehož cesta k adresáři je:  
  
     *Instalační adresář*\Microsoft Visual Studio 14.0\VC#\Snippets\\*ID jazyka*\Refactoring  
  
     Skutečné cesty je podobný následujícímu výchozí instalaci:  
  
     C:\Program Files\Microsoft Visual Studio 14.0\VC#\Snippets\1033\Refactoring.  
  
6.  Klikněte na tlačítko **otevřít** v **složka fragmentů kódů** dialogové okno a potom klikněte na **OK** ve Správci fragmentů kódu.  
  
## <a name="see-also"></a>Viz také  
 [Fragmenty kódu jazyka Visual C#](../ide/visual-csharp-code-snippets.md)   
 [Refaktoring (C#)](../csharp-ide/refactoring-csharp.md)   
 [Fragmenty kódu](../ide/code-snippets.md)



