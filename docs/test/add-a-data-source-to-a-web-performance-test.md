---
title: Přidání zdroje dat do testu výkonnosti webu v sadě Visual Studio
ms.date: 10/03/2016
ms.topic: conceptual
helpviewer_keywords:
- Web performance tests, walkthroughs
- Web performance tests, data binding (database)
ms.assetid: 2ada376d-f168-455d-9643-6acb535360c1
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 9539e8dec80afd1f334ca89e84a5130d8d47877e
ms.sourcegitcommit: 4667e6ad223642bc4ac525f57281482c9894daf4
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/20/2018
ms.locfileid: "36283286"
---
# <a name="add-a-data-source-to-a-web-performance-test"></a>Přidání zdroje dat do testu výkonnosti webu

Vázání dat různé hodnoty pro stejný test, třeba zajistit, aby poskytují různé hodnoty do svého formuláře odeslat parametry.

 ![Vazba dat do testu výkonnosti webu](../test/media/web_test_databinding_conceptual.png)

 Vytvoříme pomocí ukázkové aplikace ASP.NET. Má tři *.aspx* stránky – výchozí stránku, Red stránky a Blue stránku. Výchozí stránka má ovládací prvek přepínač zvolit red nebo blue a tlačítko pro odeslání. Další dvě *.aspx* stránky jsou velmi jednoduché. Jeden má popisek s názvem Red a dalších má popisek s názvem Blue. Když zvolíte odeslat na stránku výchozího zobrazujeme jedním z dalších stránek. Si můžete stáhnout [ColorWebApp](http://code.msdn.microsoft.com/Sample-ColorWebApp-76ff7506) ukázkové nebo postupujte podle společně s webovou aplikaci.

 ![Spuštění webové aplikace má být testována](../test/media/web_test_databinding_runwebapp.png)

 Řešení musí rovněž zahrnovat testu výkonnosti webu, který umožňuje prostřednictvím stránky webové aplikace.

 ![Řešení s testu výkonnosti webu](../test/media/web_test_databinding_solution.png)

## <a name="create-a-sql-database"></a>Vytvoření databáze SQL

1. Pokud nemáte Visual Studio Enterprise, si můžete stáhnout z [Visual Studio stáhne](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) stránky.

2. Vytvoření databáze SQL.

     ![Přidat novou databázi SQL.](../test/media/web_test_databinding_sql_addnewdb.png)

3. Vytvořte projekt databáze.

     ![Vytvoření nového projektu z databáze](../test/media/web_test_databinding_sql_addnewdbproject.png)

4. Přidání tabulky do projekt databáze.

     ![Přidá novou tabulku na projekt databáze](../test/media/web_test_databinding_sql_addnewdbtablename.png)

5. Přidáte pole do tabulky.

     ![Přidat pole do tabulky](../test/media/web_test_databinding_sql_addnewdbaddfields.png)

6. Publikujte k databázovému projektu.

     ![Publikování databáze projektu v Průzkumníku řešení](../test/media/web_test_databinding_sql_addnewdbpublish.png)

7. Přidání dat do polí.

     ![Přidání dat do pole](../test/media/web_test_databinding_sql_addnewfieldsadddata.png)

## <a name="add-the-data-source"></a>Přidejte tento zdroj dat

1. Přidání zdroje dat.

     ![Přidat zdroje dat do testu výkonnosti webu](../test/media/web_test_databinding_sql_adddatasource.png)

2. Vyberte typ zdroje dat a pojmenujte ji.

     ![Název databáze zdroje](../test/media/web_test_databinding_sql_adddatasourcedialog.png)

3. Umožňuje vytvořte připojení.

     ![Zvolte nové připojení](../test/media/web_test_databinding_sql_adddatasourcedialogconnectionnew.png)

     Zadejte podrobnosti připojení.

     ![Zadejte vlastnosti připojení databáze SQL](../test/media/web_test_databinding_sql_adddatasourcedialogconnection.png)

4. Vyberte tabulku, kterou chcete použít pro svůj test.

     ![Přidat jako zdroj dat v tabulce barev](../test/media/web_test_databinding_sql_adddatasourcedialogaddtable.png)

     Tabulka je vázána na test.

     ![Přidat uzel zdroje dat do testu výkonnosti webu](../test/media/web_test_databinding_requestnodeadded_mdb.png)

5. Uložte test.

## <a name="bind-the-data"></a>Vytvoření vazby data

1. Vytvoření vazby **ColorName** pole.

     ![Vytvoření vazby pole ColorName RadioButtonList1 hodnotu](../test/media/web_test_databinding_sql_binddatasource.png)

2. Otevřete *Local.testsettings* souboru v **Průzkumníku řešení** a vyberte **jeden spustit na řádek zdroje dat** možnost.

     ![Úpravy souborů nastavení testů](../test/media/web_test_databinding_sql_testsettings.png)

3. Uložte testu výkonnosti webu.

## <a name="run-the-test-with-the-data"></a>Spusťte test s daty

1. Spuštění testu.

     ![Spuštění testu výkonnosti webu Ověření vazby](../test/media/web_test_databinding_sql_runtest.png)

     Pro každý řádek dat se zobrazují dvě spustí. Spustit 1 odešle požadavek stránku *Red.aspx*, a spusťte 2 odešle požadavek stránku *Blue.aspx*.

     ![Výsledky testu](../test/media/web_test_databinding_sql_runresults.png)

     Při vytvoření vazby ke zdroji dat, může narušit výchozí pravidlo adresa URL odpovědi. V takovém případě Chyba v spustit 2 je způsobená pravidla, která očekává *Red.aspx* stránky z původní testovací záznam, ale datové vazby teď přesměruje, aby *Blue.aspx* stránky.

2. Opravte chybu ověření odstraněním **adresa URL odpovědi** ověřovací pravidlo a opakujte spuštění testu.

     ![Odstranit pravidlo ověření adresa URL odpovědi](../test/media/web_test_databinding_sql_deleteresponseurl.png)

     Použití datových vazeb předá teď testu výkonnosti webu.

     ![Test předá použití datových vazeb](../test/media/web_test_databinding_sql_deleteresponseurlrunresults.png)

## <a name="q--a"></a>Dotazy a odpovědi

### <a name="q-what-databases-can-i-use-as-a-data-source"></a>Otázka: jaký databáze můžete použít jako zdroj dat?

**Odpověď:** můžete použít následující:

- Microsoft SQL Azure.

- Všechny verze systému Microsoft SQL Server 2005 nebo novější.

- Soubor databáze Microsoft SQL Server (včetně SQL Express).

- Microsoft ODBC.

- Soubor aplikace Microsoft Access pomocí poskytovatele rozhraní .NET Framework pro OLE DB.

- Oracle 7.3, 8i, 9i nebo 10g.

### <a name="q-how-do-i-use-a-comma-separated-value-csv-text-file-as-a-data-source"></a>Otázka: jak používat textový soubor čárkami oddělených hodnot (CSV) jako zdroj dat?

**Odpověď:** tady je jak:

1. Vytvořte složku pro uspořádání artefakty databáze projekty a přidejte položku.

     ![Přidat novou položku do složky dat](../test/media/web_test_databinding_foldernewitem.png)

2. Vytvořte textový soubor.

     ![Název nového textového souboru ColorData.csv](../test/media/web_test_databinding_foldernewitemtextfile.png)

3. Upravit textový soubor a přidejte následující:

    ```text
    ColorId, ColorName
    0,Red
    1,Blue
    ```

4. Postupujte podle kroků v [přidejte tento zdroj dat](#add-the-data-source), zvolte soubor CSV jako zdroj dat, ale.

     ![Zadejte název a vyberte soubor CSV](../test/media/web_test_databinding_adddatasourcedialog.png)

### <a name="q-what-if-my-existing-csv-file-does-not-contain-column-headers"></a>Otázka: Co když Můj existující soubor CSV neobsahuje záhlaví sloupců?

**Odpověď:** Pokud záhlaví sloupců nelze přidat, můžete použít soubor popisu schématu do souboru CSV považovat za databázi.

1. Přidat nový textový soubor s názvem *schema.ini*.

     ![Přidejte soubor schema.ini](../test/media/web_test_databinding_schemafile.png)

2. Upravit *schema.ini* soubor, abyste přidali informace, které popisuje strukturu vaše data. Například soubor schématu s popisem soubor CSV může vypadat například takto:

    ```text
    [testdata.csv]
    ColNameHeader=False
    ```

3. Přidání zdroje dat na test.

     ![Přidat zdroje dat do testu výkonnosti webu](../test/media/web_test_databinding_sql_adddatasource.png)

4. Pokud používáte *schema.ini* souboru, zvolte **databáze** (ne soubor CSV) jako zdroje dat a pojmenujte ho.

     ![Přidat zdroje dat databáze](../test/media/web_test_databinding_adddatasourcecolortext.png)

5. Vytvoření nového připojení.

     ![Zvolte nové připojení](../test/media/web_test_databinding_sql_adddatasourcedialogconnectionnew.png)

6. Vyberte zprostředkovatele dat .NET Framework pro OLE DB.

     ![Vyberte zprostředkovatele dat .NET framework OLE DB](../test/media/web_test_databinding_adddatasourcecolortext2.png)

7. Zvolte **rozšířené**.

     ![Vyberte rozšířené](../test/media/web_test_databinding_advanced.png)

8. Pro vlastnost poskytovatele, vyberte Microsoft.Jet.OLEDB.4.0 a pak nastavte **rozšířené vlastnosti** k textu. ZÁHLAVÍ = NE.

     ![Použít rozšířené vlastnosti](../test/media/web_test_databinding_advancedproperties.png)

9. Zadejte název složky, která obsahuje soubor schématu a vyzkoušejte připojení.

     ![Zadejte cestu ke složce dat](../test/media/web_test_databinding_adddatasourcecolortext5.png)

10. Vyberte soubor CSV, který chcete použít.

     ![Vyberte textový soubor](../test/media/web_test_databinding_adddatasourcecolortext6.png)

     Po dokončení, zobrazí se soubor CSV jako tabulku.

     ![Zdroj dat přidat k testování](../test/media/web_test_databinding_adddatasourcecolortext7.png)

### <a name="q-how-do-i-use-an-xml-file-as-a-data-source"></a>Otázka: jak používat soubor XML jako zdroj dat?

**Odpověď:** Ano.

1. Vytvořte složku pro uspořádání artefakty databáze projekty a přidejte položku.

     ![Přidat novou položku do složky dat](../test/media/web_test_databinding_foldernewitem.png)

2. Vytvořte soubor XML.

     ![Přidejte soubor ColorData.xml](../test/media/web_test_databinding_additemxmlfile.png)

3. Upravte soubor XML a přidejte data:

    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <ColorData>
        <Color>
            <ColorId>0</ColorId>
            <ColorName>Red</ColorName>
        </Color>
        <Color>
            <ColorId>1</ColorId>
            <ColorName>Blue</ColorName>
        </Color>
    </ColorData>
    ```

4. Postupujte podle kroků v [přidejte tento zdroj dat](#add-the-data-source), vyberte soubor XML jako zdroj dat, ale.

     ![Zadejte název a vyberte soubor XML](../test/media/web_test_databinding_adddatasourcedialogxml.png)

### <a name="q-can-i-add-data-binding-to-a-web-service-request-that-uses-soap"></a>Otázka: je možné přidat datové vazby k požadavku webové služby, který používá SOAP?

**Odpověď:** Ano, je nutné změnit SOAP XML ručně.

1. Zvolte žádosti webové služby ve stromové struktuře požadavku a v okně Vlastnosti a potom vyberte se třemi tečkami (...) ve vlastnosti řetězec textu.

     ![Upravit řetězec textu webové služby](../test/media/web_test_databinding_webservicerequest.png)

2. Nahraďte hodnoty v těle protokolu SOAP hodnotami vázané na data pomocí následující syntaxe:

    ```xml
    {{DataSourceName.TableName.ColumnName}}
    ```

    Například pokud máte následující kód:

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
        <soap:Body>
            <CheckStatus xmlns="http://tempuri.org/">
                <userName>string</userName> <password>string</password> <orderID>int</orderID>
            </CheckStatus>
        </soap:Body>
    </soap:Envelope>
    ```

    Můžete ji změnit k tomuto:

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
        <soap:Body>
            <CheckStatus xmlns="http://tempuri.org/">
                <userName>{{DataSourceName.Users.Name}}</userName> <password>{{DataSourceName.Users.Password}}</password> <orderID>{{DataSourceName.Orders.OrderID}}</orderID>
            </CheckStatus>
        </soap:Body>
    </soap:Envelope>
    ```

3. Uložte test.