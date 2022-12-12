{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "soubor jrxml", "formát souboru jrxml", "formát souboru", "programování", "stažení souboru jrxml", "soubor .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů JRXML a rozhraních API, která mohou otevírat a vytvářet soubory JRXML.",
  "title" :"Formát souboru JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor JRXML?

Soubor JRXML je vytvořen JasperReports a obsahuje definici návrhu v oblíbeném formátu souboru [XML](/cs/web/xml/). Ukládá všechny prvky návrhu, jako je rozvržení sestavy, textová pole, obrázky, grafy, parametry a proměnné. JasperReports je knihovna Java používaná pro vytváření sestav programově načítáním dat z backendových databází a úložných médií.

## Formát souboru JRXML

Soubory JRXML jsou soubory ve formátu prostého textu, které jsou vytvořeny na základě formátu souboru XML. Rámec JasperReport dokáže zpracovat různé druhy zdrojů dat. Když je kompilován soubor .jrxml, výsledkem je soubor .jasper jako výstup. Soubor jrxml se skládá ze sady sekcí. Některé části obsahují informace související s fyzickými charakteristikami stránky, jako je rozměr stránky, umístění polí a výška pásů, zatímco některé se týkají logických charakteristik, jako je deklarace parametrů a proměnných a definice dotazu. pro výběr dat.

### Příklad souboru JRXML

Níže je uveden jednoduchý příklad souboru JRXML.
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

Níže jsou uvedeny podrobnosti příkladu.

`<queryString> ` − Toto je prázdné (protože předáváme data přes Java Beans). Obvykle obsahuje příkaz SQL, který načte výsledek sestavy.

`<field name> ` − Tento prvek se používá k mapování dat ze zdrojů dat nebo dotazů do šablon sestav. název je znovu použit v těle sestavy a rozlišuje malá a velká písmena.

`<fieldDescription> ` − Tento prvek mapuje název pole s příslušným prvkem v souboru XML.

`<staticText> ` − Toto definuje statický text, který nezávisí na žádných zdrojích dat, proměnných, parametrech nebo výrazech sestavy.

`<band> ` − Pásma obsahují data, která jsou zobrazena v sestavě.

## Reference

* [JRXML – Wikipedie](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Zdroje JRXML a soubory Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

