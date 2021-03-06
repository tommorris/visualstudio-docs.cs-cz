---
title: Běžné projektu nástroje MSBuild položky | Dokumentace Microsoftu
ms.custom: ''
ms.date: 11/04/2016
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, common project items
ms.assetid: 1eba3721-cc12-4b80-9987-84923ede5e2e
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 900241a25fabc259fb19ffa2b75f2fa12ad6e517
ms.sourcegitcommit: 0e5289414d90a314ca0d560c0c3fe9c88cb2217c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/19/2018
ms.locfileid: "39152552"
---
# <a name="common-msbuild-project-items"></a>Společné položky projektu nástroje MSBuild
V [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)], položka je pojmenovaný odkaz na jeden nebo více souborů. Položky obsahují metadat – například názvy souborů, cesty a čísel verzí. Všechny typy v projektu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] mají společnou několik položek. Tyto položky jsou definovány v souboru *Microsoft.Build.CommonTypes.xsd*.  
  
## <a name="common-items"></a>Společné položky  
 Následuje seznam všechny společné položky projektu.  
  
### <a name="reference"></a>Odkaz  
 Představuje odkaz na sestavení (spravované) v projektu.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|Cestu k nápovědě|Volitelný řetězec. Relativní nebo absolutní cesta k sestavení.|  
|Název|Volitelný řetězec. Zobrazovaný název sestavení, například "System.Windows.Forms."|  
|FusionName|Volitelný řetězec. Určuje jednoduchý nebo silné sloučeném názvu pro položku.<br /><br /> Když tento atribut je k dispozici, můžete ušetřit čas, protože není potřeba otevřít získat sloučeném názvu souboru sestavení.|  
|SpecificVersion|Nepovinný datový typ boolean. Určuje, zda by se měla odkazovat pouze verze ve sloučeném názvu.|  
|Aliasy|Volitelný řetězec. Všechny aliasy pro odkaz.|  
|Soukromé|Nepovinný datový typ boolean. Určuje, zda by měl být odkaz zkopírován do výstupní složky. Tento atribut odpovídá **Kopírovat místně** vlastnost odkazu, který je v integrovaném vývojovém prostředí sady Visual Studio.|  
  
### <a name="comreference"></a>COMReference  
 Představuje komponentu modelu COM (nespravovaného) odkaz v projektu.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|Název|Volitelný řetězec. Zobrazovaný název součásti.|  
|identifikátor GUID|Volitelný řetězec. Identifikátor GUID pro komponentu ve formě {12345678-1234-1234-1234-1234567891234}.|  
|VersionMajor|Volitelný řetězec. Hlavní část čísla verze komponenty. Například "5" Pokud celé číslo verze je "5.46."|  
|VersionMinor|Volitelný řetězec. Dílčí část čísla verze komponenty. Například "46" Pokud celé číslo verze je "5.46."|  
|LCID|Volitelný řetězec. Identifikátor národního prostředí pro komponentu.|  
|WrapperTool|Volitelný řetězec. Název nástroj obálky, který je použit na komponenty, například "tlbimp".|  
|Izolovaný režim|Nepovinný datový typ boolean. Určuje, zda je součást komponenty bez registrace.|  
  
### <a name="comfilereference"></a>COMFileReference  
 Představuje seznam knihovny typů, které do cílové ResolvedComreference informačního kanálu.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|WrapperTool|Volitelný řetězec. Název nástroj obálky, který je použit na komponenty, například "tlbimp".|  
  
### <a name="nativereference"></a>NativeReference  
 Představuje nativní soubor manifestu nebo odkaz na tento soubor.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|Název|Povinný řetězec. Základní název souboru manifestu.|  
|Cestu k nápovědě|Povinný řetězec. Relativní cesta souboru manifestu.|  
  
### <a name="projectreference"></a>ProjectReference  
 Představuje odkaz na jiný projekt.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|Název|Volitelný řetězec. Zobrazovaný název odkazu.|  
|Projekt|Volitelný řetězec. Identifikátor GUID pro odkaz ve formuláři {12345678-1234-1234-1234-1234567891234}.|  
|Balíček|Volitelný řetězec. Cesta souboru projektu, který se odkazuje.|  
|ReferenceOutputAssembly|Nepovinný datový typ boolean. Pokud nastavena na `false`, neobsahuje výstup Odkazovaný projekt jako [odkaz](#Reference) tohoto projektu, ale přesto se zajistí, že jiný projekt sestavení před tímto. Výchozí hodnota je `true`.|
  
### <a name="compile"></a>Kompilace  
 Představuje zdrojové soubory pro kompilátor.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|DependentUpon|Volitelný řetězec. Určuje soubor, tento soubor, na kterém závisí na správnou kompilaci.|  
|AutoGen|Nepovinný datový typ boolean. Určuje, zda soubor byl vygenerován pro projektu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] integrované vývojové prostředí (IDE).|  
|Odkaz|Volitelný řetězec. Konvenční cesta zobrazí, když je soubor fyzicky umístěn mimo vliv souboru projektu.|  
|Viditelné|Nepovinný datový typ boolean. Určuje, zda se zobrazí soubor v **Průzkumníka řešení** v [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].|  
|CopyToOutputDirectory|Volitelný řetězec. Určuje, jestli se má zkopírovat soubor do výstupního adresáře. Hodnoty jsou:<br /><br /> 1.  Nikdy<br />2.  Vždy<br />3.  PreserveNewest|  
  
### <a name="embeddedresource"></a>EmbeddedResource  
 Představuje prostředky mají být vloženy do generovaného sestavení.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|DependentUpon|Volitelný řetězec. Určuje soubor, tento soubor, na kterém závisí na správnou kompilaci|  
|Generátor|Povinný řetězec. Název generátoru spuštěného nad touto položkou.|  
|LastGenOutput|Povinný řetězec. Název souboru, který byl vytvořen jakýmkoliv generátorem spuštěné v této položce.|  
|CustomToolNamespace|Povinný řetězec. Obor názvů, ve které libovolný soubor generátor spuštěný nad touto položkou vytvořit kód.|  
|Odkaz|Volitelný řetězec. Konvenční cesta se zobrazí, pokud je soubor fyzicky umístěn mimo vliv projektu.|  
|Viditelné|Nepovinný datový typ boolean. Určuje, zda se zobrazí soubor v **Průzkumníka řešení** v [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].|  
|CopyToOutputDirectory|Volitelný řetězec. Určuje, jestli se má zkopírovat soubor do výstupního adresáře. Hodnoty jsou:<br /><br /> 1.  Nikdy<br />2.  Vždy<br />3.  PreserveNewest|  
|LogicalName|Povinný řetězec. Logický název vloženého zdroje.|  
  
### <a name="content"></a>Obsah  
 Představuje soubory, které nejsou kompilovány do projektu, ale může vloženy nebo publikovány společně s jeho.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|DependentUpon|Volitelný řetězec. Určuje soubor, tento soubor, na kterém závisí na správnou kompilaci.|  
|Generátor|Povinný řetězec. Název generátoru, na kterém běží nad touto položkou.|  
|LastGenOutput|Povinný řetězec. Název souboru, který byl vytvořen jakýmkoliv generátorem spuštěným nad touto položkou.|  
|CustomToolNamespace|Povinný řetězec. Obor názvů, ve které libovolný soubor generátor spuštěný nad touto položkou vytvořit kód.|  
|Odkaz|Volitelný řetězec. Konvenční cesty chcete zobrazit, pokud je soubor fyzicky umístěn mimo vliv projektu.|  
|PublishState|Povinný řetězec. Stav publikování obsahu, buď:<br /><br /> – Výchozí<br />-Zahrnuté<br />-Vyloučen<br />-DataFile<br />– Požadavek|  
|IsAssembly|Nepovinný datový typ boolean. Určuje, zda je soubor sestavení.|  
|Viditelné|Nepovinný datový typ boolean. Určuje, zda se zobrazí soubor v **Průzkumníka řešení** v [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].|  
|CopyToOutputDirectory|Volitelný řetězec. Určuje, jestli se má zkopírovat soubor do výstupního adresáře. Hodnoty jsou:<br /><br /> 1.  Nikdy<br />2.  Vždy<br />3.  PreserveNewest|  
  
### <a name="none"></a>Žádné  
 Představuje soubory, které by se neměly nijak podílet v procesu sestavení.  
  
|Název metadat položky|Popis|  
|---------------|-----------------|  
|DependentUpon|Volitelný řetězec. Určuje soubor, tento soubor, na kterém závisí na správnou kompilaci.|  
|Generátor|Povinný řetězec. Název generátoru spuštěného nad touto položkou.|  
|LastGenOutput|Povinný řetězec. Název souboru, který byl vytvořen jakýmkoliv generátorem spuštěné v této položce.|  
|CustomToolNamespace|Povinný řetězec. Obor názvů, ve které libovolný soubor generátor spuštěný nad touto položkou vytvořit kód.|  
|Odkaz|Volitelný řetězec. Konvenční cesty chcete zobrazit, pokud je soubor fyzicky umístěn mimo vliv projektu.|  
|Viditelné|Nepovinný datový typ boolean. Určuje, zda se zobrazí soubor v **Průzkumníka řešení** v [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].|  
|CopyToOutputDirectory|Volitelný řetězec. Určuje, jestli se má zkopírovat soubor do výstupního adresáře. Hodnoty jsou:<br /><br /> 1.  Nikdy<br />2.  Vždy<br />3.  PreserveNewest|  
  
### <a name="baseapplicationmanifest"></a>BaseApplicationManifest  
 Představuje základní manifest aplikace pro sestavení a obsahuje [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] informace o zabezpečení nasazení.  
  
### <a name="codeanalysisimport"></a>CodeAnalysisImport  
 Představuje projekt FxCop pro import.  
  
### <a name="import"></a>Importovat  
 Představuje sestavení, jejichž jmenné prostory by měly být naimportovány podle [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] kompilátoru.  
  
## <a name="see-also"></a>Viz také:  
 [Obecné vlastnosti projektu nástroje MSBuild](../msbuild/common-msbuild-project-properties.md)
