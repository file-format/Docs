{
  "date" : "2019-10-11",
  "keywords" :["jrxml", "plik jrxml", "format pliku jrxml", "format pliku", "programowanie", "pobieranie pliku jrxml", "plik .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku JRXML i interfejsy API, które mogą otwierać i tworzyć pliki JRXML.",
  "title" :"Format Pliku JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik JRXML?

Plik JRXML jest tworzony przez JasperReports i zawiera definicję projektu w popularnym formacie pliku [XML](/pl/web/xml/). Przechowuje wszystkie elementy projektu, takie jak układ raportu, pola tekstowe, obrazy, wykresy, parametry i zmienne. JasperReports to biblioteka Java używana do programowego tworzenia raportów poprzez pobieranie danych z baz danych zaplecza i nośników pamięci.

## Format pliku JRXML

Pliki JRXML to zwykłe pliki tekstowe tworzone na podstawie formatu pliku XML. Framework JasperReport może obsługiwać różne rodzaje źródeł danych. Gdy plik .jrxml jest kompilowany, wynikiem jest plik .jasper jako dane wyjściowe. Plik jrxml składa się z zestawu sekcji. Niektóre sekcje zawierają informacje związane z cechami fizycznymi strony, takimi jak wymiary strony, położenie pól, wysokość pasm, a inne dotyczą cech logicznych, takich jak deklaracja parametrów i zmiennych oraz definicja zapytania do wyboru danych.

### Przykład pliku JRXML

Prosty przykład pliku JRXML pokazano poniżej.
```
<a name="kanchor14"></a><?xml version="1.0" encoding="UTF-8"?>
<jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports
        http://jasperreports.sourceforge.net/xsd/jasperreport.xsd"
      name="My first report" pageWidth="595" pageHeight="842" columnWidth="535"
      leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20">
  <queryString language="SQL">
    <![CDATA[select * from address order by city]]>
  </queryString>
  <field name="ID" class="java.lang.Integer">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="FIRSTNAME" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="LASTNAME" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="STREET" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
  <field name="CITY" class="java.lang.String">
    <fieldDescription><![CDATA[]]></fieldDescription>
  </field>
```
```
<group name="CITY">
    <groupExpression><![CDATA[$F{CITY}]]></groupExpression>
    <groupHeader>
      <band height="27">
        <staticText>
          <reportElement mode="Opaque" x="0" y="0" width="139" height="27"
          forecolor="#FFFFFF" backcolor="#000000"/>
          <textElement>
            <font size="18"/>
          </textElement>
        <text><![CDATA[CITY]]></text>
      </staticText>
      <textField hyperlinkType="None">
        <reportElement mode="Opaque" x="139" y="0" width="416" height="27"
        forecolor="#FFFFFF" backcolor="#000000"/>
        <textElement>
          <font size="18" isBold="true"/>
        </textElement>
        <textFieldExpression class="java.lang.String"><![CDATA[$F{CITY}]]>
        </textFieldExpression>
      </textField>
    </band>
  </groupHeader>
  <groupFooter>
    <band height="8">
      <line direction="BottomUp">
        <reportElement key="line" x="1" y="4" width="554" height="1"/>
      </line>
    </band>
  </groupFooter>
</group>

<background>
  <band/>
</background>
  <title>
    <band height="58">
      <line>
        <reportElement x="0" y="8" width="555" height="1"/>
      </line>
      <line>
        <reportElement positionType="FixRelativeToBottom" x="0" y="51" width="555"
             height="1"/>
      </line>

      <staticText>
        <reportElement x=”65” y=”13” width ”424” height=”35”/>
        <textElement textAlignment=”Center”>
          <font size=”26” isBold=”true”/>
        </textElement>
      <text><![CDATE[Classic template]]> </text>
    </staticText>
</band>
</title>
  <pageHeader>
    <band/>
  </pageHeader>
  <columnHeader>
    <band height="18">
      <staticText>
        <reportElement mode="Opaque" x="0" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[ID]]></text>
      </staticText>
      <staticText>
        <reportElement mode="Opaque" x="138" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[FIRSTNAME]]></text>
      </staticText>
      <staticText>
        <reportElement mode="Opaque" x="276" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[LASTNAME]]></text>
      </staticText>
      <staticText>
        <reportElement mode="Opaque" x="414" y="0" width="138" height="18"
        forecolor="#FFFFFF" backcolor="#999999"/>
        <textElement>
          <font size="12"/>
        </textElement>
        <text><![CDATA[STREET]]></text>
      </staticText>
    </band>
  </columnHeader>
```

Poniżej znajdują się szczegóły przykładu.

`<queryString> ` − To jest puste (ponieważ przekazujemy dane przez Java Beans). Zwykle zawiera instrukcję SQL, która pobiera wynik raportu.

`<field name> ` − Ten element służy do mapowania danych ze źródeł danych lub zapytań do szablonów raportów. nazwa jest ponownie używana w treści raportu i rozróżniana jest wielkość liter.

`<fieldDescription> ` − Ten element odwzorowuje nazwę pola na odpowiedni element w pliku XML.

`<staticText> ` − Definiuje tekst statyczny, który nie zależy od żadnych źródeł danych, zmiennych, parametrów ani wyrażeń raportu.

`<band> ` − Pasma zawierają dane, które są wyświetlane w raporcie.

## Bibliografia

* [JRXML – Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Źródła JRXML i pliki Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

