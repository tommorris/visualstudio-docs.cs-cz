---
title: Ladění pomocí Prohlížeče ukládání
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, store viewer
- Domain-Specific Language, store
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: fd0930445ef409f27f87658a249f9c89aac22e91
ms.sourcegitcommit: ef828606e9758c7a42a2f0f777c57b2d39041ac3
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2018
ms.locfileid: "39567061"
---
# <a name="debugging-by-using-the-store-viewer"></a>Ladění pomocí Prohlížeče ukládání
Pomocí prohlížeče Store můžete zkontrolovat stav *ukládání* používané [!INCLUDE[dsl](../modeling/includes/dsl_md.md)]. Prohlížeč Store zobrazí všechny elementy modelu domény, které jsou v konkrétní úložiště, společně s vlastností elementů a propojení mezi elementy.

## <a name="opening-store-viewer"></a>Store otevírací prohlížeče
 Pokud pracujete s [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] experimentální sestavení, zastavte kódu na zarážce, kde instance úložiště obsahuje informace o modelu. Potom otevřete prohlížeč Store tak, že zadáte následující příkaz v **okamžité** okno:

```csharp
Microsoft.VisualStudio.Modeling.Diagnostics.StoreViewer.Show(mystore);
```

> [!NOTE]
>  Je třeba nahradit `mystore` s názvem instance vašeho úložiště. Navíc pokud chcete přidat obor názvů do vašeho kódu, můžete zadat příkaz pro zobrazování Store prohlížeč bez plně kvalifikovaný obor názvů:
>
>  `using Microsoft.VisualStudio.Modeling.Diagnostics;`
>
>  `...`
>
>  `StoreViewer.Show(mystore);`

 `Show` Metoda má několik přetížení. Instance úložišti nebo oddílu můžete zadat jako parametr.

 Jako alternativu můžete vložit řádek kódu, který se zobrazí v prohlížeči Store kdekoli ve vašem kódu kde parametr, který můžete předat `Show` metoda je v oboru. Tato akce zobrazí prohlížeč Store, když se na řádek kódu provádí jako snímek obsah úložiště.

### <a name="using-store-viewer"></a>Použití prohlížeče Store
 Když se otevře prohlížeč Store nemodálním okně a Windows Forms se zobrazí, jak ukazuje následující obrázek.

 ![](../modeling/media/storeviewer2.png) Prohlížeč Store

 Prohlížeč Store má tři podokna: levé, pravé horní části podokna a pravém dolním podokně. V levém podokně je stromové zobrazení typů v `DomainDataDirectory` člen úložiště. Pokud rozbalte uzel oddílu a klikněte na prvek elementu vlastnosti se zobrazí v pravém podokně. Pokud element je propojený s ostatními prvky, další prvky se zobrazí v podokně vpravo dole. Pokud dvakrát kliknete na prvek v pravém podokně se v levém podokně zvýrazní prvek.

## <a name="see-also"></a>Viz také

- [Navigace v modelu a aktualizace modelu v kódu programu](../modeling/navigating-and-updating-a-model-in-program-code.md)