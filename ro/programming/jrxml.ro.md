{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "fișier jrxml", "format fișier jrxml", "format fișier", "programare", "descărcare fișier jrxml", "fișier .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier JRXML și despre API-urile care pot deschide și crea fișiere JRXML.",
  "title" :"Format fișier JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier JRXML?

Un fișier JRXML este creat de JasperReports și conține definiția designului în format popular de fișier [XML](/ro/web/xml/). Stochează toate elementele de design, cum ar fi aspectul raportului, câmpurile de text, imaginile, diagramele, parametrii și variabilele. JasperReports este o bibliotecă Java folosită pentru crearea de rapoarte în mod programatic prin preluarea datelor din baze de date backend și medii de stocare.

## Format de fișier JRXML

Fișierele JRXML sunt fișiere text simplu care sunt create pe baza formatului de fișier XML. Cadrul JasperReport poate gestiona diferite tipuri de surse de date. Când un fișier .jrxml este compilat, rezultă fișierul .jasper ca rezultat. Un fișier jrxml constă dintr-un set de secțiuni. Unele secțiuni conțin informații legate de caracteristicile fizice ale paginii, cum ar fi dimensiunea paginii, poziționarea câmpurilor și înălțimea benzilor, în timp ce unele se referă la caracteristicile logice precum declararea parametrilor și variabilelor și definirea unei interogări. pentru selectarea datelor.

### Exemplu de fișier JRXML

Un exemplu simplu de fișier JRXML este prezentat mai jos.
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

Mai jos sunt detaliile exemplului.

`<queryString> ` − Acesta este gol (deoarece trecem date prin Java Beans). De obicei, conține instrucțiunea SQL, care preia rezultatul raportului.

`<field name> ` − Acest element este utilizat pentru a mapa datele din surse de date sau interogări, în șabloane de raport. numele este reutilizat în corpul raportului și face distincție între majuscule și minuscule.

`<fieldDescription> ` − Acest element mapează numele câmpului cu elementul corespunzător din fișierul XML.

`<staticText> ` − Aceasta definește textul static care nu depinde de nicio sursă de date, variabile, parametri sau expresii de raport.

`<band> ` − Benzile conțin datele, care sunt afișate în raport.

## Referințe

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Surse JRXML și fișiere Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

