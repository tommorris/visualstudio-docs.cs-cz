---
title: "Vlastnost &lt;název vlastnosti&gt; nelze odstranit, protože se účastní přidružení &lt;název přidružení&gt; | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 389873cc-92dd-48da-bfca-0f6c8e0ae3c2
caps.latest.revision: "3"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 150d176c105e8368fc97f36a19774824dcb91c3e
ms.sourcegitcommit: ee42a8771f0248db93fd2e017a22e2506e0f9404
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2017
---
# <a name="the-property-ltproperty-namegt-cannot-be-deleted-because-it-is-participating-in-the-association-ltassociation-namegt"></a>Vlastnost &lt;název vlastnosti&gt; nelze odstranit, protože se účastní přidružení &lt;název přidružení&gt;
Vybranou vlastnost je nastavena jako **vlastnosti přidružení** pro přidružení mezi třídami uvedené v chybové zprávě. Vlastnosti nelze odstranit, pokud se účastní přidružení mezi datových tříd.  
  
 Nastavte **vlastnosti přidružení** na jinou vlastnost třídy dat. Chcete-li povolit úspěšné odstranění požadované vlastnosti.  
  
### <a name="to-correct-this-error"></a>Oprava této chyby  
  
1.  Vyberte řádek přidružení na Návrhář relací objektů, který se připojuje datové třídy uvedené v chybové zprávě.  
  
2.  Klikněte dvakrát na řádek otevřete **přidružení Editor** dialogové okno.  
  
3.  Odeberte vlastnost z **vlastnosti přidružení**.  
  
4.  Pokuste se znovu odstranit vlastnost.  
  
## <a name="see-also"></a>Viz také
[Návrhář relací objektů zprávy](../data-tools/o-r-designer-messages.md)  
[Technologie LINQ to SQL nástroje v sadě Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)