---
title: 'Postupy: nastavení vlastních oprávnění pro aplikaci ClickOnce | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce applications, permissions
- permissions, ClickOnce applications
ms.assetid: 660459ca-ef73-44a8-b323-610001f63b93
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 6cf4b1c91650bf505daececfdf46ba42cfee68fb
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42683229"
---
# <a name="how-to-set-custom-permissions-for-a-clickonce-application"></a>Postupy: Nastavení vlastních oprávnění pro aplikaci ClickOnce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: nastavení vlastních oprávnění pro aplikaci ClickOnce](https://docs.microsoft.com/visualstudio/deployment/how-to-set-custom-permissions-for-a-clickonce-application).  
  
Můžete nasadit [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikaci, která používá výchozí oprávnění pro zóny Internetu a místního intranetu. Alternativně můžete vytvořit vlastní zónu pro konkrétní oprávnění, které aplikace potřebuje. Můžete to provést úpravou oprávnění zabezpečení na **zabezpečení** stránku **Návrháře projektu**.  
  
### <a name="to-customize-a-permission"></a>Přizpůsobení oprávnění  
  
1.  S projekt vybraný v **Průzkumníka řešení**na **projektu** nabídky, klikněte na tlačítko **vlastnosti**.  
  
2.  Klikněte na tlačítko **zabezpečení** kartu.  
  
3.  Vyberte **povolit nastavení zabezpečení ClickOnce** zaškrtávací políčko.  
  
4.  Vyberte **Toto je aplikace s částečnou důvěryhodností** přepínač.  
  
     Ovládací prvky **oprávnění zabezpečení ClickOnce** oddílu jsou povolené.  
  
5.  Z **vaše aplikace bude provedena instalace ze zóny** rozevíracího seznamu, klikněte na tlačítko **(vlastní)**.  
  
6.  Klikněte na tlačítko **editovat XML soubor oprávnění**.  
  
     Soubor app.manifest se otevře v editoru XML.  
  
7.  Před `</applicationRequestMinimum>` prvku, přidejte kód XML pro oprávnění, která vaše aplikace vyžaduje.  
  
    > [!NOTE]
    >  Můžete použít `ToXml` metoda oprávnění nastavená pro generování kódu XML pro manifest aplikace. Například pro generování kódu XML pro <xref:System.Security.Permissions.EnvironmentPermission> sadu oprávnění, volání <xref:System.Security.Permissions.EnvironmentPermission.ToXml%2A> metody. Další informace o struktuře oprávnění XML naleznete v tématu [NIB: postupy: Import oprávnění nastavit pomocí souboru XML](http://msdn.microsoft.com/en-us/dea16b54-c108-408a-ac36-cdc05f746236).  
  
## <a name="see-also"></a>Viz také  
 [Zabezpečování aplikací ClickOnce](../deployment/securing-clickonce-applications.md)   
 [Zabezpečení přístupu ke kódu pro aplikace ClickOnce](../deployment/code-access-security-for-clickonce-applications.md)   
 [Zabezpečování aplikací ClickOnce](../deployment/securing-clickonce-applications.md)



