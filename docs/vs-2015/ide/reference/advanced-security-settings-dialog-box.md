---
title: Upřesnit nastavení zabezpečení – dialogové okno | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.err.debug_in_zone_no_hostproc
- vs.err.debug_in_zone_no_hostproc:11310
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Advanced Security Settings dialog box
ms.assetid: 2e7aefe9-6d20-4f3e-b257-aee1ebcc6f5d
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 72b8bb7f6301672e89c54c9fa73a72bad8148999
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674052"
---
# <a name="advanced-security-settings-dialog-box"></a>Dialogové okno Upřesnit nastavení zabezpečení
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [rozšířené zabezpečení dialogové okno nastavení](https://docs.microsoft.com/visualstudio/ide/reference/advanced-security-settings-dialog-box).  
  
  
Toto dialogové okno umožňuje zadat nastavení zabezpečení související s laděním v zóně.  
  
 Pro přístup k tomuto dialogovému oknu, vyberte uzel projektu v **Průzkumníka řešení**a potom na **projektu** nabídky, klikněte na tlačítko **vlastnosti**. Když **Návrháře projektu** se zobrazí, klikněte na tlačítko **zabezpečení** kartu. Na **zabezpečení** stránce **povolit nastavení zabezpečení ClickOnce**, klikněte na tlačítko **Toto je aplikace s částečnou důvěryhodností**a potom klikněte na tlačítko **Upřesnit**.  
  
## <a name="uielement-list"></a>Seznam prvků uživatelského rozhraní  
 **Ladit tuto aplikaci s vybranou sadou oprávnění**  
 Pokud toto políčko zaškrtnete, sadu oprávnění vybrat na **zabezpečení** stránky se používá během ladění. Ve výchozím nastavení je tato možnost vybrána.  
  
 Pro ladění v zóně zabezpečení fungovat, musí být povolena tato možnost; Navíc **povolit hostující proces sady Visual Studio** možnost (k dispozici na **ladění** stránku **Návrháře projektu**) musí být povolené.  
  
 Pro projekty aplikace WPF webového prohlížeče **Ladit tuto aplikaci s vybranou sadou oprávnění** možnost je zkontrolovaný a zakázaný.  
  
 **Udělit aplikaci přístup ke stránce jejího původu**  
 Pokud toto políčko zaškrtnete, aplikace přístup na webový server nebo sdílená složka serveru, na kterém je publikována. Ve výchozím nastavení je tato možnost vybrána.  
  
 **Ladit tuto aplikaci, jako kdyby byla stažena z následující adresy URL**  
 Pokud budete muset povolit aplikaci přístup k webu nebo sdílená složka na serveru odpovídající **adresa URL instalace** jste zadali na **publikovat** stránky, zadejte tuto adresu URL. Tato možnost je dostupná jenom v případě **udělit aplikaci přístup ke stránce jejího původu** zaškrtnuto.  
  
## <a name="see-also"></a>Viz také  
 [Stránka Zabezpečení, Návrhář projektu](../../ide/reference/security-page-project-designer.md)



