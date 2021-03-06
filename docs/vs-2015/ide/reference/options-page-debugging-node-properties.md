---
title: Stránka Možnosti, vlastnosti uzlu ladění | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 564cc8b2-0084-420e-b560-200cc5621a7e
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 128e4719775a4ce9d06214547936110ed88b7a14
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42628628"
---
# <a name="options-page-debugging-node-properties"></a>Stránka Možnosti, vlastnosti uzlu ladění
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [stránka Možnosti, vlastnosti uzlu ladění](https://docs.microsoft.com/visualstudio/ide/reference/options-page-debugging-node-properties).  
  
  
Následující tabulky popisují stránky (nebo kolekce vlastností), které jsou přidruženy **ladění** kategorie, `DTE.Properties("Debugging", <Property Page>)` z **možnosti** dialogové okno.  
  
## <a name="general"></a>Obecné  
 `DTE.Properties("Debugging", "General")`  
  
|Název položky vlastnosti|Hodnota|Popis|  
|------------------------|-----------|-----------------|  
|PromptOnBreakpointDelete|Get/Set (Boolean)|Určuje, zda ladicí program zobrazí výzvu k zadání oprávnění před smazáním všech zarážek v projektu.|  
|BreakAllProcesses|Get/Set (Boolean)|Určuje, zda ladicí program zruší všechny procesy pokaždé, když se jeden přeruší.|  
|BreakAtBoundaries|Get/Set (Boolean)|Určuje, zda ladicí program zruší spuštění, když výjimky překročí ohraničení mezi doménami AppDomain nebo mezi spravovaný a nativní kód.|  
|EnableAddressLevelDebugging|Get/Set (Boolean)|Určuje, zda jsou povoleny funkce ladění na úrovni adres.|  
|ShowDisassemblyIfNoSource|Get/Set (Boolean)|Určuje, zda ladicí program zobrazí zpětný překlad kódu, pokud není k dispozici zdrojový kód.|  
|EnableBreakpointFilters|Get/Set (Boolean)|Určuje, zda je povolena zarážka filtrování.|  
|EnableExceptionAssistant|Get/Set (Boolean)|Určuje, jestli Pomocník pro výjimky se používá pro spravované výjimky.|  
|UnwindCallstack|Get/Set (Boolean)|Určuje, zda ladicí program unwinds zásobník volání pro neošetřené výjimce.|  
|EnableJustMyCode|Get/Set (Boolean)|Určuje, zda je povoleno pouze můj kód, pro jazyk C# a pro kód jazyka Visual Basic.|  
|ShowAllMembers|Get/Set (Boolean)|Objekty od uživatele určuje, zda ladicí program zobrazí všechny členy objektů v oknech proměnných. Tato možnost nemá žádný vliv, pokud je povoleno pouze můj kód.|  
|WarnIfNoUserCode|Get/Set (Boolean)|Určuje, zda ladicí program, vysílá varování, když se uživatel pokusí připojit k procesu, který nemá žádný uživatelský kód. Tato možnost nemá žádný vliv, pokud je povoleno pouze můj kód.|  
|EnablePropertyEvaluation|Get/Set (Boolean)|Určuje, zda ladicí program automaticky vyhodnotí, vlastnosti a volání implicitních funkcí ve spravovaném kódu.|  
|CallStringConversion|Get/Set (Boolean)|Určuje, zda ladicí program implicitně volá funkce pro převod řetězce na objektech v oknech proměnných. Tato možnost se týká pouze kód jazyka C# a JScript.|  
|EnableSourceServer|Get/Set (Boolean)|Určuje, zda ladicí program může přístupový kód ze zdrojového serveru.|  
|PrintSourceServerDiagnostics|Get/Set (Boolean)|Určuje, zda okno výstup zobrazí diagnostické zprávy týkající se na zdrojovém serveru. Tato možnost nemá žádný vliv, pokud je povolen přístup zdrojovému serveru.|  
|HighlightEntireLine|Get/Set (Boolean)|Určuje, zda ladicí program zvýrazní celého řádku pro zarážky a aktuální příkaz.|  
|RequireSourceToMatch|Get/Set (Boolean)|Určuje, zda ladicí program vyžaduje zdrojové soubory přesně shodovaly s originály při otevírání souborů pro ladění.|  
|RedirectOutputToImmediate|Get/Set (Boolean)|Určuje, zda výstup z okna výstup se přesměruje do příkazového podokna.|  
|ShowRawVariableStructure|Get/Set (Boolean)|Určuje, zda se zobrazí objekty v oknech proměnných v nezpracovaném tvaru.|  
|SuppressJitOptimization|Get/Set (Boolean)|Pro spravovaný kód určuje, zda je potlačeno just-in-time optimalizace ladicím programem.|  
|WarnIfNoSymbols|Get/Set (Boolean)|Určuje, zda ladicí program zobrazí upozornění, pokud nejsou k dispozici žádné symboly pro ladění, když se spustí proces.|  
|WarnIfScriptDisabled|Get/Set (Boolean)|Určuje, zda ladicí program zobrazí upozornění, pokud není povolené ladění skriptů při spuštění procesu.|  
|ShowMarkersForAllThreads|Get/Set (Boolean)|Určuje, zda ladicí program zobrazí značky vlákna.|  
|StepOverPropertiesAndOperators|Get/Set (Boolean)|Určuje, zda chcete krokovat přes vlastnosti a operátory ve spravovaném kódu pouze.|  
  
## <a name="edit-and-continue"></a>Upravit a pokračovat  
 `DTE.Properties("Debugging", "EditAndContinue")`  
  
|Název položky vlastnosti|Hodnota|Popis|  
|------------------------|-----------|-----------------|  
|EnableEditAndContinue|Get/Set (Boolean)|Určuje, zda je povoleno upravit a pokračovat. Tato možnost se vztahuje na všechny jazyky, které podporují funkce upravit a pokračovat.|  
|InvokedByCommands|Get/Set (Boolean)|Určuje, zda funkce upravit a pokračovat automaticky aplikuje změny kódu když uživatel vybere příkaz ladění, jako **krok** nebo **pokračovat**. Tato možnost se týká pouze nativního kódu.|  
|InvokedByCommandsAskFirst|Get/Set (Boolean)|Určuje, zda funkce upravit a pokračovat vyzve uživatele k zadání oprávnění k použití změn kódu, když uživatel vybere příkaz ladění, jako **krok** nebo **pokračovat**. Tato možnost se týká pouze nativního kódu.|  
|WarnAboutStaleCode|Get/Set (Boolean)|Určuje, zda ladicí program vydá zprávu s upozorněním při spuštění kódu neaktuální nebo zastaralý, způsobí upravit a pokračovat. Tato možnost se týká pouze nativního kódu.|  
|RelinkChangesOnStop|Získá nebo nastaví (krátký)|Určuje, zda sady Visual Studio relinks změn kódu aplikovaných procedurou Edit a Continue, když se zastaví spuštění aplikace. Tato možnost se týká pouze nativního kódu.|  
|AllowPrecompiling|Získá nebo nastaví (krátký)|Určuje, zda je povoleno upravit a pokračovat pro načtení předkompilovaných hlaviček na pozadí. Tato možnost se týká pouze nativního kódu.|  
  
## <a name="just-in-time"></a>za běhu  
 `DTE.Properties("Debugging", "JustInTime")`  
  
|Název položky vlastnosti|Hodnota|Popis|  
|------------------------|-----------|-----------------|  
|JitManaged|Get/Set (Boolean)|Určuje, zda je povoleno ladění za běhu pro spravovaný kód.|  
|JitNative|Get/Set (Boolean)|Určuje, zda je povoleno ladění za běhu pro nativní kód.|  
|JitScript|Get/Set (Boolean)|Určuje, zda je povoleno ladění za běhu pro kód skriptu.|  
  
## <a name="native"></a>Nativní  
 `DTE.Properties("Debugging", "Native")`  
  
|Název položky vlastnosti|Hodnota|Popis|  
|------------------------|-----------|-----------------|  
|LoadDllExports|Get/Set (Boolean)|Určuje, zda ladicí program načte tabulky exportu knihovny DLL.|  
|EnableRPC|Get/Set (Boolean)|Určuje, zda ladicího programu můžete krokovat s vnořením COM vzdálených volání procedur.|  
  
## <a name="see-also"></a>Viz také  
 [Řízení nastavení možností](http://msdn.microsoft.com/library/a09ed242-7494-4cde-bbd1-7a8ec617965d)   
 [Určování názvů položky vlastností na stránkách možností](http://msdn.microsoft.com/library/d450422d-47c7-4eeb-9f9f-3286264bc5aa)   
 [Stránka Možnosti, vlastnosti uzlu barev a písem](../../ide/reference/options-page-fonts-and-colors-node-properties.md)   
 [Stránka Možnosti, vlastnosti uzlu textového editoru](../../ide/reference/options-page-text-editor-node-properties.md)   
 [Obecné, ladění, dialogové okno Možnosti](../../debugger/general-debugging-options-dialog-box.md)   
 [Upravit a pokračovat, ladění, dialogové okno Možnosti](http://msdn.microsoft.com/library/009d225f-ef65-463f-a146-e4c518f86103)   
 [Just-In-Time, ladění, dialogové okno Možnosti](../../debugger/just-in-time-debugging-options-dialog-box.md)



