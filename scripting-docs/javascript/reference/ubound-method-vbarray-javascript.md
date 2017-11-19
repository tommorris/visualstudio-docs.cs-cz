---
title: "UBound – metoda (VBArray) (JavaScript) | Microsoft Docs"
ms.custom: 
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: 
ms.suite: 
ms.technology: devlang-javascript
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: ubound
dev_langs:
- JavaScript
- TypeScript
- DHTML
helpviewer_keywords: ubound method
ms.assetid: 761811c5-9a3d-4cb3-bfe0-0a8749f34496
caps.latest.revision: "16"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dfb87cf3fd552c329635a3ca3e974c84a1324bfd
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="ubound-method-vbarray-javascript"></a>ubound – metoda (VBArray) (JavaScript)
Vrátí nejvyšší hodnotu indexu používá v zadané dimenzi VBArray.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
safeArray.ubound(dimension)   
```  
  
## <a name="parameters"></a>Parametry  
 *safeArray*  
 Požadováno. Objekt VBArray.  
  
 `dimension`  
 Volitelné. Dimenze VBArray, pro kterou je chtěli vyšší vázané index. Pokud tento parametr vynechán, `ubound` chová, jako by byl předán 1.  
  
## <a name="remarks"></a>Poznámky  
 Pokud VBArray je prázdný, `ubound` metoda vrátí definován. Pokud `dim` je větší než počet dimenzí v VBArray nebo záporná, metoda generuje chybu "Dolní index mimo rozsah".  
  
## <a name="example"></a>Příklad  
 V následujícím příkladu se skládá ze tří částí. První část je kód v jazyce VBScript k vytvoření bezpečným polím jazyka Visual Basic. Druhá část je [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] kód, který určuje počet dimenzí v poli bezpečné a horní mez Každá dimenze. Obě tyto části přejděte do \<HEAD > části na stránce HTML. Je třetí součást [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] kód, který je třeba do \<textu > části spouštět další dvě části.  
  
```JavaScript  
<head>  
<script type="text/vbscript">  
<!--  
Function CreateVBArray()  
   Dim i, j, k  
   Dim a(2, 2)  
   k = 1  
   For i = 0 To 2  
      For j = 0 To 2  
         a(j, i) = k  
         k = k + 1  
      Next  
   Next  
   CreateVBArray = a  
End Function  
-->  
</script>  
  
<script type="text/javascript">  
<!--  
function VBArrayTest(vba)  
{  
   var i;  
   var a = new VBArray(vba);  
   var s = "";  
   for (i = 1; i <= a.dimensions(); i++)  
   {  
      s += "The upper bound of dimension ";  
      s += i + " is ";  
      s += a.ubound(i);  
      s += ".<br />";  
   }  
   return (s);  
}  
-->  
</script>  
</head>  
  
<body>  
<script type="text/javascript">  
   document.write(VBArrayTest(CreateVBArray()));  
</script>  
</body>  
```  
  
## <a name="requirements"></a>Požadavky  
 Podporováno v následujících režimech dokumentů: Quirks, standardy aplikace Internet Explorer 6, standardy aplikace Internet Explorer 7, standardy aplikace Internet Explorer 8, standardy aplikace Internet Explorer 9 a standardy aplikace Internet Explorer 10. Není podporováno v [!INCLUDE[win8_appname_long](../../javascript/includes/win8-appname-long-md.md)] aplikace. Viz [Informace o verzi](../../javascript/reference/javascript-version-information.md).  
  
 **Platí pro**: [objekt VBArray](../../javascript/reference/vbarray-object-javascript.md)  
  
## <a name="see-also"></a>Viz také  
 [Dimensions – metoda (VBArray)](../../javascript/reference/dimensions-method-vbarray-javascript.md)   
 [getItem – metoda (VBArray)](../../javascript/reference/getitem-method-vbarray-javascript.md)   
 [LBound – metoda (VBArray)](../../javascript/reference/lbound-method-vbarray-javascript.md)   
 [toArray – metoda (VBArray)](../../javascript/reference/toarray-method-vbarray-javascript.md)