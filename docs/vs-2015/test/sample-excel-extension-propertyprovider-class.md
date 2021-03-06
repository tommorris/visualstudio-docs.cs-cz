---
title: 'Ukázka rozšíření Excel: Třída PropertyProvider | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 075d9b8d-8658-4fca-8711-08304dbac1c5
caps.latest.revision: 11
ms.author: gewarren
manager: douge
ms.openlocfilehash: d421f4f5b2f5fbdb2f78c6b72830ac8722e56aa2
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675872"
---
# <a name="sample-excel-extension-propertyprovider-class"></a>Ukázka rozšíření aplikace Excel: třída PropertyProvider
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [Ukázka rozšíření aplikace Excel: Třída PropertyProvider](https://docs.microsoft.com/visualstudio/test/sample-excel-extension-propertyprovider-class).  
  
Tento vnitřní třída rozšiřuje <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider> třídy a nabízí vlastnosti pro [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] prvků, které se záznam a přehrávání testů uživatelského rozhraní (UI).  
  
## <a name="getcontrolsupportlevel-method"></a>GetControlSupportLevel – metoda  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider.GetControlSupportLevel%2A> Metoda vrátí číslo určující úroveň podpory, které může nabídnout poskytovatel vlastností pro zadaný ovládací prvek. Další vlastnosti zprostředkovatele je vrácená hodnota vyšší, může podporovat ovládacího prvku. V takovém případě metoda zkontroluje hodnotu vlastnosti <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.TechnologyName%2A> vlastnost zadaný ovládacího prvku. Pokud je hodnota "Excel" a pokud <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.ControlTypeName%2A> značí, že je `CellElement`, metoda vrátí nejvyšší hodnotu; jinak vrací 0, což znamená, že nenabízí žádnou podporu.  
  
## <a name="getpropertynames-method"></a>GetPropertyNames – metoda  
 Vrátí slovník názvů vlastností a popisovače vlastnosti pro podporovaných vlastností ovládacího prvku Excelové buňky.  
  
## <a name="getpropertydescriptor-method"></a>GetPropertyDescriptor – metoda  
 Tato metoda je volána v rámci testovacího rozhraní se získat popisovač předdefinované vlastnosti pro poskytnutý název vlastnosti.  
  
## <a name="getpropertyvalue-and-setpropertyvalue-methods"></a>GetPropertyValue a SetPropertyValue metody  
 `GetPropertyValue` Metoda používá `Communicator` třídy tohoto rozšíření k vrácení hodnoty vlastnosti z aplikace Excel. `SetPropertyValue` Metoda používá <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard> třídy a `Communicator` součást pro nastavení hodnoty vlastnosti. Tyto metody jsou volány testovací rozhraní.  
  
## <a name="code-generation-customization-methods"></a>Metody přizpůsobení generování kódu  
 Tyto metody nejsou implementovány pro tuto příponu. Proto, že buď vrátit `null` nebo vyvolat <xref:System.NotImplementedException>.  
  
## <a name="see-also"></a>Viz také  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>   
 <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard>   
 [Rozšiřování programových testů UI a záznamů akcí k podpoře Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)



