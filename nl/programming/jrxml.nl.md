{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml-bestand", "jrxml-bestandsindeling", "bestandsindeling", "programmeren", "jrxml-bestand downloaden", ".jrxml-bestand", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over JRXML-bestandsindeling en API's die JRXML-bestanden kunnen openen en maken.",
  "title" :"JRXML-bestandsindeling",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een JRXML-bestand?

Een JRXML-bestand is gemaakt door JasperReports en bevat een ontwerpdefinitie in het populaire [XML](/nl/web/xml/) bestandsformaat. Het slaat alle ontwerpelementen op, zoals rapportlay-out, tekstvelden, afbeeldingen, grafieken, parameters en variabelen. JasperReports is een Java-bibliotheek die wordt gebruikt voor het programmatisch maken van rapporten door gegevens op te halen uit backend-databases en opslagmedia.

## JRXML-bestandsindeling

JRXML-bestanden zijn platte tekstbestanden die zijn gemaakt op basis van het XML-bestandsformaat. JasperReport-framework kan verschillende soorten gegevensbronnen aan. Wanneer een .jrxml-bestand wordt gecompileerd, resulteert dit in een .jasper-bestand als uitvoer. Een jrxml-bestand bestaat uit een reeks secties. Sommige secties bevatten informatie met betrekking tot de fysieke kenmerken van de pagina, zoals de afmeting van de pagina, de positionering van de velden en de hoogte van de banden, terwijl sommige betrekking hebben op de logische kenmerken zoals de declaratie van de parameters en variabelen en de definitie van een zoekopdracht voor gegevensselectie.

### JRXML-bestandsvoorbeeld

Hieronder ziet u een eenvoudig JRXML-bestandsvoorbeeld.
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

Hieronder volgen de details van het voorbeeld.

`<queryString> ` − Dit is leeg (omdat we gegevens doorgeven via Java Beans). Bevat meestal de SQL-instructie, die het rapportresultaat ophaalt.

`<field name> ` − Dit element wordt gebruikt om gegevens uit gegevensbronnen of query's toe te wijzen aan rapportsjablonen. naam wordt hergebruikt in de hoofdtekst van het rapport en is hoofdlettergevoelig.

`<fieldDescription> ` − Dit element koppelt de veldnaam aan het juiste element in het XML-bestand.

`<staticText> ` − Dit definieert de statische tekst die niet afhankelijk is van gegevensbronnen, variabelen, parameters of rapportuitdrukkingen.

`<band> ` − Banden bevatten de gegevens die in het rapport worden weergegeven.

## Referenties

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML-bronnen en Jasper-bestanden](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

