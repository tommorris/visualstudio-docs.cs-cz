---
title: "Získání sestavení protokoly pomocí nástroje MSBuild | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- MSBuild, logging
- logging [MSBuild]
ms.assetid: 6ba9a754-9cc0-4fed-9fc8-4dcd3926a031
caps.latest.revision: "27"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: cd7e50a44e5d53653f233372b643c31fe58aedc9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="obtaining-build-logs-with-msbuild"></a>Získávání protokolů o sestavení pomocí nástroje MSBuild
Pomocí nástroje MSBuild pomocí přepínačů, můžete zadat kolik dat sestavení, které chcete zkontrolovat a zda chcete uložit data sestavení na jeden nebo více souborů. Můžete také zadat vlastní protokolovacího nástroje ke shromažďování dat sestavení. Informace o parametrech příkazového řádku nástroje MSBuild, které nezahrnuje v tomto tématu najdete v tématu [Reference k příkazovému řádku](../msbuild/msbuild-command-line-reference.md).  
  
> [!NOTE]
>  Pokud vytvoříte projektů pomocí prostředí Visual Studio IDE, můžete tyto sestavení řešit kontrolou protokolů o sestavení. Další informace najdete v tématu [postupy: zobrazení, ukládání a konfigurace souborů protokolu sestavení](../ide/how-to-view-save-and-configure-build-log-files.md).  
  
## <a name="setting-the-level-of-detail"></a>Nastavení úrovně podrobností  
 Při sestavování projektu pomocí nástroje MSBuild bez zadání úroveň podrobností, v protokolu výstupu se zobrazí následující informace:  
  
-   Chyby, upozornění a zprávy, které jsou klasifikovány jako vysoce důležité.  
  
-   Některé události stavu.  
  
-   Souhrn sestavení.  
  
 Pomocí **/verbosity** (**/v**) přepínat, můžete určit, kolik dat zobrazena v výstup protokolu. Při řešení potíží použijte úroveň podrobností buď `detailed` (`d`) nebo `diagnostic` (`diag`), který poskytuje nejvíc informace.  
  
 Procesu sestavení může být pomalejší, při nastavení **/verbosity** k `detailed` a pomalejší, i když nastavíte **/verbosity** k `diagnostic`.  
  
```  
msbuild MyProject.proj /t:go /v:diag  
```  
  
## <a name="saving-the-build-log-to-a-file"></a>Uložení protokolu sestavení do souboru  
 Můžete použít **/fileLogger** (**fl**) přepínače k uložení dat sestavení do souboru. Následující příklad uloží data sestavení do souboru, který je pojmenován `msbuild.log`.  
  
```  
msbuild MyProject.proj /t:go /fileLogger  
```  
  
 V následujícím příkladu je název souboru protokolu `MyProjectOutput.log`, a podrobností protokolu výstupu je nastavena na `diagnostic`. Zadejte tyto dvě nastavení pomocí **/filelogparameters** (`flp`) přepínače.  
  
```  
msbuild MyProject.proj /t:go /fl /flp:logfile=MyProjectOutput.log;verbosity=diagnostic  
```  
  
 Další informace najdete v tématu [Reference k příkazovému řádku](../msbuild/msbuild-command-line-reference.md).  
  
## <a name="saving-the-log-output-to-multiple-files"></a>Uložení výstupu protokolování do více souborů  
 Následující příklad uloží celý protokolu, který chcete `msbuild1.log`, jenom chyby, k `JustErrors.log`a pouze upozornění na `JustWarnings.log`. Příklad používá soubor čísla pro všechny tři soubory. Soubor čísla, která jsou určené jenom po **/fl** a **/flp** přepínače (například `/fl1` a `/flp1`).  
  
 **/Filelogparameters** (`flp`) přepne pro soubory 2 a 3 zadejte co název každého souboru a co chcete zahrnout do každého souboru. Není zadán žádný název souboru 1, takže výchozí název `msbuild1.log` se používá.  
  
```  
msbuild MyProject.proj /t:go /fl1 /fl2 /fl3 /flp2:logfile=JustErrors.log;errorsonly /flp3:logfile=JustWarnings.log;warningsonly  
  
```  
  
 Další informace najdete v tématu [Reference k příkazovému řádku](../msbuild/msbuild-command-line-reference.md).  
  
## <a name="using-a-custom-logger"></a>Používání vlastního protokolovacího nástroje  
 Můžete napsat vlastní protokoly vytvářením spravovaný typ, který implementuje <xref:Microsoft.Build.Framework.ILogger> rozhraní. Můžete například použít vlastní protokoly, odešlete chyby sestavení v e-mailu, přihlaste se k databázi nebo protokolu je do souboru XML. Další informace najdete v tématu [Protokolovací nástroje sestavení](../msbuild/build-loggers.md).  
  
 V příkazovém řádku MSBuild, zadejte vlastní protokoly pomocí **/logger** přepínače. Můžete také **/noconsolelogger** přepínač tak, aby zakázat výchozí konzoly protokolovač.  
  
## <a name="see-also"></a>Viz také  
 <xref:Microsoft.Build.Framework.LoggerVerbosity>   
 [Protokolovací nástroje sestavení](../msbuild/build-loggers.md)   
 [Protokolování v prostředí s více procesory](../msbuild/logging-in-a-multi-processor-environment.md)   
 [Vytváření předávání protokolovacích nástrojů](../msbuild/creating-forwarding-loggers.md)   
 [Koncepty nástroje MSBuild](../msbuild/msbuild-concepts.md)