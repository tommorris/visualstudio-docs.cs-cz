---
title: 'Postupy: aktualizace stavového řádku | Dokumentace Microsoftu'
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
- editors [Visual Studio SDK], legacy - update status bar
ms.assetid: 7500c8a7-4913-4818-a88b-bfd1b9887cb6
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 97b96023682d1acfda5aa0c47c07169b558c7569
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42666618"
---
# <a name="how-to-update-the-status-bar"></a>Postupy: aktualizace stavového řádku
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: aktualizace stavového řádku](https://docs.microsoft.com/visualstudio/extensibility/how-to-update-the-status-bar).  
  
**Stavový řádek** se ovládací panel nachází v dolní části mnoho aplikace pro windows, který obsahuje jeden nebo více řádků textu stavu nebo ukazatele.  
  
### <a name="to-update-the-status-bar"></a>Aktualizace stavového řádku  
  
1.  Implementace <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> na každém objektu jednotlivých zobrazení (DocView), která poskytuje editoru, jako je například zobrazení formuláře a zobrazení kódu.  
  
2.  Když se volá rozhraní IDE <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A>, aktualizovat informace v **stavový řádek** voláním metody <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>.  
  
    > [!NOTE]
    >  Volání rozhraní IDE <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> pouze když vaše okno dokumentu prvotní aktivaci. Pro zbývající čas, který je aktivní okno dokumentu, je nutné aktualizovat **stavový řádek** informací jako stav editoru změny.  
  
## <a name="robust-programming"></a>Robustní programování  
 A **stavový řádek** obsahuje čtyři samostatné pole:  
  
-   Stavový text  
  
-   Indikátor průběhu  
  
-   Animovaný ikonu  
  
-   Editor informací  
  
 Další informace najdete v tématu [stavové řádky](http://msdn.microsoft.com/library/fcbc5029-1aab-4e14-adf7-419038a4935e).  
  
 Rozhraní IDE automaticky volá <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> metodu vaše <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> implementace při aktivaci okno dokumentu.  
  
 Implementátor VSPackage je zodpovědný za automatickou aktualizaci stavový text ve stavovém řádku. Rozhraní IDE obnoví tento řetězec na hodnotu "PŘIPRAVENO" Pokud textové pole Stav je nastaven na prázdný text ("") v době nečinnosti.  
  
## <a name="see-also"></a>Viz také  
 [Stavové řádky](http://msdn.microsoft.com/library/fcbc5029-1aab-4e14-adf7-419038a4935e)

