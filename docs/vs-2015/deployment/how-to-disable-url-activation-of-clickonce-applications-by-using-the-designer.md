---
title: 'Postupy: zákaz aktivace adresy URL aplikací ClickOnce pomocí návrháře | Dokumentace Microsoftu'
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
- disallowURLActivation
- URL activation, ClickOnce applications
- ClickOnce deployment, URL activation
ms.assetid: a337a582-e67c-409a-b52e-607cd1a8fc57
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 6cc5571dffba9daa3ac1f5f78e354487cbc654fe
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42675377"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications-by-using-the-designer"></a>Postupy: Zákaz aktivace adresy URL aplikací ClickOnce pomocí Návrháře
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: zakázání adresa URL aktivace z aplikací ClickOnce pomocí návrháře](https://docs.microsoft.com/visualstudio/deployment/how-to-disable-url-activation-of-clickonce-applications-by-using-the-designer).  
  
Obvykle [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikace se automaticky spustí ihned po jeho instalaci z webového serveru. Z bezpečnostních důvodů se můžete rozhodnout pro toto chování zakázat a že se uživatelé můžou spouštět aplikace z **Start** nabídky místo. Následující postup popisuje, jak zákaz aktivace adresy URL.  
  
 Tento postup lze použít pouze pro [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikace nainstalované v počítači uživatele z webového serveru. Nelze použít pro online jen pro aplikace, které lze spustit pouze pomocí jejich adresy URL. Další informace o rozdílech mezi pouze v režimu online a nainstalovaných aplikací, najdete v části [Výběr strategie nasazení ClickOnce](../deployment/choosing-a-clickonce-deployment-strategy.md).  
  
 Tento postup používá [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Tuto úlohu lze provést také pomocí [!INCLUDE[winsdklong](../includes/winsdklong-md.md)]. Další informace najdete v tématu [postupy: zakázání aktivace adresy URL z aplikací ClickOnce](../deployment/how-to-disable-url-activation-of-clickonce-applications.md).  
  
## <a name="procedure"></a>Postup  
  
#### <a name="to-disable-url-activation-for-your-application"></a>Chcete-li zákaz aktivace adresy URL pro vaši aplikaci  
  
1.  Klikněte pravým tlačítkem na název vašeho projektu v **Průzkumníka řešení**a klikněte na tlačítko **vlastnosti**.  
  
2.  Na **vlastnosti** stránky, klikněte na tlačítko **publikovat** kartu.  
  
3.  Klikněte na tlačítko **možnosti**.  
  
4.  Klikněte na tlačítko **manifesty**.  
  
5.  Zaškrtněte políčko s popiskem **blokovat aplikaci při aktivaci prostřednictvím adresy URL**.  
  
6.  Při nasazování aplikace.  
  
## <a name="see-also"></a>Viz také  
 [Publikování aplikací ClickOnce](../deployment/publishing-clickonce-applications.md)



