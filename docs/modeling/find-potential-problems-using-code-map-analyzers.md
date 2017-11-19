---
title: "Nalezení potenciálních problémů pomocí analyzátorů mapy kódu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: get-started-article
f1_keywords: vs.progression.codemapanalyzers
helpviewer_keywords:
- code analysis, dependency graphs
- dependency graphs, analyzing code
- graph documents, analyzing
ms.assetid: 9dd799a7-f7eb-42ff-8612-b19dde7ff4eb
caps.latest.revision: "11"
author: alexhomer1
ms.author: ahomer
manager: douge
ms.openlocfilehash: d2ac6ceed6f2d32eb347db89e0a329331e61b937
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="find-potential-problems-using-code-map-analyzers"></a>Nalezení potenciálních problémů pomocí analyzátorů mapy kódu
Spustili analyzátorů mapy kódu, který vám pomůže identifikovat kód, který může být příliš složité nebo která potřebujete zlepšování. Například můžete použít tyto analyzátorů:  
  
|**Najít kód, který má**|**Prozkoumat tyto oblasti zobrazíte zda**|  
|-------------------------------|--------------------------------------------|  
|Smyčky nebo cyklické závislosti|Můžete je zjednodušit a zvažte, zda lze rozdělit tyto cykly.|  
|Příliš velký počet závislostí|Provádění příliš mnoho funkcí nebo zjistit dopad změny těchto oblastí. Minimální počet závislostí se zobrazí mapě kódu ve správném formátu. Abyste mohli snadněji spravovat, změnit, testování a znovu použít, zvažte, jestli Refaktorovat těchto oblastem tak, aby se více jasně definované, nebo jestli můžete sloučit kód, který provádí podobné funkce jako kód.|  
|Žádné závislosti|Jsou zapotřebí nebo jestli byste měli odebrat tento kód.|  
  
## <a name="analyze-code-maps"></a>Analýza mapy kódu  
  
1.  Na panelu nástrojů mapy zvolte **rozložení**, **analyzátorů**a pak analyzátor, který chcete spustit:  
  
    |**Analyzátor**|**K identifikaci uzlů,**|  
    |------------------|--------------------------------|  
    |**Analyzátor cyklické odkazy**|Cyklické závislosti jsou na sobě navzájem. **Poznámka:** cyklické závislosti, které jsou v **obecné typy** skupiny nejsou zobrazeny na mapě. když rozbalte skupinu.|  
    |**Najít analyzátor rozbočovače**|Jsou v horní 25 % vysoce připojené uzlů<br /><br /> **Chcete-li skrýt všechny uzly na mapě**<br /><br /> -Otevřete místní nabídky pro mapu, zvolte **Upřesnit**, **vyberte**, **skrýt nezaškrtnuté**.<br />     Mapy skryje nezaškrtnuté uzlů a nástroje analyzer identifikuje nové uzly jako rozbočovače.|  
    |**Analyzátor neregistrované uzly**|Nemají odkazy z jiných uzlů. **Upozornění:** ověření jednotlivých případech před za předpokladu, že kód nepoužívá. Určité závislosti, jako je například XAML závislosti a závislosti běhu nebyl nalezen staticky v kódu.|  
  
 Analyzátorů mapy kódu se bude nadále spouštět po jejich použití. Pokud změníte mapy, všechny použité analyzátorů bude automaticky znovu zpracovat aktualizovanou mapy. Zastaví analyzátor, na panelu nástrojů mapy, zvolte **rozložení**, **analyzátorů**. Vypněte vybrané analyzátor.  
  
> [!TIP]
>  Pokud máte velké mapy, spuštění analyzátor může způsobit nedostatku paměti výjimky. Pokud k tomu dojde, upravte mapování omezit její obor nebo vygenerovat menší a pak spustit Analyzátor.  
  
## <a name="see-also"></a>Viz také  
 [Mapování závislostí napříč vaším řešením](../modeling/map-dependencies-across-your-solutions.md)   
 [Použití map kódu k ladění aplikací](../modeling/use-code-maps-to-debug-your-applications.md)   
 [Mapování metod v zásobníku volání při ladění](../debugger/map-methods-on-the-call-stack-while-debugging-in-visual-studio.md)