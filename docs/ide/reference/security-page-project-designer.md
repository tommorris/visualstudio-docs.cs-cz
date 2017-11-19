---
title: "Stránka zabezpečení, Návrhář projektu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vb.ProjectPropertiesSecurity
- vb.XBAPProjectPropertiesSecurity
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Project Designer, Security page
- Security page in Project Designer
ms.assetid: 641d9cd3-fa07-498a-8568-3c169bb4d3d5
caps.latest.revision: "34"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4eaa6a746f67c891e9e4979f9c5b06202383e5f3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="security-page-project-designer"></a>Stránka Zabezpečení, návrhář projektu
**Zabezpečení** stránky **Návrhář projektu** slouží ke konfiguraci nastavení zabezpečení přístupu kódu pro aplikace, které jsou nasazeny pomocí [!INCLUDE[ndptecclick](../../deployment/includes/ndptecclick_md.md)] nasazení. Další informace najdete v tématu [zabezpečení přístupu kódu pro aplikace ClickOnce](../../deployment/code-access-security-for-clickonce-applications.md).  
  
 Pro přístup k **zabezpečení** klikněte na uzel projektu v **Průzkumníku řešení**a pak klikněte na **projektu** nabídky, klikněte na tlačítko **vlastnosti**. Když **Návrhář projektu** se zobrazí, klikněte na tlačítko **zabezpečení** kartě.  
  
## <a name="security-settings"></a>Nastavení zabezpečení  
 **Povolení nastavení zabezpečení ClickOnce**  
 Určuje, zda je povoleno nastavení zabezpečení v době návrhu. Pokud tato možnost vybrána, všechny ostatní možnosti na **zabezpečení** stránky nejsou k dispozici.  
  
> [!NOTE]
>  Při publikování aplikace pomocí **publikovat** průvodce, tato možnost je automaticky povolené.  
  
 Když vyberete tuto možnost, máte možnost výběru mezi dvěma přepínací tlačítka: **Toto je aplikace s úplným vztahem důvěryhodnosti** nebo **Toto je aplikace s částečnou důvěryhodností**.  
  
 Tato možnost je vybrána ve výchozím nastavení pro projekty aplikace WPF webového prohlížeče.  
  
 Tato možnost vybrána ve výchozím nastavení pro všechny ostatní typy projektu.  
  
 **Toto je aplikace s úplným vztahem důvěryhodnosti**  
 Pokud vyberete tuto možnost, aplikace, pokud je nainstalovat nebo spustit na klientském počítači požádá o oprávnění plné důvěryhodnosti. Vyhněte se použití, úplný vztah důvěryhodnosti Pokud je to možné, protože vaše aplikace bude udělen neomezený přístup k prostředkům, například systém souborů a registr.  
  
 Ve výchozím nastavení pro projekty aplikace WPF webového prohlížeče je tato možnost nastavena na částečné důvěryhodnosti.  
  
 Ve výchozím nastavení pro všechny ostatní typy projektů je tato možnost nastavena na úplný vztah důvěryhodnosti.  
  
 **Toto je aplikace s částečnou důvěryhodností**  
 Pokud vyberete tuto možnost, aplikace, pokud je nainstalovat nebo spustit na klientském počítači požádá o oprávnění částečné důvěryhodnosti. *Částečná důvěryhodnost* znamená, že se spustí jenom akce, které jsou povoleny v rámci přístupová oprávnění zabezpečení požadovaná kódu. Další informace o tom, jak nakonfigurovat oprávnění zabezpečení najdete v tématu [zabezpečení přístupu kódu pro aplikace ClickOnce](../../deployment/code-access-security-for-clickonce-applications.md).  
  
 Můžete zadat nastavení zabezpečení částečné důvěryhodnosti na možnosti v konfiguraci **oprávnění zabezpečení ClickOnce** oblasti.  
  
## <a name="clickonce-security-permissions"></a>Oprávnění zabezpečení ClickOnce  
 **Zóny, kterou vaše aplikace bude nainstalována z**  
 Určuje výchozí sadu oprávnění zabezpečení přístupu ke kódu. Zvolte **Internet** nebo **místní Intranet** pro s omezenými oprávněními nastavit, nebo zvolte **(vlastní)** chcete konfigurovat vlastní oprávnění nastavit. Pokud aplikace vyžaduje další oprávnění, než udělena v zóně, se zobrazí výzva vztahu důvěryhodnosti ClickOnce pro koncové uživatele a udělit další oprávnění. Další informace o tom, jak nakonfigurovat oprávnění zabezpečení najdete v tématu [zabezpečení přístupu kódu pro aplikace ClickOnce](../../deployment/code-access-security-for-clickonce-applications.md).  
  
 Ve výchozím nastavení pro projekty aplikace WPF webového prohlížeče, je tato možnost nastavena na **Internet**.  
  
 **Upravit oprávnění XML**  
 Otevře manifestu šablony aplikace (app.manifest) konfigurace oprávnění pro **(vlastní)** sadu oprávnění.  
  
 **Upřesnit**  
 Otevře se [rozšířené zabezpečení dialogové okno nastavení](../../ide/reference/advanced-security-settings-dialog-box.md), který slouží ke konfiguraci nastavení pro ladění aplikace s omezenými oprávněními. Tato nastavení jsou zaškrtnutá políčka během ladění a výjimek oprávnění znamenat, že vaše aplikace může potřebovat větší oprávnění než definované v zóně.  
  
## <a name="see-also"></a>Viz také  
 <xref:System.Security.Permissions.WebBrowserPermission>   
 <xref:System.Security.Permissions.MediaPermission>   
 [Zabezpečení přístupu kódu pro aplikace ClickOnce](../../deployment/code-access-security-for-clickonce-applications.md)   
 [Postupy: povolení nastavení zabezpečení ClickOnce](../../deployment/how-to-enable-clickonce-security-settings.md)   
 [Postupy: nastavení zóny zabezpečení pro aplikace ClickOnce](../../deployment/how-to-set-a-security-zone-for-a-clickonce-application.md)   
 [Postupy: nastavení vlastních oprávnění pro aplikaci ClickOnce](../../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)   
 [Postupy: ladění aplikace ClickOnce s omezenými oprávněními](../../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md)   
 [ClickOnce – zabezpečení a nasazení](../../deployment/clickonce-security-and-deployment.md)   
 [Referenční dokumentace k vlastnostem projektu](../../ide/reference/project-properties-reference.md)   
 [Dialogové okno nastavení rozšířené zabezpečení](../../ide/reference/advanced-security-settings-dialog-box.md)