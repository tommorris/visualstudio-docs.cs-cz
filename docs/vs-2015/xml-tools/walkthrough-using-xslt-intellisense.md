---
title: 'Návod: Používání XSLT IntelliSense | Dokumentace Microsoftu'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 079d95ac-2eaf-4ae1-9cd3-2c81a961a942
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5a5a773b17d5393d15a4eb9a5947fe1e3215d784
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42627666"
---
# <a name="walkthrough-using-xslt-intellisense"></a>Návod: Používání IntelliSense XSLT
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nejnovější verzi tohoto tématu můžete najít v [návod: používání IntelliSense XSLT](https://docs.microsoft.com/visualstudio/xml-tools/walkthrough-using-xslt-intellisense).  
  
  
Tento návod ukazuje, jak pomocí technologie IntelliSense XSLT na hodnotu automatické dokončení některých atributů.  
  
### <a name="to-use-intellisense-in-the-name-attribute-of-xslwith-param-and-xslcall-template-elements"></a>Použití technologie IntelliSense v atributu name xsl: s param a Call-šablony elementů  
  
1.  Vytvořte nový soubor XSLT a zkopírujte následující kód:  
  
    ```  
    <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">  
    <!-- These 2 elements effectively assign  
         $messages = resources/en.xml/<messages>,  
         then $messages is used in the "localized-message" template.  -->  
    <xsl:param name="lang">en</xsl:param>  
    <xsl:variable name="messages"  
          select="document(concat('resources/', $lang, '.xml'))/messages"/>   
  
    <xsl:template name="msg23" match="msg23">  
    </xsl:template>  
  
    <xsl:template name="localized-message">  
      <xsl:param name="msgcode"/>  
      <!-- Show message string. -->  
      <xsl:message terminate="yes">  
        <xsl:value-of select="$messages/message[@name=$msgcode]"/>  
      </xsl:message>  
    </xsl:template>  
    </xsl:stylesheet>  
    ```  
  
2.  Kurzor po vložení `<xsl:template name="msg23" match="msg23">` a stiskněte klávesu ENTER. Začněte psát následující `xsl:call-template` element:  
  
    ```  
    <xsl:call-template name="localized-message">  
    </xsl:call-template>  
    ```  
  
     Seznam názvů šablony se zobrazí v `name=""` atribut `xsl:call-template` element během psaní.  
  
3.  Kurzor po vložení `<xsl:call-template name="localized-message">` a stiskněte klávesu ENTER. Začněte psát následující `xsl:with-param` element:  
  
    ```  
    <xsl:with-param name="msgcode">msg23</xsl:with-param>  
    ```  
  
     Seznam názvů parametrů se zobrazí v `name=""` atribut `xsl:with-param` elementu.  
  
### <a name="to-use-intellisense-in-the-mode-attribute-of-an-xslapply-templates-element"></a>Použití technologie IntelliSense v režimu atribut xsl: použít šablony – element  
  
1.  Vytvořte nový soubor XSLT a zkopírujte následující kód:  
  
    ```  
    <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">  
      <xsl:template match="/">  
        <HTML>  
          <BODY>  
            <TABLE>  
              <xsl:apply-templates select="customers/customer">  
                <xsl:sort select="state"/>  
                <xsl:sort select="name"/>  
              </xsl:apply-templates>  
            </TABLE>  
          </BODY>  
        </HTML>  
      </xsl:template>  
      <xsl:template match="customer">  
        <TR>  
          <xsl:apply-templates select="name" />  
          <xsl:apply-templates select="address" />  
          <xsl:apply-templates select="phone" />  
        </TR>  
      </xsl:template>  
      <xsl:template match="name">  
        <TD STYLE="font-size:14pt font-family:serif">  
          <xsl:apply-templates />  
        </TD>  
      </xsl:template>  
      <xsl:template match="address">  
        <TD>  
          <xsl:apply-templates />  
        </TD>  
      </xsl:template>  
      <xsl:template match="phone">  
        <TD>  
          <xsl:apply-templates />  
        </TD>  
      </xsl:template>  
      <xsl:template match="phone" mode="accountNumber">  
        <xsl:param name="Area_Code"/>  
        <TD STYLE="font-style:italic">  
          1-<xsl:value-of select="."/>-001  
        </TD>  
      </xsl:template>  
    </xsl:stylesheet>  
    ```  
  
2.  Kurzor po vložení `<xsl:apply-templates select="phone" />` a stiskněte klávesu ENTER. Začněte psát následující `xsl: apply-templates` element:  
  
    ```  
    <xsl:apply-templates select="phone"  mode="accountNumber">  
    ```  
  
     Seznam režimů šablony se zobrazí v `mode=""` atribut `xsl:apply-templates` elementu.  
  
### <a name="to-use-intellisense-in-the-stylesheet-prefix-and-result-prefix-attributes-of-an-xslnamespace-alias-element"></a>Použití technologie IntelliSense v atributech šablony stylů předpony a předpon výsledek XSL: Namespace-alias – element  
  
1.  Vytvořte nový soubor XSLT a zkopírujte následující kód:  
  
    ```  
    <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:alt="http://www.w3.org/1999/XSL/Transform-alternate"  
    version="1.0">  
      <xsl:param name="browser" select="'InternetExplorer'"/>  
      <xsl:template match="/">  
        <alt:stylesheet>  
          <xsl:choose>  
            <xsl:when test="$browser='InternetExplorer'">  
              <alt:import href="IERoutines.xsl"/>  
              <alt:template match="/">  
                <div>  
                  <alt:call-template name="showTable"/>  
                </div>  
              </alt:template>  
            </xsl:when>  
            <xsl:otherwise>  
              <alt:import href="OtherBrowserRoutines.xsl"/>  
              <alt:template match="/">  
                <div>  
                  <alt:call-template name="showTable"/>  
                </div>  
              </alt:template>  
            </xsl:otherwise>  
          </xsl:choose>  
        </alt:stylesheet>  
      </xsl:template>  
    </xsl:stylesheet>  
    ```  
  
2.  Kurzor po vložení `<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:alt="http://www.w3.org/1999/XSL/Transform-alternate" version="1.0">` a stiskněte klávesu ENTER. Začněte psát následující `xsl:namespace-alias` element:  
  
    ```  
    <xsl:namespace-alias stylesheet-prefix="alt" result-prefix="xsl"/>  
    ```  
  
     Všimněte si, jak se nacházela v seznamu předpony `stylesheet-prefix` a `result-prefix` atributy `xsl:namespace-alias` elementu.  
  
## <a name="see-also"></a>Viz také  
 [Funkce IntelliSense editoru XML](../xml-tools/xml-editor-intellisense-features.md)



