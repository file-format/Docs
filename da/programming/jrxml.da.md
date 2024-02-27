{
  "date": "2019-10-11",
  "keywords": [
"jrxml",
"jrxml fil",
"jrxml filformat",
"filformat",
"programmering",
"Download jrxml fil",
".jrxml-fil",
".jrxml"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om JRXML filformat og API'er, der kan åbne og oprette JRXML filer.",
  "title": "JRXML filformat",
  "linktitle": "JRXML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jrxm-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en JRXML fil?

En JRXML-fil er oprettet af JasperReports og indeholder designdefinition i populært [XML](/web/xml/)-filformat. Den gemmer alle designelementer såsom rapportlayout, tekstfelter, billeder, diagrammer, parametre og variabler. JasperReports er et Java-bibliotek, der bruges til at oprette rapporter programmatisk ved at hente data fra backend-databaser og lagringsmedier.

## JRXML filformat

JRXML-filer er almindelige tekstfiler, der er oprettet baseret på XML-filformatet. JasperReport framework kan håndtere forskellige slags datakilder. Når en .jrxml-fil kompileres, resulterer det i en .jasper-fil som output. En jrxml-fil består af et sæt sektioner. Nogle sektioner indeholder information relateret til sidens fysiske egenskaber såsom sidedimension, placering af felterne og højden af båndene, mens nogle vedrører de logiske karakteristika såsom deklaration af parametre og variabler og definitionen af en forespørgsel til datavalg.

### JRXML fil eksempel

Et simpelt JRXML-fileksempel er vist nedenfor.
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

Følgende er detaljerne i eksemplet.

`<queryString> ` − Dette er tomt (da vi sender data gennem Java Beans). Indeholder normalt SQL-sætningen, som henter rapportresultatet.

`<field name> ` − Dette element bruges til at kortlægge data fra datakilder eller forespørgsler til rapportskabeloner. navn genbruges i rapportens krop og skelner mellem store og små bogstaver.

`<fieldDescription> ` − Dette element tilknytter feltnavnet med det relevante element i XML-filen.

`<staticText> ` − Dette definerer den statiske tekst, der ikke afhænger af nogen datakilder, variabler, parametre eller rapportudtryk.

`<band> ` − Bånd indeholder dataene, som vises i rapporten.

## Referencer

 * [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
 * [JRXML-kilder og Jasper-filer](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

