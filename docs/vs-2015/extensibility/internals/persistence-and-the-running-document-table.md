---
title: Trvalost a spuštění tabulky dokumentů | Dokumentace Microsoftu
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
- persistence, managing
- IVsPersistHierarchyItem interface, implementing
- architecture, persistence
- running document table (RDT), architecture
ms.assetid: 27117eae-6c58-4189-a61a-1397a43b5ecf
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 44f8025bd20fe6522ec0f835e299a2a9efd9ca1e
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42671797"
---
# <a name="persistence-and-the-running-document-table"></a>Trvalost a spuštěná tabulka dokumentů
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [trvalosti a spuštění tabulky dokumentů](https://docs.microsoft.com/visualstudio/extensibility/internals/persistence-and-the-running-document-table).  
  
V [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE, projekty jsou zcela zodpovědní za správu trvalost jejich položky projektu, které jsou-li toho dosáhnout pomocí služby, <xref:Microsoft.VisualStudio.Shell.Interop.SVsRunningDocumentTable>. Dokumenty představují základní jednotkou přetrvávání v prostředí sady Visual Studio. Projekty koordinovat otevření, uložení a přejmenování dokumentů s tabulce spuštěných dokumentů (r...), prostředek, který sleduje stav všech otevřených dokumentech.  
  
## <a name="managing-persistence"></a>Správa trvalosti  
 Projekty řízen implementace službu trvalého uložení prostředí <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem> rozhraní. Zatímco prostředí nikdy nesmí přímo dotazem dokument k uchování samotné, požádá vlastnící projekt (nebo hierarchie) k uložení dokumentu. Umožňuje pro projekt uložte jeho data položky projektu do místních souborů, vzdálené soubory, databáze, úložiště nebo jiné médium.  
  
 Globální prostředí udržuje rámcový. Prostředí udržuje položky pro všechna otevřená okna a dokumenty v r..., díky tomu je možné pro něho přijímat speciální oznámení, jako je například při zavření řešení. Kromě toho rámcový umožňuje prostředí tak, aby sledovat jejich odpovídající uzly v **Průzkumníka řešení**. Rámcový udržuje jeden záznam na otevřené, trvalé objektu, včetně souborů projektu a položek projektů dokumenty.  
  
## <a name="see-also"></a>Viz také  
 [Spuštění tabulky dokumentů](../../extensibility/internals/running-document-table.md)   
 [Výběr a měna v prostředí IDE](../../extensibility/internals/selection-and-currency-in-the-ide.md)

