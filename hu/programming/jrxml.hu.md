{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml fájl", "jrxml fájlformátum", "fájlformátum", "programozás", "jrxml fájl letöltése", ".jrxml fájl", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a JRXML fájlformátumról és az API-król, amelyek képesek megnyitni és létrehozni JRXML fájlokat.",
  "title" :"JRXML fájlformátum",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a JRXML fájl?

A JRXML fájlt a JasperReports hoz létre, és népszerű [XML](/hu/web/xml/) fájlformátumban tartalmazza a tervezési definíciót. Tárolja az összes tervezési elemet, mint például a jelentés elrendezése, szövegmezők, képek, diagramok, paraméterek és változók. A JasperReports egy Java-könyvtár, amelyet jelentések programozott létrehozására használnak háttéradatbázisokból és adathordozókról való lekéréssel.

## JRXML fájlformátum

A JRXML fájlok egyszerű szöveges fájlok, amelyek az XML fájlformátum alapján jönnek létre. A JasperReport keretrendszer különféle típusú adatforrásokat képes kezelni. Amikor egy .jrxml fájlt lefordítanak, az .jasper fájlt eredményez kimenetként. A jrxml fájl egy sor szakaszból áll. Egyes részek az oldal fizikai jellemzőivel kapcsolatos információkat tartalmaznak, mint például az oldal mérete, a mezők elhelyezkedése és a sávok magassága, míg mások a logikai jellemzőkkel, például a paraméterek és változók deklarációjával, valamint a lekérdezés meghatározásával kapcsolatos információkat tartalmaznak. az adatok kiválasztásához.

### JRXML fájl példa

Az alábbiakban egy egyszerű JRXML fájl példa látható.
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

Az alábbiakban a példa részleteit közöljük.

`<queryString> ` − Ez üres (mivel adatokat továbbítunk a Java Beans-en). Általában tartalmazza az SQL utasítást, amely lekéri a jelentés eredményét.

`<field name> ` − Ez az elem adatforrásokból vagy lekérdezésekből származó adatok jelentéssablonokba való leképezésére szolgál. A név újra használatos a jelentéstörzsben, és megkülönbözteti a kis- és nagybetűket.

`<fieldDescription> ` − Ez az elem leképezi a mező nevét az XML fájl megfelelő elemével.

`<staticText> ` − Ez a statikus szöveget határozza meg, amely nem függ semmilyen adatforrástól, változótól, paramétertől vagy jelentéskifejezéstől.

`<band> ` − A sávok tartalmazzák az adatokat, amelyek a jelentésben jelennek meg.

## Hivatkozások

* [JRXML – Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML-források és Jasper-fájlok](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

