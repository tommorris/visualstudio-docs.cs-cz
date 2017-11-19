---
title: "Formátování specifikátory v ladicím programu (C#) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- expressions [C#], formatting values
- variables [debugger], watch variable symbols
- symbols, watch variable formatting
- QuickWatch dialog box, using format specifiers
- specifiers, watch variable format
- QuickWatch dialog box, format specifiers in C#
- specifiers
- watch variable symbols
- Watch window, format specifiers in C#
- format specifiers, debugger
- debugger, format specifiers recognized by
ms.assetid: 345c8589-5f36-4d34-a58c-e56271687dd6
caps.latest.revision: "29"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: edb41f8fea8447f8616b4c20f442ffd4fa8b48c8
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="format-specifiers-in-c-in-the-visual-studio-debugger"></a>Specifikátory formátu v jazyce C# v ladicím programu sady Visual Studio
Formát, ve kterém je zobrazená hodnota v lze změnit **sledovat** okno použití specifikátorů formátu. Můžete také použít specifikátory formátu v **Immediate** okně **příkaz** okno a to i v systému windows zdroje. Pokud přesunutí ukazatele myši na výrazu v těchto windows, zobrazí se v datového tipu výsledek. Datatips – bude odrážet specifikace formátu v popis dat zobrazení.  
  
 K specifikátor formátu, zadejte výraz oddělený čárkou. Za čárkou přidejte příslušnou specifikátor.  
  
## <a name="using-format-specifiers"></a>Použití specifikátorů formátu  
 Pokud máte následující kód:  
  
```CSharp  
{  
        int my_var1 = 0x0065;  
        int my_var2 = 0x0066;  
        int my_var3 = 0x0067;  
}  
```  
  
 Přidat `my_var1` proměnné do okna kukátka (při ladění, **ladění > Windows > sledovat > sledovat 1**) a nastavte zobrazení na šestnáctkové (v **sledovat** okna, klikněte pravým tlačítkem na proměnnou a Vyberte **hexadecimální zobrazení**). Nyní **sledovat** ukazuje, že obsahuje hodnotu 0x0065. Tato hodnota, vyjádřené jako celé desetinné číslo namísto šestnáctkové celé číslo ve sloupci Název po názvu proměnné najdete v části Přidání specifikátor formátu desetinného čísla: **, d**. Hodnota sloupce teď zobrazuje Desítková hodnota 101  
  
 ![WatchFormatCSharp](../debugger/media/watchformatcsharp.png "WatchFormatCSharp")  
  
## <a name="format-specifiers"></a>Specifikátory formátu  
 V následující tabulce jsou uvedeny C# specifikátory formátů rozpoznávané aplikací ladicího programu.  
  
|Specifikátor|Formát|Původní hodnotu sledování|Zobrazí|  
|---------------|------------|--------------------------|--------------|  
|AC|Vynutí vyhodnocení výrazu. To může být užitečné, když je vypnutý implicitní vyhodnocení vlastnosti a funkce implicitní volání.|Zpráva "vyhodnocení funkce implicitní vypnutý uživatelem."|\<Hodnota >|  
|d|desítkové celé číslo|0x0065|101|  
|dynamické odkazy|Zobrazí zadaný objekt pomocí dynamického zobrazení|Zobrazí všechny členy objektu, včetně dynamického zobrazení|Zobrazí pouze dynamického zobrazení|  
|h|hexadecimální celé číslo|61541|0x0000F065|  
|NQ|řetězec s žádné uvozovky|"Řetězec"|Moje řetězec|  
|hidden|Zobrazí všechny veřejné a jiné veřejné členy|Zobrazí veřejné členy|Zobrazí všechny členy|  
|Nezpracovaná|Zobrazí položky, jak se zobrazí v uzlu nezpracované položky. Na objekty proxy pouze platná.|Slovník\<T >|Nezpracovaná zobrazení slovník\<T >|  
|výsledky|Použít s proměnnou typ, který implementuje rozhraní IEnumerable nebo rozhraní IEnumerable\<T >, obvykle výsledek výrazu dotazu. Zobrazí pouze členové, které obsahují výsledku dotazu.|Zobrazí všechny členy.|Zobrazí členy splňují podmínky dotazu.|  
  
## <a name="see-also"></a>Viz také  
 [Sledování a QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Automatické hodnoty a místní hodnoty – Windows](../debugger/autos-and-locals-windows.md)