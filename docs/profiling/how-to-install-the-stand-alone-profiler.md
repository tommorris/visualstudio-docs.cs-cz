---
title: 'Postupy: Instalace samostatného profileru | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- performance tools, installing stand-alone profiler
- profiling tools, stand-alone profiler
ms.assetid: cae81c95-83cd-4ab6-8a98-84ef977a2f6d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3898f61987f1767dba57a63bfb3b5b753e8d37aa
ms.sourcegitcommit: 1b9c1e333c2f096d35cfc77e846116f8e5054557
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/06/2018
ms.locfileid: "34815610"
---
# <a name="how-to-install-the-stand-alone-profiler"></a>Postupy: Instalace samostatného profileru
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] poskytuje příkazového řádku na základě samostatného profileru, která se může spustit bez instalace [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] IDE. Tato situace nastane, když počítač není nebo nemůže mít nainstalované prostředí pro vývoj. Například byste neměli instalovat prostředí pro vývoj na webovém serveru produkční.  
  
> [!NOTE]
>  Při použití samostatného profileru ke shromažďování dat výkonu pro webovou stránku ASP.NET [VSPerfASPNetCmd](../profiling/vsperfaspnetcmd.md) nástroj řádku, se doporučuje namísto [VSPerfCmd](../profiling/vsperfcmd.md) nástroj.  
  
### <a name="to-install-the-stand-alone-profiler"></a>Instalace samostatného profileru  
  
1.  Vyhledejte instalační program samostatné profilu (*vs_profiler.exe*) na [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] instalačním médiu v adresáři, který zahrnuje *\Standalone profileru* cestu a potom ho spusťte.  
  
2.  Přidejte cesty pro *vsintr.exe* a *msdis150.dll* do systémové cesty.  
  
    > [!NOTE]
    >  Ve výchozí instalaci [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], *vsinstr.exe* a *msdis150.dll* jsou umístěné v *\Program Files\Visual nástrojů nástroje Studio 10\Team*.  
  
3.  Na příkazovém řádku zadejte **vsinstr –**.  
  
    > [!NOTE]
    >  Pokud se zobrazí informace o využití pro vsinstr.exe, vše, co je správně nastavena. Pokud se zobrazí chyba s oznámením vsinstr.exe nebo jeden z jejich závislých nebyl nalezen, ujistěte se, že máte vaší cesty nastavit správně, jak je popsáno v kroku 2.  
  
4.  Nastavení serveru symbol nastavením vašeho **_NT_SYMBOL_PATH** proměnnou **symsrv\*symsrv.dll\*c:\localcache\*http://msdl.microsoft.com/download/symbols**  
  
5.  Po nastavení serveru symbol pomocí proměnných prostředí systému spuštění příkazového řádku profileru nástrojů v příkazovém řádku nový. To umožňuje nové proměnné prostředí se projeví. V okně příkazového řádku zadejte následující příkaz:  
  
     **spuštění % COMSPEC %**  
  
    > [!NOTE]
    >  Podrobné pokyny o tom, jak nastavit balíček symbol serveru najdete v tématu [postupy: odkaz na Windows symbolů informace](../profiling/how-to-reference-windows-symbol-information.md).  
  
6.  Použití [vsperfreport –](../profiling/vsperfreport.md) nástroj k serializaci vaší symboly do souboru profilování dat (.vsp). Použití **vsperfreport – /summary:all /packsymbols** přepínače. Pokud nemáte symboly vložit v datovém souboru, ujistěte se, že máte nastavení proměnné prostředí _NT_SYMBOL_PATH.  
  
## <a name="see-also"></a>Viz také:  
 [Profil z příkazového řádku](../profiling/using-the-profiling-tools-from-the-command-line.md)   
 [Návod: Profilace z příkazového řádku pomocí vzorkování](../profiling/walkthrough-command-line-profiling-using-sampling.md)   
 [Návod: Profilace z příkazového řádku pomocí instrumentace](../profiling/walkthrough-command-line-profiling-using-instrumentation.md)   
 [Postupy: odkaz na Windows symbolů informace](../profiling/how-to-reference-windows-symbol-information.md)   
 [VSPerfReport](../profiling/vsperfreport.md)