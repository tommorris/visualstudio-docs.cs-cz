---
title: "Návrhář aktivity TryCatch | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- System.Activities.Statements.TryCatch.UI
- System.Activities.Statements.Catch`1.UI
ms.assetid: 02a326c2-4009-442f-b7cb-e42121fd2992
caps.latest.revision: "8"
author: ErikRe
ms.author: erikre
manager: erikre
ms.openlocfilehash: a00afe1ac5e0eda29378a439398bc6bd4d90e71b
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="trycatch-activity-designer"></a>Návrhář aktivity TryCatch
**TryCatch** Návrhář aktivity se používá k vytvoření a konfigurace <xref:System.Activities.Statements.TryCatch> aktivity.  
  
## <a name="the-trycatch-activity"></a>TryCatch aktivity  
 <xref:System.Activities.Statements.TryCatch> Obsahuje aktivitu <xref:System.Activities.Statements.TryCatch.Try%2A> aktivity, kolekce **Catch\<TException >** a <xref:System.Activities.Statements.TryCatch.Finally%2A> aktivity. A <xref:System.Activities.Statements.Catch%601> typu **TException** obsahuje <xref:System.Activities.Statements.Catch%601.ExceptionType%2A> a <xref:System.Activities.Statements.Catch%601.Action%2A>. Společně se používají k implementaci typické chybu na základě výjimky mechanismu pro zpracování. A <xref:System.Activities.Statements.TryCatch> aktivity se pokusí provést jeho <xref:System.Activities.Statements.TryCatch.Try%2A> aktivity. Pokud <xref:System.Activities.Statements.TryCatch.Try%2A> aktivity výjimku, <xref:System.Activities.Statements.TryCatch> aktivita používá jeho **Catch < TException\>**  kolekce tak, aby odpovídaly výjimku. Pokud není nalezena shoda, pak se <xref:System.Activities.Statements.Catch%601.Action%2A> k odpovídající položce **Catch\<TException >** proveden, slouží jako chyba zpracování logiku pro výjimku. Pokud aktivity v <xref:System.Activities.Statements.TryCatch.Try%2A> části úspěšně dokončit nebo aktivity v <xref:System.Activities.Statements.TryCatch.Catches%2A> úspěšně dokončit, <xref:System.Activities.Statements.TryCatch> aktivita provede jeho <xref:System.Activities.Statements.TryCatch.Finally%2A> aktivity. [! ZAHRNOUT[crdefault](/dotnet/framework/windows-workflow-foundation/exceptions).  
  
### <a name="using-the-trycatch-activity-designer"></a>Pomocí návrháře TryCatch aktivity  
 **TryCatch** Návrhář aktivity naleznete v **zpracování chyb** kategorii **sada nástrojů**, který přistupuje kliknutím **sady nástrojů** karty na levé straně [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] (případně vyberte možnost **nástrojů** z **zobrazení** nabídky nebo řadič + ALT + X.)  
  
 **TryCatch** Návrhář aktivity můžete přetáhnout z **sada nástrojů** a vynechaných na [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] prostor kdekoli aktivity jsou obvykle umístěny, například jako uvnitř <xref:System.Activities.Statements.Sequence>. Tím se vytvoří <xref:System.Activities.Statements.TryCatch> aktivitu výchozí <xref:System.Activities.Activity.DisplayName%2A> z TryCatch. <xref:System.Activities.Activity.DisplayName%2A> Hodnota se dá upravit v hlavičce **TryCatch** Návrhář aktivity nebo v **DisplayName** pole mřížku vlastností. Ostatní vlastnosti musí být upravit na povrch **TryCatch** Návrhář aktivity.  
  
 Klikněte na tlačítko Rozšířené v pravém horním rohu **TryCatch** designer, ve kterém najdete v části **zkuste**, **zachytí**, a **nakonec** oknech Rozšířené zobrazení. Chcete-li přidat catch, klikněte na tlačítko **přidat nové catch** na tlačítko **TryCatch** designer. Tlačítko změny typu pole se seznamem. Vyberte typ výjimky a stiskněte klávesu ENTER, chcete-li přidat catch. Po přidání **Catch**, rozšíří oblasti catch a aktivity může být přetažen do catch k definování provádění logiku pro catch. Upozorňujeme, že se na pravé straně oblasti rozšířené catch textové pole. Můžete pojmenovat proměnnou výjimky pomocí tohoto textového pole. Výjimka proměnné lze použít pouze pro aktivity v rámci stejné **Catch**.  
  
 **TryCatch** designer nepodporuje úpravy **Catch**. Pokud chcete změnit typ výjimky, je nutné odstranit **Catch** a přidat nový. A **Catch** odstraníte jeho výběrem a odstranění nebo pomocí **odstranit** nabídky v místní nabídce přístup kliknutím pravým tlačítkem.  
  
### <a name="the-trycatch-properties"></a>Vlastnosti TryCatch  
 Následující tabulce je zobrazena <xref:System.Activities.Statements.TryCatch>vlastnosti a popisuje, jak se používají v návrháři.  
  
|Název vlastnosti|Požadováno|Použití|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Určuje nepovinné popisný název <xref:System.Activities.Statements.TryCatch> aktivity. Výchozí hodnota je TryCatch.|  
|<xref:System.Activities.Statements.TryCatch.Try%2A>|False|Aktivity nejprve provést, když <xref:System.Activities.Statements.TryCatch> provede.|  
|<xref:System.Activities.Statements.TryCatch.Catches%2A>|False|Kolekce **Catch** elementy, aby kontrolovat, když <xref:System.Activities.Statements.TryCatch.Try%2A> aktivity vyvolá výjimku.<br /><br /> Přidáte potřebovat alespoň jedné aktivity v <xref:System.Activities.Statements.TryCatch.Catches%2A> nebo aktivitu v <xref:System.Activities.Statements.TryCatch.Finally%2A> bloku.|  
|<xref:System.Activities.Statements.TryCatch.Finally%2A>|False|Aktivity při spuštění <xref:System.Activities.Statements.TryCatch.Try%2A> a všechny nezbytné aktivit v <xref:System.Activities.Statements.TryCatch.Catches%2A> dokončení provádění kolekce.<br /><br /> Přidáte potřebovat alespoň jedné aktivity v <xref:System.Activities.Statements.TryCatch.Catches%2A> nebo aktivitu v <xref:System.Activities.Statements.TryCatch.Finally%2A> bloku.|  
  
## <a name="see-also"></a>Viz také  
 [Kolekce](../workflow-designer/collection-activity-designers.md)   
 [Opětovné](../workflow-designer/rethrow-activity-designer.md)   
 [Throw](../workflow-designer/throw-activity-designer.md)