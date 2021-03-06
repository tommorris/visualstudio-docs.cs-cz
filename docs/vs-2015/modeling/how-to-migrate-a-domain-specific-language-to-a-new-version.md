---
title: 'Postupy: migrace jazyka specifického pro doménu na novou verzi | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6a1ae073-443e-45ca-8bc9-9b944362b449
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 1d97e0204122e6dfcae89da7b04a0a303a0bd9a4
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/05/2018
ms.locfileid: "43774698"
---
# <a name="how-to-migrate-a-domain-specific-language-to-a-new-version"></a>Postupy: Migrace jazyka specifického pro doménu na novou verzi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [postupy: migrace jazyka specifického pro doménu na novou verzi](https://docs.microsoft.com/visualstudio/modeling/how-to-migrate-a-domain-specific-language-to-a-new-version).  
  
Můžete migrovat projekty, které definice a používání jazyka specifického pro doménu na [!INCLUDE[vs2010](../includes/vs2010-md.md)] oproti verzi [!INCLUDE[dsl](../includes/dsl-md.md)] , který byl distribuován s [!INCLUDE[vs_orcas_long](../includes/vs-orcas-long-md.md)].  
  
 Nástroj pro migraci se poskytuje jako součást [!INCLUDE[vssdk_current_long](../includes/vssdk-current-long-md.md)]. Tento nástroj převede [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] projekty a řešení, které používají nebo definovat nástroje DSL.  
  
 Nástroj pro migraci musíte spustit explicitně: se nespustí automaticky při otevření řešení v [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Nástroje a dokument obsahuje podrobné pokyny najdete v této cestě:  
  
 **%Program Files%\Microsoft Visual Studio 2010 SDK\VisualStudioIntegration\Tools\DSLTools\DslProjectsMigrationTool.exe**  
  
## <a name="before-you-migrate-your-dsl-projects"></a>Před migraci vašich projektů DSL  
 Nástroj pro migraci změní [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] soubory projektu (**.csproj**) a soubory řešení (**.sln**).  
  
#### <a name="to-prepare-projects-for-migration"></a>Příprava migrace projektů.  
  
-   Ujistěte se, **.csproj** a **.sln** lze zapisovat soubory. Pokud jsou pod správou zdrojových kódů, ujistěte se, že jsou rezervovány.  
  
-   Vytvořte kopii složky, které máte v úmyslu migrovat.  
  
## <a name="migrating-a-collection-of-projects"></a>Migrace kolekce projektů  
  
#### <a name="to-migrate-dsl-projects-and-solutions-to-visual-studio-2010"></a>K migraci DSL projekty a řešení pro Visual Studio 2010  
  
1.  Spusťte nástroj pro migraci DSL.  
  
    -   Můžete dvakrát klikněte na panel nástrojů v Průzkumníku Windows (nebo Průzkumníka souborů) nebo spusťte nástroj z příkazového řádku. Tento nástroj je v tomto umístění:  
  
         **%ProgramFiles%\Microsoft Visual Studio 2010 SDK\VisualStudioIntegration\Tools\DSLTools\DslProjectsMigrationTool.exe**  
  
2.  Zvolte složku, která obsahuje řešení a projekty, které chcete převést.  
  
    -   Zadejte cestu do pole v horní části stránky nástroje, nebo klikněte na tlačítko **Procházet**.  
  
     Nástroj pro migraci zobrazí strom projektů, které definují nebo použijte DSL. Každý projekt, který používá zahrnuje stromu **Microsoft.VisualStudio.Modeling.Sdk** nebo **TextTemplating** sestavení.  
  
3.  Kontrola stromu projektů a zrušte zaškrtnutí políčka projekty, které nechcete převést.  
  
    -   Vyberte projekt nebo řešení zobrazíte seznam změn, které způsobí, že nástroj.  
  
        > [!NOTE]
        >  Zaškrtávací políčka, které se zobrazují vedle názvu složky nemají žádný vliv. Je třeba rozbalit složky ke kontrole projekty a řešení.  
  
4.  Převod projektů.  
  
    1.  Klikněte na tlačítko **převést**.  
  
         Před každý soubor projektu je převést, kopie _projektu_**.csproj** budou uloženy jako _projektu_**. vs2008.csproj**  
  
         Kopírování jednotlivých _řešení_**.sln** budou uloženy jako _řešení_**. vs2008.sln**  
  
    2.  Prozkoumejte všechny neúspěšné převody, které jsou hlášeny.  
  
         V textovém okně jsou hlášeny chyby. Kromě toho stromové zobrazení ukazuje rvená vlaječka v každém uzlu, který se nepovedlo převést. Můžete kliknout na uzel, který má získat další informace o této chybě.  
  
5.  **Transformovat všechny šablony** v řešení obsahující úspěšně převeden projekty.  
  
    1.  Otevřete řešení.  
  
    2.  Klikněte na tlačítko **Transformovat všechny šablony** tlačítko v hlavičce Průzkumníku řešení.  
  
        > [!NOTE]
        >  Tento krok můžete provést zbytečné. Další informace najdete v tématu [jak automatizovat Transformovat všechny šablony](http://msdn.microsoft.com/en-us/b63cfe20-fe5e-47cc-9506-59b29bca768a).  
  
6.  Aktualizujte váš vlastní kód v projektech převedený.  
  
    -   Pokus o sestavení projektů a prozkoumejte všechny chyby.  
  
    -   Otestujte návrháře.  
  
## <a name="see-also"></a>Viz také  
 [Co je nového v produktu Visualization and Modeling SDK](../misc/what-s-new-in-visualization-and-modeling-sdk.md)



