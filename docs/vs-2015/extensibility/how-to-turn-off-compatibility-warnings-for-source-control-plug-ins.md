---
title: 'Postupy: vypnutí upozornění kompatibility pro ovládací prvek moduly plug-in zdrojového kódu | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control plug-ins, turning off compatibility warnings
- compatibility warnings, turning off
ms.assetid: ba318e12-921b-4b7a-a8c2-12c712be1dbf
caps.latest.revision: 22
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5cfa9ed4b06f8a2f567f6446f85f35e3f0cde244
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668900"
---
# <a name="how-to-turn-off-compatibility-warnings-for-source-control-plug-ins"></a>Postupy: vypnutí upozornění kompatibility pro ovládací prvek moduly plug-in zdrojového kódu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [zapnout vypnutí upozornění kompatibility pro moduly plug-in správy zdrojových kódů](https://docs.microsoft.com/visualstudio/extensibility/how-to-turn-off-compatibility-warnings-for-source-control-plug-ins).  
  
Při použití správy zdrojového kódu v se uživatel může zobrazit upozornění na kompatibilitu s několika [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Upozornění zobrazí závisí na možnostech modul plug-in správy zdrojového kódu a může být vypnuta, protože podrobné tady.  
  
### <a name="to-disable-the-warning-to-ensure-optimal-source-control-integration-with-visual-studio"></a>Toto upozornění zakážete: "aby integrace správy optimální zdrojového kódu pomocí sady Visual Studio..."  
  
-   Nastavte následující položku registru (přidání hodnota v případě potřeby):  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\DontDisplayCheckDotNETCompatible = DWORD: 00000001  
  
     Toto upozornění se zobrazí u všech jinou hodnotu než[!INCLUDE[vsvss](../includes/vsvss-md.md)] moduly plug-in.  
  
### <a name="to-disable-the-warning-the-installed-source-control-provider-does-not-support-all-the-capabilities"></a>Toto upozornění zakážete: "nainstalovaný poskytovatel správy zdrojů nepodporuje všechny požadované možnosti..."  
  
-   Nastavte následující hodnoty registru dva (přidání hodnot v případě potřeby):  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\WarnedOldMSSCCIProvider = DWORD: 00000000  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\UseOldSCC = DWORD: 00000001  
  
     Toto upozornění se zobrazí, pokud modul plug-in správy zdrojového kódu nepodporuje explicitně opětovný vstup pro více projektů (tj. Pokud můžete zkontrolovat v pouze jeden soubor a projekt současně).  
  
     Je nejvhodnější pro podporu opětovný vstup (`SCC_CAP_REENTRANT` schopností); tím se již toto upozornění. Nicméně pokud tato podpora není možné, můžete nastavit tyto položky registru.  
  
## <a name="see-also"></a>Viz také  
 [Příznaky funkcí](../extensibility/capability-flags.md)

