---
title: Lib – úloha | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VC.Project.VCLibrarianTool.Name
- VC.Project.VCLibrarianTool.TreatLibWarningsAsErrors
- VC.Project.VCLibrarianTool.Verbose
- vc.task.lib
- VC.Project.VCLibrarianTool.ErrorReporting
- VC.Project.VCLibrarianTool.LinkLibraryDependencies
- VC.Project.VCLibrarianTool.LinkTimeCodeGeneration
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), LIB task
- LIB task (MSBuild (Visual C++))
ms.assetid: e062c7f9-cc69-4a83-9361-1bb5355e5fe8
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dcdcece820af764e627aafc43ef405c627724b68
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/05/2018
ms.locfileid: "43775968"
---
# <a name="lib-task"></a>LIB – úloha
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [lib – úloha](https://docs.microsoft.com/visualstudio/msbuild/lib-task).  
  
  
Zabalí nástroj Microsoft 32bitový Správce knihovny lib.exe. Správce knihovny vytváří a spravuje knihovnu objektových souborů Common Object File Format (COFF). Správce knihovny můžete vytvořit soubory exportu a importu knihovny odkaz exportovat definice. Další informace najdete v tématu [LIB Reference](http://msdn.microsoft.com/library/ecc7f643-bbd4-47a3-8dc6-b360f880db91) a [spuštění knihovny LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).  
  
## <a name="parameters"></a>Parametry  
 Následující tabulka popisuje parametry **LIB** úloh. Většina úkolů parametry odpovídají možnost příkazového řádku.  
  
|Parametr|Popis|  
|---------------|-----------------|  
|**AdditionalDependencies**|Volitelné **String []** parametru.<br /><br /> Určuje další položky pro přidání do příkazového řádku.|  
|**AdditionalLibraryDirectories**|Volitelné **String []** parametru.<br /><br /> Přepíše cestu ke knihovně prostředí. Zadejte název adresáře.<br /><br /> Další informace najdete v tématu [/Libpath (další proměnná Libpath)](http://msdn.microsoft.com/library/7240af0b-9a3d-4d53-8169-2a92cd6958ba).|  
|**AdditionalOptions**|Volitelné **řetězec** parametru.<br /><br /> Seznam možností lib.exe uvedená na příkazovém řádku. Například ** "_/option1 /option2 /option#_". Tento parametr použijte k určení možností lib.exe, které nejsou reprezentovány jakýkoli jiný **LIB** parametr úlohy.<br /><br /> Další informace najdete v tématu [spuštění knihovny LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**DisplayLibrary**|Volitelné **řetězec** parametru.<br /><br /> Zobrazí informace o výstupní knihovně. Zadejte název souboru pro přesměrování informace do souboru. Zadejte "CON" nebo nic přesměrovat informace do konzoly.<br /><br /> Tento parametr **/LIST** možností lib.exe.|  
|**ErrorReporting**|Volitelné **řetězec** parametru.<br /><br /> Určuje, jak odeslat informace o interní chybě společnosti Microsoft, lib.exe selže v době běhu.<br /><br /> Zadejte jednu z následujících hodnot, z nichž každý odpovídá možnosti příkazového řádku.<br /><br /> -   **NoErrorReport** -   **/errorreport: žádné**<br />-   **PromptImmediately** - **/ERRORREPORT:PROMPT**<br />-   **QueueForNextLogin** - **/ERRORREPORT:QUEUE**<br />-   **SendErrorReport** -   **/errorreport: Send**<br /><br /> Další informace najdete v tématu **/errorreport** možnost příkazového řádku na [spuštění knihovny LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**ExportNamedFunctions**|Volitelné **String []** parametru.<br /><br /> Určuje jednu nebo více funkcí pro export.<br /><br /> Tento parametr **/EXPORT:** možností lib.exe.|  
|**ForceSymbolReferences**|Volitelné **řetězec** parametru.<br /><br /> Lib.exe vynutí zahrnutí odkazu pro zadaný symbol.<br /><br /> Tento parametr **/INCLUDE:** možností lib.exe.|  
|**IgnoreAllDefaultLibraries**|Volitelné `Boolean` parametru.<br /><br /> Pokud `true`, odebere všechny výchozí knihovny ze seznamu knihoven této lib.exe prohledává při překladu externích odkazů.<br /><br /> Tento parametr odpovídá formě bez parametrů **: / NODEFAULTLIB** možností lib.exe.|  
|**IgnoreSpecificDefaultLibraries**|Volitelné **String []** parametru.<br /><br /> Odebere zadaný knihoven ze seznamu knihoven této lib.exe prohledává při překladu externích odkazů.<br /><br /> Tento parametr **: / NODEFAULTLIB** možností lib.exe, který přijímá `library` argument.|  
|**LinkLibraryDependencies**|Volitelné `Boolean` parametru.<br /><br /> Pokud `true`, určuje, že knihovny vytvořené jako výstupy závislostí projektu automaticky připojeny.|  
|**LinkTimeCodeGeneration**|Volitelné `Boolean` parametru.<br /><br /> Pokud `true`, určuje generování kódu při propojování.<br /><br /> Tento parametr **/LCTG** možností lib.exe.|  
|**MinimumRequiredVersion**|Volitelné **řetězec** parametru.<br /><br /> Určuje minimální požadovanou verzi subsystému. Zadejte čárkami oddělený seznam desetinná čísla v rozsahu 0 až 65535.|  
|**ModuleDefinitionFile**|Volitelné **řetězec** parametru.<br /><br /> Určuje název souboru definice modulu (.def).<br /><br /> Tento parametr **def** možností lib.exe, který přijímá `filename` argument.|  
|**Jméno**|Volitelné **řetězec** parametru.<br /><br /> Při vytváření knihovny importu, určuje název knihovny DLL pro kterou má být sestaven knihovny importu.<br /><br /> Tento parametr **/NAME** možností lib.exe, který přijímá `filename` argument.|  
|**Výstupní soubor**|Volitelné **řetězec** parametru.<br /><br /> Přepíše výchozí název a umístění programu, vytvoří tento lib.exe.<br /><br /> Tento parametr **/OUT** možností lib.exe, který přijímá `filename` argument.|  
|**RemoveObjects**|Volitelné **String []** parametru.<br /><br /> Vynechá zadaný objekt z výstupní knihovně. Lib.exe vytvoří výstupní knihovnu tak, že zkombinuje všechny objekty (ať už v souborech objektů nebo knihoven) a poté odstraní všechny objekty, které jsou určeny tuto možnost.<br /><br /> Tento parametr **/REMOVE** možností lib.exe, který přijímá `membername` argument.|  
|**Zdroje**|Vyžaduje `ITaskItem[]` parametru.<br /><br /> Určuje seznam zdrojových souborů, oddělené mezerami.|  
|**Subsystém**|Volitelné **řetězec** parametru.<br /><br /> Určuje prostředí pro spustitelný soubor. Volba subsystému ovlivňuje symbol vstupního bodu nebo funkci vstupního bodu.<br /><br /> Zadejte jednu z následujících hodnot, z nichž každý odpovídá možnosti příkazového řádku.<br /><br /> -   **Konzola** -   **/Subsystem: Console**<br />-   **Windows** -   **/Subsystem: Windows**<br />-   **Nativní** - **souboru**<br />-   **Aplikace EFI** - **/SUBSYSTEM:EFI_APPLICATION**<br />-   **Ovladač spouštěcí služby EFI** - **/SUBSYSTEM:EFI_BOOT_SERVICE_DRIVER**<br />-   **PAMĚŤ ROM EFI** - **/SUBSYSTEM:EFI_ROM**<br />-   **Modul Runtime EFI** - **/SUBSYSTEM:EFI_RUNTIME_DRIVER**<br />-   **WindowsCE** - **/SUBSYSTEM:WINDOWSCE**ReplaceThisText<br />-   **POSIX** - **/SUBSYSTEM:POSIX**<br /><br /> Další informace najdete v tématu [/Subsystem (určení subsystému)](http://msdn.microsoft.com/library/d7b133cf-cf22-4da8-ab46-6552702c0b9b).|  
|**SuppressStartupBanner**|Volitelné **logická** parametru.<br /><br /> Pokud `true`, zabraňuje zobrazování čísel zprávu o autorských právech a verze při spuštění úlohy.<br /><br /> Další informace najdete v tématu **/nologo** možnost v [spuštění knihovny LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**TargetMachine**|Volitelné **řetězec** parametru.<br /><br /> Určuje cílovou platformu pro program nebo knihovnu DLL.<br /><br /> Zadejte jednu z následujících hodnot, z nichž každý odpovídá možnosti příkazového řádku.<br /><br /> -   **MachineARM** - **/MACHINE:ARM**<br />-   **MachineEBC** - **/MACHINE:EBC**<br />-   **MachineIA64** - **/MACHINE:IA64**<br />-   **MachineMIPS** - **/MACHINE:MIPS**<br />-   **MachineMIPS16** - **/MACHINE:MIPS16**<br />-   **MachineMIPSFPU** -**/MACHINE:MIPSFPU**<br />-   **MachineMIPSFPU16** - **/MACHINE:MIPSFPU16**<br />-   **MachineSH4** - **/MACHINE:SH4**<br />-   **MachineTHUMB** - **/MACHINE:THUMB**<br />-   **MachineX64** - **/MACHINE:X 64**<br />-   **MachineX86** - **/MACHINE:X 86**<br /><br /> Další informace najdete v tématu [/Machine (určení cílové platformy)](http://msdn.microsoft.com/library/8d41bf4b-7e53-4ab9-9085-d852b08d31c2).|  
|**TrackerLogDirectory**|Volitelné **řetězec** parametru.<br /><br /> Určuje adresář protokolu sledovacího modulu.|  
|**TreatLibWarningAsErrors**|Volitelné **logická** parametru.<br /><br /> Pokud `true`, způsobí, že **LIB** úkolů nelze vytvořit výstupní soubor, pokud lib.exe vygeneruje upozornění. Pokud `false`, vygeneruje výstupní soubor.<br /><br /> Další informace najdete v tématu **/WX** možnost v [spuštění knihovny LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
|**UseUnicodeResponseFiles**|Volitelné **logická** parametru.<br /><br /> Pokud `true`, nastaví systém projektu při není vytvořen nástrojem librarian generoval soubory odezvy UNICODE. Zadejte `true` Pokud soubory v projektu mají cesty UNICODE.|  
|**Verbose**|Volitelné **logická** parametru.<br /><br /> Pokud `true`, se zobrazí podrobnosti o průběhu relace; to zahrnuje názvy přidávané soubory .obj. Informace odeslány na standardní výstup a je možné přesměrovat do souboru.<br /><br /> Další informace najdete v tématu **/VERBOSE** možnost [spuštění knihovny LIB](http://msdn.microsoft.com/library/d54f5c81-7147-4b2c-a8db-68ce6eb1eabd).|  
  
## <a name="remarks"></a>Poznámky  
  
## <a name="see-also"></a>Viz také  
 [Referenční dokumentace úlohy](../msbuild/msbuild-task-reference.md)



