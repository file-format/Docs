{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml-Datei", "jrxml-Dateiformat", "Dateiformat", "Programmierung", "jrxml-Datei-Download", ".jrxml-Datei", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das JRXML-Dateiformat und APIs, die JRXML-Dateien öffnen und erstellen können.",
  "title" :"JRXML-Dateiformat",
  "linktitle" :"JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine JRXML-Datei?

Eine JRXML-Datei wird von JasperReports erstellt und enthält Designdefinitionen im gängigen Dateiformat [XML](/de/web/xml/). Es speichert alle Designelemente wie Berichtslayout, Textfelder, Bilder, Diagramme, Parameter und Variablen. JasperReports ist eine Java-Bibliothek, die zum programmgesteuerten Erstellen von Berichten verwendet wird, indem Daten aus Backend-Datenbanken und Speichermedien abgerufen werden.

## JRXML-Dateiformat

JRXML-Dateien sind reine Textdateien, die basierend auf dem XML-Dateiformat erstellt werden. Das JasperReport-Framework kann verschiedene Arten von Datenquellen verarbeiten. Wenn eine .jrxml-Datei kompiliert wird, führt dies zu einer .jasper-Datei als Ausgabe. Eine jrxml-Datei besteht aus einer Reihe von Abschnitten. Einige Abschnitte enthalten Informationen zu den physikalischen Eigenschaften der Seite, wie z. B. Seitenabmessungen, Positionierung der Felder und Höhe der Bänder, während andere die logischen Eigenschaften betreffen, z. B. die Deklaration der Parameter und Variablen und die Definition einer Abfrage zur Datenauswahl.

### JRXML-Dateibeispiel

Unten sehen Sie ein einfaches Beispiel für eine JRXML-Datei.
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

Es folgen die Details des Beispiels.

`<queryString> ` − Dies ist leer (da wir Daten durch Java Beans leiten). Enthält normalerweise die SQL-Anweisung, die das Berichtsergebnis abruft.

`<field name> ` − Dieses Element wird verwendet, um Daten aus Datenquellen oder Abfragen Berichtsvorlagen zuzuordnen. name wird im Berichtstext wiederverwendet und es wird zwischen Groß- und Kleinschreibung unterschieden.

`<fieldDescription> ` − Dieses Element ordnet den Feldnamen dem entsprechenden Element in der XML-Datei zu.

`<staticText> ` − Dies definiert den statischen Text, der nicht von Datenquellen, Variablen, Parametern oder Berichtsausdrücken abhängt.

`<band> ` − Bänder enthalten die Daten, die im Bericht angezeigt werden.

## Verweise

* [JRXML – Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML-Quellen und Jasper-Dateien] (https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

