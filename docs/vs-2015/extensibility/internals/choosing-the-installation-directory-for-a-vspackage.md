---
title: Výběr instalačního adresáře pro balíček VSPackage | Dokumentace Microsoftu
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
- VSPackages, installation directory
ms.assetid: 01fbbb5b-f747-446c-afe0-2a081626a945
caps.latest.revision: 18
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2ebe7ce3855b2d91687251176dc3dd5acd4c7ad2
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42696132"
---
# <a name="choosing-the-installation-directory-for-a-vspackage"></a>Výběr instalačního adresáře pro balíček VSPackage
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [výběr instalačního adresáře pro balíček VSPackage](https://docs.microsoft.com/visualstudio/extensibility/internals/choosing-the-installation-directory-for-a-vspackage).  
  
V systému souborů uživatele musí být VSPackage a jeho podpůrné soubory. Umístění závisí na, jestli sady VSPackage je spravovaná nebo nespravovaná, schéma vytváření verzí vedle sebe a výběru uživatelů.  
  
## <a name="unmanaged-vspackages"></a>Nespravované rozšíření VSPackages  
 Nespravované VSPackage je server COM, který můžete nainstalovat do libovolného umístění. Registrační informace musí přesně odráží jeho umístění. Instalační program uživatelského rozhraní (UI) by měly poskytnout výchozí umístění jako podadresář vlastnosti Instalační služby systému Windows ProgramFilesFolder. Příklad:  
  
 [ProgramFilesFolder] MyCompany\MyVSPackageProduct\V1.0\  
  
 Uživatel by měl být může změnit výchozí adresář, aby uživatelé, kteří ponechat malý spouštěcí oddíl a instalaci aplikace a nástroje na jiný svazek.  
  
 Pokud schéma vedle sebe používá VSPackage označené verzí, můžete ukládat různé verze podadresářů. Příklad:  
  
 [ProgramFilesFolder] MyCompany\MyVSPackageProduct\V1.0\2002\  
  
 [ProgramFilesFolder] MyCompany\MyVSPackageProduct\V1.0\2003\  
  
 [ProgramFilesFolder] MyCompany\MyVSPackageProduct\V1.0\2005\  
  
## <a name="managed-vspackages"></a>Spravovaná rozšíření VSPackages  
 Spravovaná rozšíření VSPackages můžete také nainstalovat do libovolného umístění. Nicméně měli byste zvážit, vždy je nainstalovat do globální mezipaměti sestavení (GAC), abyste zkrátili dobu načítání sestavení. Protože spravovaných rozšíření VSPackages jsou vždy sestavení se silným názvem, je instalovat do mezipaměti GAC znamená, že jejich ověření podpisu se silným názvem trvá pouze v době instalace. Sestavení se silným názvem nainstalované jinde v systému souborů musí mít jejich podpisy ověřit pokaždé, když jsou načteny. Pokud provádíte instalaci spravované rozšíření VSPackages v mezipaměti GAC, použijte nástroj regpkg **/Assembly** přepínač tak, aby zapisovat položky registru odkazuje na sestavení silným názvem.  
  
 Pokud nainstalujete spravovaných rozšíření VSPackages na místě než GAC, postupujte podle starší Rady pro nespravované rozšíření VSPackages zadané pro výběr directory hierarchie. Použijte nástroj regpkg **/ codebase** přepínač tak, aby zapisovat položky registru odkazuje na cestu k sestavení balíčku VSPackage.  
  
 Další informace najdete v tématu [registrace a zrušení registrace rozšíření VSPackages](../../extensibility/registering-and-unregistering-vspackages.md).  
  
## <a name="satellite-dlls"></a>Satelitní knihovny DLL  
 Podle konvence VSPackage satelitní knihovny DLL, které obsahují prostředky pro konkrétní národní prostředí – se nacházejí v podadresářích adresáře balíčku VSPackage. Podadresáře odpovídají hodnotám ID (LCID) národního prostředí.  
  
 [Správa rozšíření VSPackages](../../extensibility/managing-vspackages.md) označuje, že položky registru řídí umístění [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] skutečně hledá na VSPackage satelitní knihovny DLL. Nicméně [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] se pokouší načíst satelitní knihovny DLL v podadresáři s názvem hodnoty LCID, v uvedeném pořadí:  
  
1.  Výchozí LCID (VS LCID \1033 například pro angličtinu)  
  
2.  Výchozí LCID dílčího výchozí.  
  
3.  Výchozí systémové nastavení LCID.  
  
4.  Výchozí systémové nastavení LCID s dílčího výchozí.  
  
5.  USA Angličtina (. \1033 nebo. \0x409).  
  
 Pokud vaše knihovna DLL balíčku VSPackage zahrnuje prostředky a SatelliteDll\DllName registru vstupních bodů, [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] , pokusí se načíst ve výše uvedeném pořadí.  
  
## <a name="see-also"></a>Viz také  
 [Volba mezi sdíleným a Verzovaným rozšířením VSPackages](../../extensibility/choosing-between-shared-and-versioned-vspackages.md)   
 [Správa rozšíření VSPackages](../../extensibility/managing-vspackages.md)   
 [Registrace spravovaného balíčku](http://msdn.microsoft.com/en-us/f69e0ea3-6a92-4639-8ca9-4c9c210e58a1)

