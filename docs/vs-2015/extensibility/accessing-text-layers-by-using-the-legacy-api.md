---
title: Přístup k textu vrstvy pomocí starší verze rozhraní API | Dokumentace Microsoftu
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
- editors [Visual Studio SDK], legacy - text layers
ms.assetid: 2258fcdd-38d1-479d-b8f8-1d4e6525f72c
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bfc9cd494f308244791b82f3f001e2bd54f71204
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42676922"
---
# <a name="accessing-text-layers-by-using-the-legacy-api"></a>Přístup k textu vrstvy pomocí starší verze rozhraní API
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [přístup k textu vrstvy pomocí starší verze rozhraní API](https://docs.microsoft.com/visualstudio/extensibility/accessing-text-layers-by-using-the-legacy-api).  
  
Text vrstva obvykle zapouzdřuje určitý aspekt rozložení textu. Například vrstva "funkce na-time" Skryje text před a za funkci obsahující znak stříšky (textový kurzor).  
  
 Text vrstvě se nachází mezi vyrovnávací paměť a zobrazení a mění způsob zobrazení se zobrazí obsah přípravné vyrovnávací paměti.  
  
## <a name="text-layer-information"></a>Informace o vrstvě textu  
 Následující seznam popisuje, jak fungují text vrstvy [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]:  
  
-   Text ve vrstvě text můžete opatřený s barevné zvýrazňování syntaxe a značky.  
  
-   Momentálně nelze implementovat vlastní vrstvy.  
  
-   Poskytuje vrstvu <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>, který je odvozen z <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>. Samotné vyrovnávací paměti textu je také implementováno jako vrstvu, která umožňuje zobrazení řešit polymorphically vrstvách.  
  
-   Libovolný počet vrstvy můžou být mezi zobrazením a vyrovnávací paměti. Každá vrstva se zabývá pouze vrstvy pod ní a zobrazení se zabývá do značné míry vrstvě úplně nahoře. (Zobrazení má některé informace o vyrovnávací paměti.)  
  
-   Vrstva může mít vliv pouze vrstvy, které jsou pod ním. Ho nemůže ovlivnit vrstvy nad ním nad rámec standardních události pocházející.  
  
-   V editoru skrytý text, syntetické a zalamování řádků jsou implementovány jako vrstvy. Skryté a syntetické text můžete implementovat bez práci přímo s vrstvami. Další informace najdete v tématu [osnovy ve službě starší verze jazyka](../extensibility/internals/outlining-in-a-legacy-language-service.md) a <xref:Microsoft.VisualStudio.TextManager.Interop.IVsSyntheticTextSession>.  
  
-   Každá vrstva text má vlastní místní systém souřadnic, který je zveřejněný prostřednictvím <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer> rozhraní. Zalamování řádků vrstvy, například může obsahovat dva řádky během základní textové vyrovnávací paměti může obsahovat pouze jeden řádek.  
  
-   Zobrazení komunikuje s vrstvami prostřednictvím <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView> rozhraní. Pomocí tohoto rozhraní sjednotit zobrazení souřadnic s vyrovnávací paměť souřadnic.  
  
-   Žádné vrstvy, jako je vrstva syntetické text, který pochází text musí poskytnout implementaci místní <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.CreateTrackingPoint%2A>.  
  
-   Kromě <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>, musí implementovat vrstvu text <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer> a aktivovat události v <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLinesEvents> rozhraní.  
  
## <a name="see-also"></a>Viz také  
 [Barevné zvýrazňování syntaxe ve vlastních editorech](../extensibility/syntax-coloring-in-custom-editors.md)   
 [Text značky pomocí starší verze rozhraní API](../extensibility/using-text-markers-with-the-legacy-api.md)   
 [Přizpůsobení nabídky a ovládací prvky editoru pomocí starší verze rozhraní API](../extensibility/customizing-editor-controls-and-menus-by-using-the-legacy-api.md)

