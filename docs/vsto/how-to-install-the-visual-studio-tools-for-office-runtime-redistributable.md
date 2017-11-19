---
title: 'Postupy: instalace sady Visual Studio Tools for Office Runtime Redistributable | Microsoft Docs'
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office runtime [Office development in Visual Studio]
- installing Office development tools in Visual Studio
ms.assetid: ac7a9ad3-e810-4d7f-a0e2-9992c9036b8d
caps.latest.revision: "94"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 8d3439a98a445761a8d357d9b4bef631da034943
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-install-the-visual-studio-tools-for-office-runtime-redistributable"></a>Postupy: Instalace nástrojů Visual Studio Tools for Office runtime Redistributable
  Visual Studio 2010 Tools for Office Runtime musí být nainstalován na každém počítači, který spouští řešení, které jsou vytvořené pomocí nástroje Microsoft Office developer tools v [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Modul runtime se nainstaluje automaticky při instalaci [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]a Microsoft Office. Další informace najdete v tématu [Visual Studio Tools for Office Runtime instalace scénáře](../vsto/visual-studio-tools-for-office-runtime-installation-scenarios.md).  
  
 Je třeba postupovat podle pokynů ruční instalace níže v následujících situacích:  
  
-   Je potřeba nainstalovat [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] na serveru. Například chcete použít <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> třídy ke správě řešení na úrovni dokumentu na serveru.  
  
-   Potřebujete nainstalovat modul runtime na počítači, který již má všechny další požadavky pro řešení pro systém Office nainstalován.  
  
    > [!NOTE]  
    >  Musíte být správce na vývojovém počítači, aby instalaci rozhraní .NET Framework a [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)].  
  
### <a name="to-install-the-visual-studio-tools-for-office-runtime"></a>K instalaci sady Visual Studio Tools for Office runtime  
  
1.  Nainstalujte [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] nebo novější.  
  
    -   Ke stažení [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)], najdete v části [rozhraní Microsoft .NET Framework 4 (Webová instalační služba)](http://go.microsoft.com/fwlink/?LinkId=178957).  
  
    -   Ke stažení [!INCLUDE[net_client_v40_long](../vsto/includes/net-client-v40-long-md.md)], najdete v části [rozhraní Microsoft .NET Framework 4 Client Profile (Webová instalační služba)](http://go.microsoft.com/fwlink/?LinkId=178958).  
  
    -   Ke stažení [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)], najdete v části [rozhraní Microsoft .NET Framework 4.5](http://www.microsoft.com/download/details.aspx?id=30653).  
  
2.  Spustit vstor_redist.exe k instalaci [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)].  
  
     Můžete stáhnout tyto soubory instalaci ze [Visual Studio 2010 Tools for Office Runtime](http://go.microsoft.com/fwlink/?LinkId=140384). Požadavky na [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] shodovat s požadavky na rozhraní .NET Framework.  
  
     [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]Obsahuje jazykové sady. Pokud vaše instalace systému Windows je nastavena na jiný jazyk než anglický, můžete zobrazit zprávy runtime ve stejném jazyce, který používáte pro Windows. Podobně pokud koncoví uživatelé instalovat [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] a poté spusťte řešení v instalaci systému Windows, které jsou nastaveny na jiný jazyk než anglický, runtime zprávy se zobrazí ve stejném jazyce jako Windows. V některých případech může být nutné další jazykové sady. Například může být nutné další jazykové sady, pokud vaše kopie systému Windows používá více než jedna jazyková nastavení nebo přepnutí na jiný jazyk po jste již nainstalovali [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]. Můžete najít jazykové sady v [Microsoft Visual Studio 2010 Tools pro sadu Microsoft Office System (verze 4.0 Runtime) Language Pack](http://go.microsoft.com/fwlink/?LinkId=140386).  
  
## <a name="see-also"></a>Viz také  
 [Začínáme &#40; vývoj pro Office v sadě Visual Studio &#41;](../vsto/getting-started-office-development-in-visual-studio.md)   
 [Konfigurace počítače pro vývoj řešení pro systém Office](../vsto/configuring-a-computer-to-develop-office-solutions.md)   
 [Postupy: Konfigurace počítače pro vývoj řešení pro systém Office](../vsto/how-to-configure-a-computer-to-develop-office-solutions.md)   
 [Postupy: instalace primární spolupracující sestavení sady Office](../vsto/how-to-install-office-primary-interop-assemblies.md)   
 [Správa dokumentů na serveru s použitím třídy ServerDocument](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md)   
 [Nasazení řešení Office](../vsto/deploying-an-office-solution.md)  
  
  