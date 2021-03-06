---
title: Keybinding – Element | Dokumentace Microsoftu
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, KeyBindings
- KeyBinding element (VSCT XML schema)
ms.assetid: e55a1098-15df-42a9-9f87-e3a99cf437dd
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: eb8e0dca8293d5d5e853dde19e0c411cfd3e4e63
ms.sourcegitcommit: 9765b3fcf89375ca499afd9fc42cf4645b66a8a2
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/20/2018
ms.locfileid: "46495294"
---
# <a name="keybinding-element"></a>Keybinding – element
Keybinding – element určuje klávesové zkratky pro příkazy.  
  
 Příkazy může mít jeden a duální klávesové zkratky, které jsou k nim má přiřazené. Příkladem jednoho vazbu klíče je **Ctrl**+**S** pro **Uložit** příkazu. Duální klávesové zkratky vyžadují dvě po sobě jdoucích kombinace kláves pro spuštění příkazu. Je například duální vazbu klíče **Ctrl * +** K **,** Ctrl**+** K ** nastavení záložku.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<Keybinding guid="MyGuid" id="MyId" Editor="MyEditor" key1="B" key2="x" mod1="Control" mod2="Alt" />  
```  
  
## <a name="attributes-and-elements"></a>Atributy a elementy  
 Následující části popisují atributy, podřízené prvky a nadřazené prvky.  
  
### <a name="attributes"></a>Atributy  
  
|Atribut|Popis|  
|---------------|-----------------|  
|identifikátor GUID|Požadováno.|  
|id|Požadováno.|  
|editor|Požadováno. Identifikátor GUID editoru určuje kontext úprav, pro kterou bude klávesová zkratka aktivní. Hodnota oboru globální vazby je "guidVSStd97".|  
|key1|Požadováno. Platné hodnoty jsou všechny typable alfanumerické znaky a dvěma číslicemi šestnáctkových hodnot předchází 0 x a [VK_constants](/windows/desktop/inputdev/virtual-key-codes).|  
|mod1|Volitelné. Libovolnou kombinaci **Ctrl**, **Alt**, a **Shift** odděleny mezerou.|  
|key2|Volitelné. Platné hodnoty jsou všechny typable alfanumerické znaky a dvěma číslicemi šestnáctkových hodnot předchází 0 x a [VK_constants](/windows/desktop/inputdev/virtual-key-codes).|  
|mod2|Volitelné. Libovolnou kombinaci **Ctrl**, **Alt**, a **Shift** odděleny mezerou.|  
|Emulátor|Volitelné.|  
|Podmínka|Volitelné. Zobrazit [podmíněné atributy](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Podřízené prvky  
  
|Prvek|Popis|  
|-------------|-----------------|  
|Nadřazené||  
|Poznámka||  
  
### <a name="parent-elements"></a>Nadřazené prvky  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[Keybindings – element](../extensibility/keybindings-element.md)|Seskupí elementy klávesové zkratky a další seskupení klávesové zkratky.|  
  
## <a name="example"></a>Příklad  
  
```  
<KeyBindings>  
  <KeyBinding guid="guidWidgetPackage" id="cmdidUpdateWidget"   
    editor="guidWidgetEditor" key1="VK_F5"/>  
  <KeyBinding guid="guidWidgetPackage" id="cmdidRunWidget"   
    editor="guidWidgetEditor" key1="VK_F5" mod1="Control"/>  
</KeyBindings>  
```  
  
## <a name="see-also"></a>Viz také:  
 [Keybindings – element](../extensibility/keybindings-element.md)   
 [Soubory tabulky (.vsct) příkaz pro Visual Studio](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
