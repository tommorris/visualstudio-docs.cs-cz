---
title: 'Postupy: Změna výstupního adresáře sestavení | Dokumentace Microsoftu'
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
- output directory, changing
ms.assetid: a8333c89-afb2-4b1d-b2e2-9146da852402
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a12accc247d79a68eaafc9878dc5e9d7d8c7d6dc
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42670077"
---
# <a name="how-to-change-the-build-output-directory"></a>Postupy: Změna výstupního adresáře sestavení
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: Změna výstupního adresáře sestavení](https://docs.microsoft.com/visualstudio/ide/how-to-change-the-build-output-directory).  
  
Zadejte umístění výstupu na základě podle konfigurace (pro ladění, vydání nebo obojí), vygenerované váš projekt.  
  
> [!NOTE]
>  Pokud máte **nastavení** projektu naleznete v poznámce na konci tohoto článku.  
  
## <a name="changing-the-build-output-directory"></a>Změna adresáře výstupu sestavení  
  
#### <a name="to-change-the-build-output-directory"></a>Změna výstupního adresáře sestavení  
  
1.  V panelu nabídky zvolte **projektu**, *Appname* **vlastnosti**. Můžete také kliknout pravým tlačítkem na uzel projektu v **Průzkumníka řešení** a vyberte **vlastnosti**.  
  
2.  Pokud máte projekt jazyka Visual Basic, vyberte **kompilaci** kartu. Pokud máte projekt jazyka Visual C#, vyberte **sestavení** kartu. Pokud máte projekt jazyka C++ nebo JavaScript projektu, vyberte **Obecné** kartu.  
  
3.  V rozevíracího seznamu v horní části konfigurace zvolte konfiguraci, jejíž výstup souboru umístění, které chcete změnit (debug, release nebo všechny).  
  
     Vyhledejte položku výstupní cestu (**výstupní cesta sestavení** v jazyce Visual Basic **výstupní adresář** v jazyce Visual C++ **výstupní cesta** v JavaScriptu a C#). Zadejte nový výstupní adresář sestavení relativní k adresáři projektu.  
  
> [!NOTE]
>  V nastavení projektu **název výstupního souboru** pole změní pouze umístění souboru Setup.exe, ne však umístění souborů projektu. Další informace najdete v tématu **sestavení, vlastnosti konfigurace, dialogové okno Vlastnosti projektu nasazení**.  
  
## <a name="see-also"></a>Viz také  
 [Stránka sestavení, Návrhář projektu (C#)](../ide/reference/build-page-project-designer-csharp.md)   
 [Obecná stránka vlastností (projekt)](http://msdn.microsoft.com/library/593b383c-cd0f-4dcd-ad65-9ec9b4b19c45)   
 [Kompilace a sestavení](../ide/compiling-and-building-in-visual-studio.md)



