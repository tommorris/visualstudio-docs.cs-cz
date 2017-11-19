---
title: "Podporované změny kódu (C# a Visual Basic) | Microsoft Docs"
ms.custom: 
ms.date: 10/11/2017
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
- Edit and Continue [C#], supported code changes
- Edit and Continue [Visual Basic], supported code changes
ms.assetid: c7a48ea9-5a7f-4328-a9d7-f0e76fac399d
caps.latest.revision: "27"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9a0a7d55b19455e22836d4750c0842a47816ee86
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2017
---
# <a name="supported-code-changes-c-and-visual-basic"></a>Podporované změny kódu (C# a Visual Basic)
Upravit a pokračovat zpracovává většinu typů změn kódu uvnitř těla metody. Během ladění, ale nejde použít většinu změn mimo metod a několik změn uvnitř těla metody. Chcete-li tyto nepodporované změny použít, musí Zastavte ladění a restartujte s novou verzí kódu.

## <a name="supported-changes-to-code"></a>Podporované změny kódu

Následující tabulka uvádí změny, které mohou být provedeny C# a kód jazyka Visual Basic během relace ladění bez restartování relace.

|Jazyk element nebo funkce|Operace upravování podporované|Omezení|
|-|-|-|
|Typy|Přidání metody, pole, konstruktory, a další|[Ano](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|Iterátory|Přidat nebo upravit|Ne|
|asynchronní/await výrazy|Přidat nebo upravit|[Ano](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|Dynamické objekty|Přidat nebo upravit|Ne|
|výrazy lambda|Přidat nebo upravit|[Ano](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|LINQ – výrazy|Přidat nebo upravit|[Stejné jako výrazy lambda](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|

> [!NOTE]
> Upravit a pokračovat obecně podporuje novější jazykové funkce jako je například řetězec interpolace a podmíněné operátory s null. Nejnovější informace najdete v tématu [Šif podporované upravuje](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits) stránky.

## <a name="unsupported-changes-to-code"></a>Nepodporované změny kódu
 Následující změny nelze použít během relace ladění kódu jazyka C# a Visual Basic:  
  
-   Změny aktuální nebo jiné active příkaz.  
  
     Aktivních příkazů zahrnout všechny příkazy, funkce v zásobníku volání, které byly volána potřebujete k aktuálnímu příkazu.  
  
     Aktuální příkaz je označena kvalifikátorem žlutý pozadí v okně zdroje. Jiné active příkazy jsou označené nástrojem šedou barvou pozadí a jsou jen pro čtení. Tyto výchozí barvy lze změnit v **možnosti** dialogové okno.

- Následující tabulka uvádí nepodporované změny kódu jazyka elementu.

|Jazyk element nebo funkce|Nepodporované úpravy operace|
|-|-|
|Všechny elementy kódu|Přejmenování|
|Obory názvů|Přidejte|
|Obory názvů, typy, členy|Odstranit|
|Obecné typy|Přidat nebo upravit|
|Rozhraní|Upravit|
|Typy|Přidat člena abstraktní nebo virtuální, přidejte přepsání (viz [podrobnosti](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
|Typy|Přidat – destruktor|
|Členové|Upravit členů odkazující na vloženého typu spolupráce|
|Členy (Visual Basic)|Upravit člena s On Error nebo Resume – příkaz|
|Členy (Visual Basic)|Upravit členů obsahující klauzuli dotazu agregace, Group By, jednoduché připojení nebo připojení LINQ skupiny|
|Metody|Změna podpisů|
|Metody|Ujistěte se, abstraktní metodu stát neabstraktní přidáním textu – metoda|
|Metody|Odstraňte text – metoda|
|Atributy|Přidat nebo upravit|
|Události nebo vlastnosti|Upravit parametr typu, základní typ delegovat typu nebo návratový typ |
|Operátory nebo indexery|Upravit parametr typu, základní typ delegovat typu nebo návratový typ |
|catch – bloky|Upravit, pokud obsahuje aktivní příkaz|
|try-catch-finally – bloky|Upravit, pokud obsahuje aktivní příkaz|
|using – příkazy|Přidejte|
|asynchronní metody nebo lambdas|Upravit asynchronní metoda nebo lambda v projektu cílení na rozhraní .NET Framework 4 a snížení (viz [podrobnosti](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
|Iterátory|Upravit iterace v projektu cílení na rozhraní .NET Framework 4 a snížení (viz [podrobnosti](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
  
## <a name="unsafe-code"></a>Nezabezpečený kód  
 Nezabezpečený kód změny mají stejná omezení jako změny bezpečné kódu s jeden další omezení: Upravit a pokračovat nepodporuje změny nezabezpečený kód, který ukončí v rámci metodu, která obsahuje `stackalloc` operátor.  

## <a name="unsupported-app-scenarios"></a>Aplikace nepodporované scénáře

Nepodporované aplikace a platformy zahrnout ASP.NET 5, emulátor Silverlight 5, Windows Phone a Windows Phone a Windows 8.1.

> [!NOTE]
> Aplikace, které jsou podporovány zahrnuty UWP Windows 10 a x86 a x64 aplikací, které se zaměřují rozhraní .NET Framework 4.6 desktop nebo novější verze (pouze plochy verze rozhraní .NET Framework je).
  
## <a name="unsupported-scenarios"></a>Nepodporované scénáře  
 Upravit a pokračovat není dostupná v těchto scénářích ladění:  
  
-   Ladění ve smíšeném režimu (nativní nebo spravovaný).  
  
-   Ladění SQL.  
  
-   Ladění zotavení po havárii. Watson výpis.  
  
-   Úpravy kódu po neošetřené výjimky, když "**Unwind zásobníku volání na neošetřených výjimek**" možnost není vybraná.  
  
-   Ladění aplikace embedded runtime.  
  
-   Ladění aplikace pomocí připojit k procesu (**ladění > připojit k procesu**) namísto spuštění aplikace tak, že zvolíte **spustit** z **ladění** nabídky.  
  
-   Ladění optimalizovaného kódu.  
  
-   Ladění starší verzi kódu po novou verzi se nepodařilo sestavit z důvodu chyby sestavení.
  
## <a name="see-also"></a>Viz také  
 [Upravit a pokračovat (Visual C#)](../debugger/edit-and-continue-visual-csharp.md)   
 [Postupy: použití operace upravit a pokračovat (C#)](../debugger/how-to-use-edit-and-continue-csharp.md)