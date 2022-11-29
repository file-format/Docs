{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml-fil", "jrxml-filformat", "filformat", "programmering","jrxml-filnedladdning", ".jrxml-fil", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om JRXML-filformat och API:er som kan öppna och skapa JRXML-filer.",
  "title" :"JRXML filformat",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en JRXML fil?

En JRXML-fil skapas av JasperReports och innehåller designdefinition i populära [XML](/sv/web/xml/) filformat. Den lagrar alla designelement som rapportlayout, textfält, bilder, diagram, parametrar och variabler. JasperReports är ett Java-bibliotek som används för att skapa rapporter programmatiskt genom att hämta data från backend-databaser och lagringsmedia.

## JRXML filformat

JRXML-filer är vanliga textfiler som skapas baserat på XML-filformatet. JasperReport-ramverket kan hantera olika typer av datakällor. När en .jrxml-fil kompileras resulterar det i en .jasper-fil som utdata. En jrxml-fil består av en uppsättning sektioner. Vissa avsnitt innehåller information relaterad till sidans fysiska egenskaper såsom sidans dimension, placeringen av fälten och höjden på banden, medan vissa gäller de logiska egenskaperna såsom deklaration av parametrar och variabler och definitionen av en fråga för val av data.

### JRXML-filexempel

Ett enkelt JRXML-filexempel visas nedan.
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

Följande är detaljerna i exemplet.

`<queryString> ` − Det här är tomt (eftersom vi skickar data genom Java Beans). Innehåller vanligtvis SQL-satsen, som hämtar rapportresultatet.

`<field name> ` − Detta element används för att mappa data från datakällor eller frågor till rapportmallar. namnet återanvänds i rapportens kropp och är skiftlägeskänsligt.

`<fieldDescription> ` − Detta element mappar fältnamnet med lämpligt element i XML-filen.

`<staticText> ` − Detta definierar den statiska texten som inte är beroende av några datakällor, variabler, parametrar eller rapportuttryck.

`<band> ` − Band innehåller data som visas i rapporten.

## Referenser

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML-källor och Jasper-filer](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

