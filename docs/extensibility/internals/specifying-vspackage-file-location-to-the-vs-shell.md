---
title: Zadání umístění souboru VSPackage VS prostředí | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- managed VSPackages, file location
- VSPackages, managed package file location
ms.assetid: beb8607a-4183-4ed2-9ac8-7527f11513b1
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7a4270fbd723e6c5aa6f16066066e0ca4ac74e5d
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2018
ms.locfileid: "31131999"
---
# <a name="specifying-vspackage-file-location-to-the-vs-shell"></a>Zadání umístění souboru VSPackage prostředí VS
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] musí být schopný k nalezení knihovny DLL pro načtení VSPackage sestavení. Abyste ji mohli najít různými způsoby, jak je popsáno v následující tabulce.  
  
|Metoda|Popis|  
|------------|-----------------|  
|Pomocí klíče registru základu kódu.|CodeBase klíč slouží k přímé [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] se načíst sestavení VSPackage z plně kvalifikované cesty. Hodnota klíče musí být cesta k souboru na knihovnu DLL. Toto je nejlepší způsob, jak mají [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] načíst vaše sestavení balíčku. Tento postup se někdy označuje jako "CodeBase a privátního instalační adresář techniku." Během registrace hodnota základu kódu, je předaná do atribut třídy registrace prostřednictvím instance <xref:Microsoft.VisualStudio.Shell.RegistrationAttribute.RegistrationContext> typu.|  
|Umístit do knihovny DLL **PrivateAssemblies** adresáře.|Umístěte sestavení v **PrivateAssemblies** podadresáři [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] adresáře. Sestavení se nachází v **PrivateAssemblies** se automaticky zjišťují, ale nejsou viditelné v **přidat odkazy** dialogové okno. Rozdíl mezi **PrivateAssemblies** a **PublicAssemblies** je, že sestavení v **PublicAssemblies** jsou uvedené v **přidat odkazy**  dialogové okno. Pokud jste se rozhodli způsobem "CodeBase a privátního instalační adresář", pak byste měli nainstalovat do **PrivateAssemblies** adresáře.|  
|Použití sestavení se silným názvem a klíče registru sestavení.|Sestavení klíč slouží k explicitně přímé [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] načíst silné s názvem VSPackage sestavení. Hodnota klíče musí být silný název sestavení.|  
|Umístit do knihovny DLL **PublicAssemblies** adresáře.|Nakonec sestavení může být umístěna do **PublicAssemblies** podadresáři. Sestavení se nachází v **PublicAssemblies** se automaticky zjišťují a zobrazí také v **přidat odkazy** dialogovém okně [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].<br /><br /> VSPackage sestavení by měla být umístěna pouze v **PublicAssemblies** adresář, v případě, že obsahují spravované součásti, které jsou určeny k znovu použít jiné VSPackage vývojáři. Většina sestavení tato kritéria nesplňují.|  
  
> [!NOTE]
>  Sestavení se silným názvem, podepsaný použijte pro všechny závislé sestavení. Tyto sestavení musí být také nainstalován ve vlastní adresáře nebo globální mezipaměti sestavení (GAC). Je to ochrana proti je v konfliktu s sestavení, které mají stejný název základního souboru, označuje jako vazbu na název příliš slabé.