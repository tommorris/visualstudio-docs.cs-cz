---
title: "Různé, XML, textový Editor, dialogové okno Možnosti | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: fd3fff31-cddc-422d-a2f0-a5a1ef492afd
caps.latest.revision: "2"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 871190deb39504a498061602b11f927832d71f35
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="miscellaneous-xml-text-editor-options-dialog-box"></a>Různé, XML, textový Editor, dialogové okno Možnosti
Toto dialogové okno umožňuje změnit nastavení automatického dokončování a schématu pro Editor XML. Dostanete **možnosti** dialogové okno z **nástroje** nabídky.  
  
> [!NOTE]
>  Tato nastavení jsou k dispozici, když vyberete **textového editoru** složku, **XML** složku a potom **různé** možnost z **možnosti** dialogové okno.  
  
## <a name="auto-insert"></a>Automatické vkládání  
 **Zavřít značky**  
 Pokud automatické dokončování nastavení zaškrtnuté, editor automaticky přidá koncová značka, když zadáte pravé ostré závorky (>) zavřete úvodní značky, pokud už není uzavřený značky. Toto je výchozí chování.  
  
 Dokončení prázdný element není závislá na nastavení automatické dokončování. Můžete vždy automatického dokončování prázdný element zadáním zpětné lomítko (/).  
  
 **Atribut uvozovky**  
 Při vytváření atributy XML, editor vloží `=" "` znaků a umisťuje šipka nahoru (^) uvnitř dvojitých uvozovek.  
  
 Ve výchozím nastavení je zaškrtnuto.  
  
 **Namespace – deklarace**  
 Editor automaticky vloží deklarace oboru názvů, bez ohledu na jsou potřeba.  
  
 Ve výchozím nastavení je zaškrtnuto.  
  
 **Další kód (komentáře, CDATA)**  
 Komentáře, CDATA, DOCTYPE, pokyny pro zpracování a jiné značky jsou automaticky dokončit.  
  
 Ve výchozím nastavení je zaškrtnuto.  
  
## <a name="network"></a>Sítě  
 **Automaticky stahovat specifikace DTD a schémat.**  
 Schémata a definice typu dokumentu (specifikace DTD) se automaticky stáhnou z umístění protokolu HTTP. Tato funkce používá System.Net s detekce automaticky proxy serveru povoleno.  
  
 Ve výchozím nastavení je zaškrtnuto.  
  
## <a name="outlining"></a>Sbalování  
 **Zadejte popisující režimu při otevírání souborů**  
 Spustí funkci popisující při otevření souboru.  
  
 Ve výchozím nastavení je zaškrtnuto.  
  
## <a name="caching"></a>Ukládání do mezipaměti  
 **Schémata**  
 Určuje umístění mezipaměti schématu. Na tlačítko Procházet (**...** ) otevře **Procházet adresář** dialogové okno na aktuální umístění mezipaměti schématu. Můžete vybrat jiný adresář, nebo můžete vybrat složku v dialogovém okně klikněte pravým tlačítkem a zvolte **otevřete** vidět co je v adresáři.  
  
## <a name="see-also"></a>Viz také  
 [Vlastnosti dokumentu XML, vlastnosti – okno](../xml-tools/xml-document-properties-properties-window.md)   
 [Součásti editoru XML](../xml-tools/xml-editor-components.md)