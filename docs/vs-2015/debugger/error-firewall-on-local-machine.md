---
title: 'Chyba: Brána Firewall v místním počítači | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.firewall.localmachine
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: ab60dda9-7934-4891-aa2f-001380d2ed83
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6f4cee2d391038c9157666078c6fd83027bc35e6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42674279"
---
# <a name="error-firewall-on-local-machine"></a>Chyba: Brána firewall v místním počítači
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [Chyba: Brána Firewall v místním počítači](https://docs.microsoft.com/visualstudio/debugger/error-firewall-on-local-machine).  
  
Bránu na místním počítači, počítač, na kterém běží Visual Studio, není nastavené pro povolení vzdáleného ladění. Spravované nebo nativní vzdáleného ladění s výchozí spojení, musíte otevřít port TCP 135 DCOM provoz. Musí být otevřeny sdílení souborů a tiskáren a devenv.exe musí být přidán do seznamu výjimek. Některé porty protokolu IPSEC může být nutné také.  
  
 Další informace najdete v tématu [nastavit Up the Remote Tools na zařízení](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c).



