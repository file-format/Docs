{
  "date": "2019-10-11",
  "keywords": [
"jrxml",
"jrxml failą",
"jrxml failo formatas",
"Dokumento formatas",
"programavimas",
"Parsisiųsti jrxml failą",
".jrxml failą",
".jrxml"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie JRXML failo formatą ir API, kurios gali atidaryti ir kurti JRXML failus.",
  "title": "JRXML failo formatas",
  "linktitle": "JRXML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jrxm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra JRXML failas?

JRXML failą sukuria JasperReports ir jame yra dizaino apibrėžimas populiariu [XML](/web/xml/) failo formatu. Jame saugomi visi dizaino elementai, tokie kaip ataskaitos išdėstymas, teksto laukai, vaizdai, diagramos, parametrai ir kintamieji. JasperReports yra Java biblioteka, naudojama programiniam ataskaitoms kurti, nuskaitant duomenis iš užpakalinių duomenų bazių ir laikmenų.

## JRXML failo formatas

JRXML failai yra paprasto teksto failai, sukurti remiantis XML failo formatu. JasperReport sistema gali apdoroti įvairių tipų duomenų šaltinius. Kai sukompiliuojamas .jrxml failas, kaip išvestis gaunamas .jasper failas. Jrxml failą sudaro sekcijų rinkinys. Kai kuriose skiltyse pateikiama informacija, susijusi su fizinėmis puslapio savybėmis, pvz., puslapio matmenimis, laukų padėtimi ir juostų aukščiu, o kai kuriuose – su loginėmis savybėmis, tokiomis kaip parametrų ir kintamųjų deklaravimas bei užklausos apibrėžimas. duomenų pasirinkimui.

### JRXML failo pavyzdys

Žemiau parodytas paprastas JRXML failo pavyzdys.
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

Toliau pateikiamos pavyzdžio detalės.

`<queryString> ` − Tai tuščia (kadangi mes perduodame duomenis per Java Beans). Paprastai yra SQL sakinys, kuris nuskaito ataskaitos rezultatą.

`<field name> ` − Šis elementas naudojamas duomenims iš duomenų šaltinių arba užklausų susieti į ataskaitų šablonus. pavadinimas pakartotinai naudojamas ataskaitos tekste ir jame skiriamos didžiosios ir mažosios raidės.

`<fieldDescription> ` − Šis elementas susieja lauko pavadinimą su atitinkamu elementu XML faile.

`<staticText> ` – Tai apibrėžia statinį tekstą, kuris nepriklauso nuo jokių duomenų šaltinių, kintamųjų, parametrų ar ataskaitos išraiškų.

`<band> ` − Juostose yra duomenys, kurie rodomi ataskaitoje.

## Nuorodos

 * [JRXML – Vikipedija](https://en.wikipedia.org/wiki/JasperReports#JRXML)
 * [JRXML šaltiniai ir Jasper failai](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

