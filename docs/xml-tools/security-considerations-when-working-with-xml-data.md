---
title: "Aspekty zabezpečení při práci s daty XML | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: fce2b708-1aef-454f-be59-52b76f359351
caps.latest.revision: "2"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 46bd68bd4556c782ac8dc6e1664dafe0ce80f99e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="security-considerations-when-working-with-xml-data"></a>Aspekty zabezpečení při práci s daty XML
Toto téma popisuje problémy zabezpečení, které potřebujete vědět o při práci s editoru XML nebo XSLT ladicího programu.  
  
## <a name="xml-editor"></a>XML Editor  
 Editor souborů XML je založen na editoru textu sady Visual Studio. Přitom spoléhá na <xref:System.Xml> a <xref:System.Xml.Xsl> třídy pro zpracování řadu procesů XML.  
  
-   Transformace XSLT jsou spouštěny v nové doméně aplikace. Transformace XSLT jsou *v izolovaném prostoru*; to znamená, zásady zabezpečení přístupu kódu počítače slouží k určení omezená oprávnění podle toho, kde je umístěné Styl XSLT. Například šablony stylů z umístění v Internetu mít nejvíce omezená oprávnění, zatímco stylů zkopíruje na vašem pevném disku, spusťte s úplný vztah důvěryhodnosti.  
  
-   <xref:System.Xml.Xsl.XslCompiledTransform> Třída se používá ke kompilaci XSLT do převodního jazyka Microsoft pro dosažení vyššího výkonu během provádění.  
  
-   Schémata, které odkazují na externí umístění v souboru katalogu se automaticky stáhnou při poprvé načte editoru XML. <xref:System.Xml.Schema.XmlSchemaSet> Třída se používá ke kompilaci schémat. Soubor katalogu, který se dodává s editoru XML nemá odkazy na všechny externí schémat. Uživatel musí explicitně přidat odkaz na externí schéma před editoru XML soubory ke stažení souboru schématu. Stahování HTTP lze zakázat pomocí **různé možnosti v nabídce Nástroje** stránky pro Editor XML.  
  
-   Pomocí editoru XML <xref:System.Net> třídy ke stažení schémat.  
  
## <a name="xslt-debugger"></a>Ladicí program XSLT  
 Ladicí program XSLT využívá modul aplikace Visual Studio spravovaného ladění a třídy z <xref:System.Xml> a <xref:System.Xml.Xsl> oboru názvů.  
  
-   Ladicí program XSLT spustí každý transformace XSLT v doméně aplikace v izolovaném prostoru. Zásady zabezpečení přístupu kódu počítače slouží k určení omezená oprávnění podle toho, kde je umístěné Styl XSLT. Například šablony stylů z umístění v Internetu mít nejvíce omezená oprávnění, zatímco stylů zkopíruje na vašem pevném disku, spusťte s úplný vztah důvěryhodnosti.  
  
-   Styl XSLT je kompilovat, pomocí <xref:System.Xml.Xsl.XslCompiledTransform> třídy.  
  
-   Vyhodnocení výrazu XSLT je načten modulem spravované ladění. Modul spravované ladění předpokládá, že veškerý kód je spustit z místního počítače uživatele. Podle toho <xref:System.Xml.Xsl.XslCompiledTransform> třída stáhne soubor XSLT na místním počítači uživatele. Možnost, že mohlo dojít zvýšení oprávnění v provádění oprávnění zmírnit provádění všechny transformace XSLT v nové doméně aplikace s omezenými oprávněními  
  
## <a name="see-also"></a>Viz také  
 [Aplikační domény](/dotnet/framework/app-domains/application-domains)  