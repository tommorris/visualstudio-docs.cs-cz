---
title: "Postupy: vytvoření a úprava konfigurací | Microsoft Docs"
ms.custom: 
ms.date: 06/21/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- solution build configurations, editing
- build configurations, creating
- solution build configurations, creating
- build configurations, editing
- builds [Visual Studio], setting up
- property pages
- Configuration Manager
- project build configurations, creating
- project build configurations, editing
ms.assetid: 19be121c-148e-4ece-bbfc-d20b08cfc3f7
caps.latest.revision: "15"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: afa939c0b8a033930f5e8e7bcc525d6f33e55f86
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-create-and-edit-configurations"></a>Postupy: Vytvoření a úprava konfigurací
Můžete vytvořit několik konfigurace sestavení řešení. Například můžete nakonfigurovat sestavení ladicí verze, která vaše testery vám pomůže najít a opravit problémy, a můžete nakonfigurovat různé druhy sestavení, které můžete distribuovat do různých zákazníků.  

 [!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]  

## <a name="creating-build-configurations"></a>Vytváření konfigurace sestavení  
 Můžete použít **nástroje Configuration Manager** dialogové okno Vybrat nebo upravit existující konfigurace sestavení, nebo můžete vytvořit nové.  

#### <a name="to-open-the-configuration-manager-dialog-box"></a>Chcete-li otevřít dialogové okno nástroje Configuration Manager  

-   V **Průzkumníku řešení**, otevřete místní nabídku pro řešení a zvolte **nástroje Configuration Manager**.  

    > [!NOTE]
    >  Pokud **nástroje Configuration Manager** příkaz se nezobrazí v místní nabídce, vyhledejte v části **sestavení** nabídky v řádku nabídek. Pokud se nezobrazí existuje buď v řádku nabídek zvolte **nástroje**, **možnosti**a potom v levém podokně **možnosti** dialogové okno, rozbalte seznam **projekty a Řešení**, **Obecné**a v pravém podokně, vyberte **zobrazit Rozšířená konfigurace sestavení** zaškrtávací políčko.  

     V **nástroje Configuration Manager** dialogové okno, můžete použít **aktivní konfigurace řešení** rozevíracího seznamu vyberte položku konfigurace sestavení řešení celou, upravit existující nebo vytvořit nový konfigurace. Můžete použít **platforma Active řešení** rozevíracího seznamu vyberte platformu, konfigurace cílí upravit existující, nebo přidat nové platformě. **Projektu kontexty** podokně zobrazí projekty v řešení. Pro každý projekt můžete vyberte platformu a konfigurace specifické pro projekt, upravit existující, nebo vytvořit novou konfiguraci nebo přidat nové platformě. Můžete také vybrat políček, která označuje, zda každý projekt zahrnuty při použití konfigurace celé řešení k sestavení nebo nasazení řešení.  

 Po nastavení konfigurace, které chcete, můžete nastavit vlastnosti projektu, které jsou vhodné pro tyto konfigurace.  

#### <a name="to-set-properties-based-on-configurations"></a>Nastavení vlastností na základě konfigurací  

-   V **Průzkumníku řešení**, otevřete místní nabídky pro projekt a zvolte **vlastnosti**.  

     **Stránky vlastností** otevře se okno.  

     Nastavení vlastností pro vaše konfigurace. Například pro konfiguraci vydání, můžete zadat, když je integrované řešení, a pro konfiguraci ladění, můžete určit, že je optimalizovaný kód `DEBUG` symbol Podmíněná kompilace je součástí. Další informace o nastavení vlastnosti stránky najdete v tématu [vlastností Správa projektů a řešení](../ide/managing-project-and-solution-properties.md).  

## <a name="creating-and-modifying-project-configurations"></a>Vytvoření a úprava konfigurace projektu  

#### <a name="to-create-a-project-configuration"></a>Pro vytvoření konfigurace projektu  

1.  Otevřete **nástroje Configuration Manager** dialogové okno.  

2.  Vyberte projekt v **projektu** sloupce.  

3.  V **konfigurace** rozevíracího seznamu pro tento projekt, vyberte **nový**.  

     **Novou konfiguraci projektu** otevře se dialogové okno.  

4.  V **název** pole, zadejte název pro novou konfiguraci.  

5.  Pro použití s nastavením vlastnosti z existující konfigurace projektu, v **Kopírovat nastavení z** rozevíracího seznamu, vyberte takovou konfiguraci.  

6.  Chcete-li vytvořit řešení celou konfiguraci ve stejnou dobu, vyberte **vytvořit novou konfiguraci řešení** zaškrtávací políčko.  

#### <a name="to-rename-a-project-configuration"></a>Chcete-li přejmenovat konfigurace projektu  

1.  Otevřete **nástroje Configuration Manager** dialogové okno.  

2.  V **projektu** sloupce, vyberte projekt, který má projektu konfiguraci, kterou chcete přejmenovat.  

3.  V **konfigurace** rozevíracího seznamu pro tento projekt, vyberte **upravit**.  

     **Upravit konfigurace projektu** otevře se dialogové okno.  

4.  Vyberte název konfigurace projektu, který chcete změnit.  

5.  Vyberte **přejmenovat**a pak zadejte nový název.  

## <a name="creating-and-modifying-solution-wide-build-configurations"></a>Vytvoření a úprava celé řešení konfigurace sestavení  

#### <a name="to-create-a-solution-wide-build-configuration"></a>Pro vytvoření konfigurace sestavení řešení celou  

1.  Otevřete **nástroje Configuration Manager** dialogové okno.  

2.  V **aktivní konfigurace řešení** rozevíracího seznamu vyberte **nový**.  

     **Novou konfiguraci řešení** otevře se dialogové okno.  

3.  V **název** textové pole, zadejte název pro novou konfiguraci.  

4.  Chcete použít nastavení z existující konfigurace řešení, v **Kopírovat nastavení z** rozevíracího seznamu, vyberte takovou konfiguraci.  

5.  Pokud chcete vytvořit konfigurace projektu ve stejnou dobu, vyberte **vytvořit nové konfigurace projektu** zaškrtávací políčko.  

#### <a name="to-rename-a-solution-wide-build-configuration"></a>Chcete-li přejmenovat řešení celé konfigurace sestavení  

1.  Otevřete **nástroje Configuration Manager** dialogové okno.  

2.  V **aktivní konfigurace řešení** rozevíracího seznamu vyberte **upravit**.  

     **Upravit konfigurace řešení** otevře se dialogové okno.  

3.  Vyberte název konfigurace řešení, které chcete změnit.  

4.  Vyberte **přejmenovat**a pak zadejte nový název.  

#### <a name="to-modify-a-solution-wide-build-configuration"></a>Ke změně konfigurace sestavení řešení celou  

1.  Otevřete **nástroje Configuration Manager** dialogové okno.  

2.  V **aktivní konfigurace řešení** rozevíracího seznamu vyberte konfigurace, kterou chcete.  

3.  V **projektu kontexty** podokně, pro každý projekt, vyberte **konfigurace** a **platformy** a vyberte ohledně **sestavení**ho a zda má být **nasadit** ho...  

## <a name="see-also"></a>Viz také  
 [Principy konfigurací sestavení](../ide/understanding-build-configurations.md)   
 [Sestavování a čištění projektů a řešení v sadě Visual Studio](../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)   
 [Správa vlastností projektů a řešení](managing-project-and-solution-properties.md)
