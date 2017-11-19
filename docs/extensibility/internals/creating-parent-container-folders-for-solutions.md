---
title: "Vytváření složek nadřazený kontejner pro řešení | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- solutions, creating parent containers
- source control plug-ins, creating parent containers
ms.assetid: 961e68ed-2603-4479-a306-330eda2b2efa
caps.latest.revision: "15"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6ea901fe4e380fd867db1c63e44bc1cb6e144feb
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="creating-parent-container-folders-for-solutions"></a>Vytváření složek nadřazený kontejner pro řešení
V modulu Plugin řízení zdroj API verze 1.2 může uživatel určit, jeden kořenový zdroj ovládacího prvku cíl pro všechny webové projekty v řešení. Tento jeden kořenový nazývá Super Unified kořenové (SUR).  
  
 V modulu Plugin řízení zdroj API verze 1.1 Pokud uživatel přidaný vícenásobných řešení ke správě zdrojového kódu byl uživatel vyzván k zadejte jeden zdroj cíl ovládacího prvku pro každý webový projekt.  
  
## <a name="new-capability-flags"></a>Nové funkce příznaky  
 `SCC_CAP_CREATESUBPROJECT`  
  
 `SCC_CAP_GETPARENTPROJECT`  
  
## <a name="new-functions"></a>Nové funkce  
 [SccCreateSubProject](../../extensibility/scccreatesubproject-function.md)  
  
 [SccGetParentProjectPath](../../extensibility/sccgetparentprojectpath-function.md)  
  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE téměř vždy vytvoří složku SUR při přidávání řešení do správy zdrojového kódu. Konkrétně dělá to tak, v následujících případech:  
  
-   Projekt je sdílená webového projektu.  
  
-   Existují různé jednotky pro projekt a soubor řešení.  
  
-   Existují jiné sdílené složky pro projekt a soubor řešení.  
  
-   Projekty byly přidány samostatně (v řízené zdroje řešení).  
  
 V [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] je navrženo, že název složky SUR být stejný jako název řešení bez přípony. Následující tabulka shrnuje chování ve dvou verzích.  
  
|Funkce|tSource řízení Plug-in rozhraní API verze 1.1|Zdroj ovládacího prvku modulu Plug-in rozhraní API verze 1.2|  
|-------------|----------------------------------------------|---------------------------------------------|  
|Přidat řešení do SCC|SccInitialize()<br /><br /> SccGetProjPath()<br /><br /> SccGetProjPath()<br /><br /> SccOpenProject()|SccInitialize()<br /><br /> SccGetProjPath()<br /><br /> SccCreateSubProject()<br /><br /> SccCreateSubProject()<br /><br /> SccOpenProject()|  
|Přidání projektu řízenou zdroj řešení|SccGetProjPath()<br /><br /> OpenProject()|SccGetParentProjectPath()<br /><br /> SccOpenProject() **Poznámka:** Visual Studio předpokládá, že je řešení přímými podřízenými sursaft|  
  
## <a name="examples"></a>Příklady  
 V následující tabulce jsou uvedeny dva příklady. V obou případech [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] uživatel vyzván k cílové umístění pro řešení ve správě zdrojového kódu, dokud *user_choice* je zadán jako cíl. Pokud je zadána user_choice, se přidají dva projekty a řešení bez výzvy pro uživatele pro zdroj ovládacího prvku cílů.  
  
|Řešení obsahuje|Na disku umístění|Struktura výchozí databáze|  
|-----------------------|-----------------------|--------------------------------|  
|sln1.sln<br /><br /> Server web1<br /><br /> Web2|C:\Solutions\sln1<br /><br /> C:\Inetpub\wwwroot\Web1<br /><br /> \\\server\wwwroot$\web2|$/*user_choice*/sln1<br /><br /> $/*user_choice*  /C/serveru Web1<br /><br /> $/*user_choice*/Web2|  
|sln1.sln<br /><br /> Server web1<br /><br /> Win1|C:\Solutions\sln1<br /><br /> D:\Inetpub\wwwroot\Web1<br /><br /> C:\solutions\sln1\Win1|$/*user_choice*/sln1<br /><br /> $/*user_choice*  /D/serveru web1<br /><br /> $/*user_choice*  /sln1/win1|  
  
 SUR složce a jejích podsložkách se vytvoří bez ohledu na to, zda operace byla zrušena nebo nezdaří z důvodu chyby. Nejsou automaticky odstraňovány v podmínkách zrušit nebo chyba.  
  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]výchozí chování verze 1.1, pokud modul plug-in správy zdroje nevrátí `SCC_CAP_CREATESUBPROJECT` a `SCC_CAP_GETPARENTPROJECT` příznaky schopnosti. Kromě toho uživatelé [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] můžete se vrátit k chování verze 1.1 podle nastavení tyto klíče na hodnotu DWORD: 00000001:  
  
 [HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl] "DoNotCreateSolutionRootFolderInSourceControl" = dword: 00000001  
  
## <a name="see-also"></a>Viz také  
 [Co je nového v zdroj ovládacího prvku modulu Plug-in rozhraní API verze 1.2](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)