---
title: "Vybrané připojení používá poskytovatele Nepodporovaná databáze | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 4d25dfa1-8fa4-4529-9b90-973bc2ec2993
caps.latest.revision: "3"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 956f6ab5180475bf0abb03e4353fe0343f876ae1
ms.sourcegitcommit: ee42a8771f0248db93fd2e017a22e2506e0f9404
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2017
---
# <a name="the-selected-connection-uses-an-unsupported-database-provider"></a>Vybrané připojení používá poskytovatele Nepodporovaná databáze
Tato zpráva se zobrazí při přetažení položky, které nepoužívají zprostředkovatele dat .NET Framework pro SQL Server z **Průzkumníka serveru**/**Průzkumník databáze** na [technologie LINQ to SQL Nástroje v sadě Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md).  
  
 [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)] Podporuje pouze datová připojení, které používají zprostředkovatele rozhraní .NET Framework pro SQL Server. Platné jsou pouze připojení k serveru Microsoft SQL Server nebo Microsoft SQL Server databázový soubor.  
  
### <a name="to-correct-this-error"></a>Oprava této chyby  
  
-   Přidat pouze položky z připojení dat, která pomocí zprostředkovatele dat .NET Framework pro SQL Server [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)].  
  
## <a name="see-also"></a>Viz také
<xref:System.Data.SqlClient>  
[Návrhář relací objektů zprávy](../data-tools/o-r-designer-messages.md)  
[Technologie LINQ to SQL nástroje v sadě Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)