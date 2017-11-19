---
title: "Postupy: generování fragmentu kódu XML z schématu XML | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2c128d2a-aaa6-4814-aa95-e07056afe338
caps.latest.revision: "2"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 1090d1509152aaa507220d3119977bb8e9252876
ms.sourcegitcommit: c0422a3d594ea5ae8fc03f1aee684b04f417522e
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/02/2017
---
# <a name="how-to-generate-an-xml-snippet-from-an-xml-schema"></a>Postupy: generování fragmentu kódu XML z schématu XML
Editor souborů XML má možnost k vygenerování XML fragmenty ze schématu schématu XML definition language (XSD). Například jako vytváření souboru XML, zatímco umístěný vedle názvu elementu, stisknete klávesu TAB k naplnění element s daty XML vygenerovat z informace o schématu pro daný element.  
  
 Tato funkce je dostupná u elementů jenom. Také platí následující pravidla:  
  
-   Element musí mít typ přidružené schéma; To znamená element musí být platná podle některé přidružené schéma. Typ schématu nemůže být abstraktní a musí obsahovat povinné atributy typu nebo požadované podřízené elementy.  
  
-   V editoru aktuálního elementu musí být prázdné bez atributů. Například následující jsou všechny platné  
  
    -   `<Account`  
  
    -   `<Account>`  
  
    -   `<Account></Account>`  
  
-   Kurzor musí být umístěné vpravo název elementu.  
  
Vygenerovaný fragment kódu obsahuje všechny povinné atributy a prvky. Pokud `minOccurs` je větší než jeden požadované minimální počet instancí tohoto prvku je zahrnuta v tomto fragmentu kódu, až do maximálního počtu instancí 100. Všechny pevné hodnoty zjištěné v výsledek schématu v pevné hodnoty v tomto fragmentu kódu. `xsd:any`a `xsd:anyAttribute` elementy jsou ignorovány a mít za následek žádná další fragment konstrukce.  
  
Výchozí hodnoty jsou generovány a jsou uvedené jako upravitelné hodnoty. Pokud schéma určí výchozí hodnotu, tato výchozí hodnota se používá. Ale pokud schéma výchozí hodnota je řetězec prázdný, editor generuje výchozí hodnoty následujícím způsobem:  
  
-   Pokud typ schématu obsahuje všechny omezující vlastnosti výčtu přímo nebo nepřímo prostřednictvím všechny členy typu union, první Výčtová hodnota nalezena v modelu objektu schématu se používá jako výchozí.  
  
-   Pokud je typ schématu atomickým typem, editor získá atomic typ a vloží název atomic typu. Pro odvozený typ jednoduchého používá základní jednoduchého typu. Pro typ seznamu atomic typ je `itemType`. Pro spojení, atomic typ je typ atomic prvního `memberType`.  
  
## <a name="example"></a>Příklad  
 Kroky v této části ukazují, jak použijete generované schématu XML fragment kódu funkci editoru XML.  
  
> [!NOTE]
>  Než zahájíte tyto postupy, uložte soubor schématu do místního počítače.  
  
#### <a name="to-create-a-new-xml-file-and-associate-it-with-an-xml-schema"></a>K vytvoření nového souboru XML a přidružte ji k schématu XML  
  
1.  Na **soubor** nabídky, přejděte na příkaz **nový**a klikněte na tlačítko **soubor**.  
  
2.  Vyberte **souboru XML** v **šablony** panelu a klikněte na tlačítko **otevřete**.  
  
     Nový soubor se otevře v editoru. Tento soubor obsahuje deklaraci XML výchozí `<?xml version="1.0" encoding="utf-8">`.  
  
3.  V okně vlastností dokumentu klikněte na tlačítko Procházet (**...** ) na **schémata** pole.  
  
     **XSD schémata** se zobrazí dialogové okno.  
  
4.  Klikněte na tlačítko **přidat**.  
  
     **Otevřete schématu XSD** se zobrazí dialogové okno.  
  
5.  Vyberte soubor schématu a klikněte na tlačítko **otevřete**.  
  
6.  Click **OK**.  
  
     Schéma XML je nyní přidružené k dokumentu XML.  
  
#### <a name="to-generate-an-xml-snippet"></a>Ke generování fragmentu kódu XML  
  
1.  Typ `<` v podokně editor.  
  
2.  Zobrazí se seznam členů možné položky:  
  
     **!--** přidání komentáře.  
  
     **! DOCTYPE** přidejte typ dokumentu.  
  
     **?** Chcete-li přidat instrukce pro zpracování.  
  
     **Obraťte se na** přidat kořenový element.  
  
3.  Vyberte **kontaktujte** ze seznamu členů a stiskněte klávesu ENTER.  
  
     Editor přidá počáteční značce `<Contact` a umisťuje kurzor po název elementu.  
  
4.  Stiskněte klávesu TAB pro generování kódu XML dat pro `Contact` element podle jeho informace o schématu.  
  
### <a name="input"></a>Vstup  
 Následující schéma soubor je používán návodu.  
  
```xml
<?xml version="1.0" encoding="utf-8" ?>  
<xs:schema elementFormDefault="qualified"  
           xmlns:xs="http://www.w3.org/2001/XMLSchema">  
  <xs:simpleType name="phoneType">  
    <xs:restriction base="xs:string">  
      <xs:enumeration value="Voice"/>  
      <xs:enumeration value="Fax"/>  
      <xs:enumeration value="Pager"/>  
    </xs:restriction>  
  </xs:simpleType>  
  <xs:element name="Contact">  
    <xs:complexType>  
      <xs:sequence>  
        <xs:element name="Name">  
          <xs:simpleType>  
            <xs:restriction base="xs:string"></xs:restriction>  
          </xs:simpleType>  
        </xs:element>  
        <xs:element name="Title"  
                    type="xs:string" />  
        <xs:element name="Phone"  
                    minOccurs="1"  
                    maxOccurs="unbounded">  
          <xs:complexType>  
            <xs:sequence>  
              <xs:element name="Number"  
                          minOccurs="1">  
                <xs:simpleType>  
                  <xs:restriction base="xs:string"></xs:restriction>  
                </xs:simpleType>  
              </xs:element>  
              <xs:element name="Type"  
                          default="Voice"  
                          minOccurs="1"  
                          type="phoneType"/>  
            </xs:sequence>  
          </xs:complexType>  
        </xs:element>  
      </xs:sequence>  
    </xs:complexType>  
  </xs:element>  
</xs:schema>  
```  
  
### <a name="output"></a>Výstup  
 Následuje XML data, která se generuje na základě informací schématu přidružené `Contact` elementu. Položky označen jako `bold` určit upravitelné pole v tomto fragmentu kódu XML.  
  
```xml
<Contact>  
  <Name>name</Name>  
  <Title>title</Title>  
  <Phone>  
    <Number>number</Number>  
    <Type>Voice</Type>  
  </Phone>  
</Contact>  
```  
  
## <a name="see-also"></a>Viz také  
 [Fragmenty kódu XML](../xml-tools/xml-snippets.md)   
 [Postupy: použití fragmenty kódu XML](../xml-tools/how-to-use-xml-snippets.md)