---
title: Groups – Element | Dokumentace Microsoftu
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Groups
- Groups element (VSCT XML schema)
ms.assetid: 740ca4ec-79fa-4b98-8f9a-2a137f9f7f98
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: bb437530e121daab218d8506bb41493c0423e826
ms.sourcegitcommit: 1c2ed640512ba613b3bbbc9ce348e28be6ca3e45
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/03/2018
ms.locfileid: "39497344"
---
# <a name="groups-element"></a>Groups – element
Obsahuje položky, které definují skupiny příkaz VSPackage.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<Groups>  
  <Group>... </Group>  
  <Group>... </Group>  
</Groups>  
```  
  
## <a name="attributes-and-elements"></a>Atributy a elementy  
 Následující části popisují atributy, podřízené prvky a nadřazené prvky.  
  
### <a name="attributes"></a>Atributy  
  
|Atribut|Popis|  
|---------------|-----------------|  
|Podmínka|Volitelné. Zobrazit [podmíněné atributy](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Podřízené prvky  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[Skupinového elementu](../extensibility/group-element.md)|Reprezentuje skupinu jednoho příkazu.|  
|[Groups – element](../extensibility/groups-element.md)|Obsahuje položky, které definují skupiny příkaz VSPackage.|  
  
### <a name="parent-elements"></a>Nadřazené prvky  
  
|Prvek|Popis|  
|-------------|-----------------|  
|[Commands – element](../extensibility/commands-element.md)|Představuje kolekci příkazů na panelu nástrojů VSPackage.|  
  
## <a name="example"></a>Příklad  
  
```xml  
<Groups>  
  <Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">  
    <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>  
  </Group>  
</Groups>  
```  
  
## <a name="see-also"></a>Viz také:  
 [Jak balíčky VSPackages přidávají prvky uživatelského rozhraní](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [Příkazy, nabídky a panely nástrojů](../extensibility/internals/commands-menus-and-toolbars.md)