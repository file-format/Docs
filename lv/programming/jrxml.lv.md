{
  "date": "2019-10-11",
  "keywords": [
"jrxml",
"jrxml failu",
"jrxml faila formātā",
"faila formātā",
"programmēšana",
"jrxml faila lejupielāde",
".jrxml failu",
".jrxml"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par JRXML faila formātu un API, kas var atvērt un izveidot JRXML failus.",
  "title": "JRXML faila formāts",
  "linktitle": "JRXML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jrxm-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir JRXML fails?

JRXML failu izveido JasperReports, un tas satur dizaina definīciju populārā [XML](/web/xml/) faila formātā. Tajā tiek saglabāti visi dizaina elementi, piemēram, atskaites izkārtojums, teksta lauki, attēli, diagrammas, parametri un mainīgie. JasperReports ir Java bibliotēka, ko izmanto, lai programmatiski izveidotu pārskatus, izgūstot datus no aizmugursistēmas datu bāzēm un datu nesējiem.

## JRXML faila formāts

JRXML faili ir vienkārša teksta faili, kas izveidoti, pamatojoties uz XML faila formātu. JasperReport sistēma var apstrādāt dažāda veida datu avotus. Kad tiek kompilēts .jrxml fails, kā izvade tiek iegūts .jasper fails. Jrxml fails sastāv no sadaļu kopas. Dažas sadaļas satur informāciju, kas saistīta ar lapas fiziskajiem parametriem, piemēram, lapas izmēru, lauku izvietojumu un joslu augstumu, savukārt dažas sadaļas attiecas uz loģiskajiem raksturlielumiem, piemēram, parametru un mainīgo deklarāciju un vaicājuma definīciju. datu atlasei.

### JRXML faila piemērs

Vienkāršs JRXML faila piemērs ir parādīts zemāk.
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

Tālāk ir sniegta detalizēta informācija par piemēru.

`<queryString> ` − Tas ir tukšs (jo mēs nododam datus caur Java Beans). Parasti satur SQL priekšrakstu, kas izgūst pārskata rezultātu.

`<field name> ` - Šis elements tiek izmantots, lai kartētu datus no datu avotiem vai vaicājumiem pārskatu veidnēs. nosaukums tiek atkārtoti izmantots ziņojuma pamattekstā un ir reģistrjutīgs.

`<fieldDescription> ` – Šis elements kartē lauka nosaukumu ar atbilstošo elementu XML failā.

`<staticText> ` – Tas definē statisko tekstu, kas nav atkarīgs no datu avotiem, mainīgajiem, parametriem vai atskaites izteiksmēm.

`<band> ` − Joslas satur datus, kas tiek parādīti atskaitē.

## Atsauces

 * [JRXML — Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
 * [JRXML avoti un Jasper faili](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

