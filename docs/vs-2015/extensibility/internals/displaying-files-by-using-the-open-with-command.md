---
title: Zobrazení souborů pomocí příkazu Otevřít | Dokumentace Microsoftu
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
- project types, supporting Open With command
- Open With command
- persistence, supporting Open With command
ms.assetid: 53794bc3-1b73-4d40-954e-cfade1abddcf
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 83160c6a55f73dc1dc81c602260ffa53830b3e1f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633448"
---
# <a name="displaying-files-by-using-the-open-with-command"></a>Zobrazení souborů pomocí příkazu Otevřít v aplikaci
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [zobrazení souborů pomocí příkazu Otevřít s](https://docs.microsoft.com/visualstudio/extensibility/internals/displaying-files-by-using-the-open-with-command).  
  
Projekt můžete požádat o integrované vývojové prostředí pro zobrazení **otevřít v** dialogové okno. Tento požadavek se zobrazí výzva k otevření souboru, který má výběr standardních editorů. Následující kroky popisují tento proces.  
  
1.  Volání projektu <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A>, zadáte třeba hodnotu OSE_UseOpenWithDialog pro `OSEOpenDocEditor` parametru.  
  
2.  Neřiďte příponou názvu souboru dokumentu, rozhraní IDE určí, editory, které uvedený v registru můžete otevřít zadaný dokument a zobrazí tyto informace **otevřít v programu** dialogové okno.  
  
    > [!NOTE]
    >  Projekty, které mají vnitřní editor, který musí být součástí **otevřít v** dialogovému oknu musíte zaregistrovat objekt pro vytváření editoru pro každý takový editor. Vnitřní editory pracovat pouze spolu s konkrétní typ projektu, který se prosazuje provádění <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> metody. Rozhraní IDE má objekt factory integrovaného editoru pro základní editor textového a binárního editoru. Integrované vývojové prostředí také vytvoří instanci objektu pro vytváření editoru jménem každý registrovaný přidružení souboru Windows. Příkladem takových souborů je Microsoft Word.  
  
3.  Poté, co uživatel vybere položku ze **otevřít v** dokumentu voláním otevře se dialogové okno, pak IDE <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A> metoda. Další informace najdete v tématu [jak: otevřít standardní editory](../../extensibility/how-to-open-standard-editors.md).  
  
## <a name="see-also"></a>Viz také  
 [Otevření a uložení položek projektu](../../extensibility/internals/opening-and-saving-project-items.md)   
 [Zobrazení souborů pomocí příkazu Otevřít soubor](../../extensibility/internals/displaying-files-by-using-the-open-file-command.md)   
 [Postupy: Otevření standardních editorů](../../extensibility/how-to-open-standard-editors.md)

