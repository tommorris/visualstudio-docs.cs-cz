---
title: 'Postupy: implementace najít a nahradit mechanismus | Dokumentace Microsoftu'
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
- editors [Visual Studio SDK], legacy - find and replace
ms.assetid: bbd348db-3d19-42eb-99a2-3e808528c0ca
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: eaae77979fc15954b4480a038c791a15bd95ab65
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42633839"
---
# <a name="how-to-implement-the-find-and-replace-mechanism"></a>Postupy: implementace najít a nahradit mechanismus
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [jak: implementovat najít a nahradit mechanismus](https://docs.microsoft.com/visualstudio/extensibility/how-to-implement-the-find-and-replace-mechanism).  
  
Visual Studio nabízí dva způsoby implementace najít a nahradit. Jedním ze způsobů je předat bitovou kopii text do prostředí a ten zpracování vyhledávání, zvýrazňování a nahrazení textu. To umožňuje uživatelům zadat více rozpětí textu. Alternativně vašeho balíčku VSPackage můžete řídit tento samotné funkce. V obou případech musíte upozornit prostředí o aktuální cíl a cíle pro všechny otevřené dokumenty.  
  
### <a name="to-implement-findreplace"></a>K implementaci najít a nahradit  
  
1.  Implementace <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget> rozhraní na jednom z objektů vrácených podle vlastnosti rámce <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID> nebo <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>. Pokud vytváříte vlastní editor, měli byste implementovat toto rozhraní jako součást třídy vlastní editor.  
  
2.  Použití <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetCapabilities%2A> metoda postup určení možností, které podporuje vaše editoru a označuje, zda implementuje hledání text obrázku.  
  
     Pokud váš editor podporuje text hledání obrázků, implementovat <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage%2A>.  
  
     V opačném případě implementovat <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A> a <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A>.  
  
3.  Pokud se rozhodnete implementovat <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A> a <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A> metody, můžete zjednodušit hledání úloh pomocí volání <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper> rozhraní.  
  
## <a name="see-also"></a>Viz také  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage%2A>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A>   
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSPROPID>

