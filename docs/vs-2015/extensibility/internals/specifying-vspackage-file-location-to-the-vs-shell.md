---
title: Určení umístění souboru balíčku VSPackage pro prostředí sady VS | Dokumentace Microsoftu
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
- managed VSPackages, file location
- VSPackages, managed package file location
ms.assetid: beb8607a-4183-4ed2-9ac8-7527f11513b1
caps.latest.revision: 21
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bcb78478e3e7396c2cef5f6d1f786c92130c49d2
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42668441"
---
# <a name="specifying-vspackage-file-location-to-the-vs-shell"></a>Specifikace umístění souboru balíčku VSPackage pro prostředí sady VS
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [určení umístění souboru balíčku VSPackage pro prostředí sady VS](https://docs.microsoft.com/visualstudio/extensibility/internals/specifying-vspackage-file-location-to-the-vs-shell).  
  
[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] musí být schopna najít sestavení knihovny DLL pro načtení sady VSPackage. Můžete jej umístit různými způsoby, jak je popsáno v následující tabulce.  
  
|Metoda|Popis|  
|------------|-----------------|  
|Použijte klíč registru CodeBase.|Klíč základu kódu je možné směrovat [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] načtení balíčku VSPackage sestavení z plně kvalifikované cesty. Hodnotu klíče by měl být cesta k souboru na knihovnu DLL. Toto je nejlepší způsob, jak mají [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] načíst sestavení vašeho balíčku. Tato technika se někdy označuje jako "základu kódu a soukromého instalační adresář techniku." Během registrace byla předána hodnota základu kódu do třídy atributů registrace prostřednictvím instance <xref:Microsoft.VisualStudio.Shell.RegistrationAttribute.RegistrationContext> typu.|  
|Umístit knihovnu DLL do **PrivateAssemblies** adresáře.|Umístění sestavení v **PrivateAssemblies** podadresáře [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] adresáře. Sestavení součástí **PrivateAssemblies** , zjišťují se automaticky, ale nejsou viditelné v **Add References** dialogové okno. Rozdíl mezi **PrivateAssemblies** a **PublicAssemblies** je, že sestavení v **PublicAssemblies** jsou uvedené na **přidat odkazy**  dialogové okno. Pokud jste se rozhodli používat techniku "základu kódu a soukromého instalační adresář", pak byste měli nainstalovat do **PrivateAssemblies** adresáře.|  
|Použijte sestavení se silným názvem a klíčem registru sestavení.|Klíč sestavení je možné explicitně směrovat [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] silné zatížení s názvem sestavení VSPackage. Hodnota klíče musí být silný název sestavení.|  
|Umístit knihovnu DLL do **PublicAssemblies** adresáře.|Nakonec sestavení můžou také umístit **PublicAssemblies** podadresáře. Sestavení se nachází v **PublicAssemblies** se automaticky zjistí a zobrazí se také v **Add References** dialogové okno v [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].<br /><br /> VSPackage sestavení by měla být umístěna pouze v **PublicAssemblies** adresáře, pokud obsahují spravované součásti, které mají za cíl opakovaně využít pro jiné vývojáře VSPackage. Většina sestavení toto kritérium nesplňují.|  
  
> [!NOTE]
>  Sestavení silným názvem, podepsaný držitelem se používají pro všechna závislá sestavení. Tato sestavení musí být nainstalovaná také do vlastního adresáře nebo globální mezipaměti sestavení (GAC). Je to ochrana proti je v konfliktu s sestavení, které mají stejný základní název souboru, označované jako weak vazbu.

