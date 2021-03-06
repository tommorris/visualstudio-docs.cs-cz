---
title: Balení a nasazení řešení služby SharePoint | Microsoft Docs
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- packaging [SharePoint development in Visual Studio]
- deploying [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, packaging and deploying
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 2421a1f39f2969563bc10a43367936ae499fac30
ms.sourcegitcommit: d9e4ea95d0ea70827de281754067309a517205a1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2018
ms.locfileid: "37120204"
---
# <a name="package-and-deploy-sharepoint-solutions"></a>Zabalení a nasazení řešení služby SharePoint
  Obvykle řešení služby SharePoint je nasazený na serveru služby SharePoint pomocí souboru balíčku (WSP) řešení. Visual Studio můžete použít k uspořádání vaší SharePoint – položky projektu do funkcí a chcete-li vytvořit balíček pro nasazení vaší funkcí služby SharePoint.  
  
 Toto téma poskytuje následující informace:  
  
-   [Vytváření funkcí a balíčků](#Creating)  
  
-   [Funkce a balení nástroj podpory](#Tools)  
  
-   [Nasazení řešení služby SharePoint](#Deploying)  
  
-   [Nasazení souborů v řešení služby SharePoint](#DeployingFiles)  
  
## <a name="create-features-and-packages"></a>Vytváření funkcí a balíčků
 Visual Studio můžete použít k seskupení souvisejících prvků služby SharePoint do *funkce*. Funkce pro definici seznamu kontaktů může obsahovat třeba instanci seznamu a definice seznamu. Tyto dva prvky můžete zkombinovat do jednoho funkce pro účely nasazení. Další informace o funkcích najdete v tématu [stavebním blokem: funkce](http://go.microsoft.com/fwlink/?LinkID=169183).  
  
 Dále můžete vytvoření balíčku řešení služby SharePoint (*WSP*) sady více funkcí, lokality do jednoho balíčku, který ukládá soubory ve formátu vyžaduje SharePoint nasadit soubory do definice sestavení a další soubory server. Další informace najdete v tématu [stavebním blokem: řešení](http://go.microsoft.com/fwlink/?LinkID=169186).  
  
## <a name="feature-and-packaging-tool-support"></a>Funkce a podpory nástroje balení
 Nástroje pro vývoj pro SharePoint v sadě Visual Studio vám pomůže rychle uspořádání souborů služby SharePoint do funkcí a řešení balíčky pro nasazení jednodušší. Tyto nástroje můžete nakonfigurovat balíček funkcí a řešení.  
  
-   Funkce Designer a návrháře balíčků.  
  
-   Průzkumníku balíčků, okno nástroje.  
  
-   Průzkumník řešení.  
  
### <a name="feature-designer-and-package-designer"></a>Funkce designer a návrháře balíčků
 Můžete vytvořit funkce, nastavení rozsahů a označit další funkce, jako závislosti pomocí návrháře funkce. Návrhář také zobrazí poslední souboru XML, který popisuje každou funkci. Další informace najdete v tématu [funkcí služby SharePoint vytvořit](../sharepoint/creating-sharepoint-features.md).  
  
 Použijte funkci k určitému webu nebo skupinu webů tak, že nastavení jeho *oboru* v Návrháři funkce. Pokud je zapnuta pro jednotlivé webové stránky, tato funkce funguje jen v této určitého webového serveru. Pokud je zapnuta pro kolekci webů, položky ve funkci se vztahují ke kolekci celý web. Další informace najdete v tématu [Element oboru](http://go.microsoft.com/fwlink/?LinkID=169189).  
  
 Pokud vaše funkce závisí na jiné funkce, můžete nastavit *funkci aktivace závislost* označit závislé součásti před zpřístupněním vaší funkce. Závislost aktivace funkce zkontroluje, pokud jsou v tomto oboru již aktivován závislé součásti. Další informace najdete v tématu [aktivace závislosti a oboru](http://go.microsoft.com/fwlink/?LinkID=169190).  
  
 V Návrháři balíček můžete seskupit prvky služby SharePoint do jednoho řešení balíčku a nakonfigurovat, zda chcete-li obnovit webový server během nasazení. Pokud chcete nastavit typ nasazení serveru, použijte **vlastnosti** okno. Návrhář také vytvoří soubor XML, který popisuje obsah balíčku. Další informace najdete v tématu [balíčků řešení služby SharePoint vytvořit](../sharepoint/creating-sharepoint-solution-packages.md).  
  
 Během nasazení službu Internetové informační služby (IIS) je zastavena zkopírovat soubory řešení na serveru SharePoint. Pomocí návrháře balíčků v sadě Visual Studio, můžete určit, zda má webový server restartovat. Pokud chcete konfigurovat, pokud je řešení nasazeno na front-end webovém serveru nebo aplikační server, použijte **vlastnosti** okno. Další informace najdete v tématu [prvek řešení (řešení)](http://go.microsoft.com/fwlink/?LinkID=169191).  
  
### <a name="packaging-explorer"></a>Průzkumníku balíčků  
 Aby doplňovala funkce Designer a návrháře balíčků, můžete v Průzkumníku balíčků seskupit soubory služby SharePoint do funkcí a balíčků. Kromě toho se zobrazí hierarchické zobrazení projektu služby SharePoint balíčku, funkce, položky a soubory. Průzkumníku balíčků je okno nástroje, který vám pomůže dokončit následující úlohy:  
  
-   Otevřete položky projektu služby SharePoint a soubory.  
  
-   Přetahování položek projektu služby SharePoint z jednu funkci do jiného.  
  
-   Přetahování položek projektu služby SharePoint a funkce z jeden balíček do jiného.  
  
-   Přidejte novou funkci balíčku.  
  
-   Otevřete návrháře funkce nebo balíčku.  
  
-   Ověřte funkce a balíčky.  
  
 Nástroje pro vývoj pro SharePoint v sadě Visual Studio mít pravidel ověřování k zajištění, že je správně vytvořen balíčku řešení. Kromě toho pravidla ověřte, zda *WSP* soubor řešení můžete úspěšně nasazen a aktivovat na serveru služby SharePoint. Další informace o schématu XML pro funkce, najdete v tématu [funkce schémata](http://go.microsoft.com/fwlink/?LinkID=169192).  
  
 V systému projektu služby SharePoint můžete přidat vlastní funkce a pravidel ověřování balíčku. Další informace najdete v tématu [postupy: vytvoření vlastní funkce a balíček ověřovacích pravidel pro řešení služby SharePoint](../sharepoint/how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions.md).  
  
 Další informace o Průzkumníku balíčků najdete v tématu [postupy: Přidání nebo odebrání funkcí a položek z balíku pomocí Průzkumníku balíčků](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-packaging-explorer.md).  
  
### <a name="solution-explorer"></a>Průzkumník řešení
 Procházejte a otevřít soubory projektu služby SharePoint můžete Průzkumníku řešení. Použít místní nabídky v Průzkumníku řešení pro přidání funkcí, přijímačů událostí funkce a funkce prostředky. Kromě toho můžete otevřít funkce návrhářů a návrháři balíček ke konfiguraci funkce a balíčky pro nasazení.  
  
## <a name="deploy-sharepoint-solutions"></a>Nasazení řešení služby SharePoint
 Po přizpůsobení funkcí a balíčku v sadě Visual Studio, můžete vytvořit *WSP* souboru k nasazení na servery služby SharePoint. Visual Studio můžete použít pro ladění a testování. *wsp* pouze na serveru SharePoint na vývojovém počítači. Další informace o tom, jak nasadit řešení služby SharePoint na vzdálený server služby SharePoint, naleznete v části [nasazení řešení](http://go.microsoft.com/fwlink/?LinkID=169194).  
  
 Můžete také upravit jednotlivé kroky nasazení na vývojovém počítači. Další informace najdete v tématu [nasazení, publikování a upgradování balíčků řešení služby SharePoint](../sharepoint/deploying-publishing-and-upgrading-sharepoint-solution-packages.md).  
  
## <a name="deploy-files-in-sharepoint-solutions"></a>Nasazení souborů v řešení služby SharePoint
 Obvykle když přidáte položky projektu služby SharePoint do řešení služby SharePoint, všechny požadované soubory jsou zahrnuty. Soubory, které mohou být zkompilovány (soubory kódu) jsou integrované ve výstupu sestavení řešení. Však možná budete také muset přidat-kompilační soubory, například *.xml*, *.txt*, nebo soubory prostředků, do projektu služby SharePoint. Tyto soubory nejsou zabalené automaticky ve vašem řešení. Aby se zajistilo, že přitom se zabalí, buď přidejte soubory do mapované složky nebo do položky projektu služby SharePoint.  
  
 Soubory přidány do mapované složky se automaticky zkopírují do podregistr služby SharePoint, když je řešení nasazeno. Soubory přidané do položky projektu služby SharePoint se nasadí do umístění, které je zadáno v **umístění nasazení** na základě vlastnosti pro každý soubor, který je částečně nastaven **typ nasazení** vlastnost. Ve výchozím nastavení **typ nasazení** hodnota vlastnosti je **NoDeployment**, což znamená, že soubor není nasazený s řešením. Je nutné nastavit jinou hodnotu pro vlastnost, zahrnout soubor v balíčku.  
  
 Chcete-li například přidat *.xml* soubor do projektu služby SharePoint, proveďte jednu z těchto akcí:  
  
-   Do projektu přidejte složku namapované "Rozložení" služby SharePoint. Tím se vytvoří v **Průzkumníku řešení** složku s názvem **rozložení** má podsložku pro projekt. Přidat *.xml* soubor do nové složky. Ve výchozím nastavení, soubor se nasadí do služby SharePoint systému souborů v části *... \TEMPLATE\LAYOUTS\\\<název složky >*. Informace o tom, jak přidat mapované složky najdete v tématu [postupy: Přidání a odebrání mapovaných složek](../sharepoint/how-to-add-and-remove-mapped-folders.md).  
  
-   Přidat *.xml* souboru do složky položky projektu služby SharePoint a poté změňte **typ nasazení** vlastnost *.xml* souboru z **NoDeployment**  jiné nastavení, jako **RootFile** nebo **ElementFile**. Odpovídající **typ nasazení** nastavení závisí na soubor a projekt. Další informace o **typ nasazení** najdete v části Nastavení vlastností [řešení služby SharePoint vyvíjet](../sharepoint/developing-sharepoint-solutions.md).  
  
 Pokud přidaný soubor se nevztahuje na žádné konkrétní projekty v řešení, můžete přidat prázdného projektu služby SharePoint k řešení a potom k němu přidejte další soubory. Další alternativou k nasazení soubory do služby SharePoint, zejména k databázi obsahu je do projektu přidejte modul a potom přidat soubory do modulu. Další informace najdete v tématu [použijte moduly vložení souborů do řešení](../sharepoint/using-modules-to-include-files-in-the-solution.md).  
  
## <a name="see-also"></a>Viz také:
 [Vývoj řešení služby SharePoint](../sharepoint/developing-sharepoint-solutions.md)   
 [Vytváření a ladění řešení služby SharePoint](../sharepoint/building-and-debugging-sharepoint-solutions.md)  
  
