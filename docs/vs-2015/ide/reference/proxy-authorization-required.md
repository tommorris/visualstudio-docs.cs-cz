---
title: Vyžaduje se autorizace proxy | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c2d24ae1-9902-460e-b72a-0299eed9ee82
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 855fa85a8135ceac60f262fc5510fad4aa34b006
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669448"
---
# <a name="proxy-authorization-required"></a>Vyžaduje se autorizace proxy
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [nutná autorizace Proxy](https://docs.microsoft.com/visualstudio/ide/reference/proxy-authorization-required).  
  
  
K této chybě obvykle dochází, když jsou uživatelé připojeni ke službě Visual Studio Online prostřednictvím proxy serveru a proxy server blokuje volání. Visual Studio Online slouží k ukládání uživatel přihlášený rozhraní IDE.  
  
## <a name="to-correct-this-error"></a>Oprava této chyby  
  
-   Restartujte sadu Visual Studio. By se zobrazit dialogové okno ověřování proxy serveru. V dialogovém okně zadejte svoje přihlašovací údaje.  
  
-   Pokud předchozí krok problém nevyřeší, může to být vzhledem k tomu, že váš proxy server zobrazovat výzvu k zadání pověření pro http://go.microsoft.com řeší, ale provádí se *. visualStudio.com adresy. Pro tyto servery potřebujete na seznam povolených v následujícím seznamu pro odblokování všech scénářů přihlašování v aplikaci Visual Studio:  
  
    -   *.windows.net  
  
    -   *.microsoftonline.com  
  
    -   *.visualstudio.com  
  
    -   *.microsoft.com  
  
    -   *.live.com  
  
-   V opačném případě můžete odebrat http://go.microsoft.com adresy, ze seznamu povolených, aby se zobrazí dialogové okno ověřování proxy serveru pro obě http://go.microsoft.com adresy a koncové body serveru při restartování sady Visual Studio.  
  
-   NEBO  
  
-   Pokud chcete použít výchozí pověření s proxy serverem, máte následující:  
  
    1.  Hledání devenv.exe.config (konfigurační soubor devenv.exe): **%ProgramFiles%\Microsoft Visual Studio 14.0\Common7\IDE** (nebo **% ProgramFiles (x86) %\Microsoft Visual Studio 14.0\Common7\IDE**) .  
  
    2.  V konfiguračním souboru najít `<system.net>` blokovat a přidejte tento kód:  
  
        ```xml  
        <defaultProxy enabled="true" useDefaultCredentials="true">  
            <proxy bypassonlocal="True" proxyaddress=" HYPERLINK "http://<yourproxy:port#" http://<yourproxy:port#>"/>  
        </defaultProxy>  
  
        ```  
  
         Je třeba vložit adresu proxy serveru správná pro vaši síť v `proxyaddress="<http://<yourproxy:port#>`.  
  
-   NEBO  
  
-   Můžete také postupujte podle pokynů v [tento příspěvek](http://blogs.msdn.com/b/rido/archive/2010/05/06/how-to-connect-to-tfs-through-authenticated-web-proxy.aspx) přidáte kód, který vám umožní používat proxy server.



