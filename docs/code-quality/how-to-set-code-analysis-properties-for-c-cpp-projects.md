---
title: "Postupy: nastavení vlastností analýzy kódu pro projekty C/C++ | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.codeanalysis.propertypages.native
- VC.Project.VCCLCompilerTool.EnablePrefast
- VC.Project.VCFxCopTool.EnablePREfast
- VC.Project.VCFxCopTool.IgnoreGeneratedCode
helpviewer_keywords:
- properties, C/C++ Code Analysis
- properties, Code Analysis
- code analysis properties
- C/C++ code analysis properties
ms.assetid: 7af52097-6d44-4785-9b9f-43b7a7d447d7
caps.latest.revision: "17"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: b2ad22eccb561bf58ee845d58268620aad778a20
ms.sourcegitcommit: fb751e41929f031d1a9247bc7c8727312539ad35
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2017
---
# <a name="how-to-set-code-analysis-properties-for-cc-projects"></a>Postupy: Nastavení vlastností analýzy kódu pro projekty C/C++
Můžete nakonfigurovat pravidla, které používá nástroj pro analýzu kódu k analýze kódu v každé konfiguraci vašeho projektu. Kromě toho můžete nastavit analýzy kódu pro potlačení upozornění z kódu, které se generují a přidávají do projektu pomocí nástroje třetích stran.  
  
## <a name="code-analysis-property-page"></a>Stránka vlastností analýzy kódu  
 **Analýza kódu** stránka vlastností obsahuje všechna nastavení konfigurace analýzy kódu pro projekt. Otevřete stránku vlastností analýzy kódu pro projekt v **Průzkumníku řešení**, klikněte pravým tlačítkem na projekt a pak klikněte na tlačítko **vlastnosti**. Potom rozbalte **vlastnosti konfigurace** a vyberte **analýza kódu** kartě.  
  
## <a name="project-configuration-and-platform"></a>Konfigurace projektu a platforma  
 **Konfigurace** seznamu a **platformy** seznamu umožňují používat nastavení analýzy kódu pro různé kombinace parametrů konfigurace a platformy jiný projekt. Můžete například nastavit analýzy kódu pro použití jedné sady pravidel projektu pro ladění sestavení a jinou sadu pro verzi sestavení.  
  
## <a name="enabling-code-analysis"></a>Povolení analýza kódu  
 Můžete rozhodnout, jestli se má povolit analýzy kódu pro váš projekt tak, že vyberete **povolit kód analýzy pro C/C++ v sestavení**. V kombinaci s **konfigurace** seznamu, se může například rozhodnete zákaz analýzy kódu pro sestavení pro ladění a povolit ho pro verzi sestavení.  
  
 Pokud projekt obsahuje spravovaného kódu, můžete se rozhodnout, zda chcete povolit nebo zakázat analýza kódu tak, že vyberete **povolit analýza kódu v sestavení**.  
  
 Analýza kódu slouží ke zlepšení kvality kódu a vyhnout se běžné nástrahy. Proto pečlivě zvažte, jestli se má zákaz analýzy kódu. Je obvykle lepší zakázat sady pravidel nebo jednotlivých pravidel, které nechcete použít do projektu.  
  
## <a name="generated-code"></a>Generovaný kód  
 Vývojáři často pomocí nástroje vám pomůžou s vývojem aplikací rychle. Tyto nástroje mohou generovat kód, který je přidán do projektu. Můžete chtít najdete v části porušení pravidel, které zjistí analýza kódu generovaného kódu. Nemusí ale chcete zobrazovat v případě, že nechcete udržovat kód.  
  
 **Potlačit výsledky z vygeneruje kód** v zaškrtávací políčko **Obecné** vlastnosti stránky lze vybrat, zda chcete zobrazit upozornění analýzy kódu ze spravovaného kódu, který je generovaný nástroj třetí strany .  
  
## <a name="rule-sets"></a>Sady pravidel  
 Pokud projekt obsahuje spravovaného kódu, můžete vybrat pravidla pro použití v analýza kódu tak, že vyberete sadu z pravidel **spuštění této sady pravidel** seznamu.  
  
## <a name="see-also"></a>Viz také  
 [Analýza kvality spravovaného kódu](../code-quality/analyzing-managed-code-quality-by-using-code-analysis.md)   
 [Analýza kódu pro C/C++ upozornění](../code-quality/code-analysis-for-c-cpp-warnings.md)