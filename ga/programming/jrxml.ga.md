{
  "date": "2019-10-11",
  "keywords": [
"jrxml",
"comhad jrxml",
"Formáid comhaid jrxml",
"formáid comhaid",
"ríomhchlárú",
"Jrxml comhad a íoslódáil",
".jrxml comhad",
".jrxml"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid JRXML agus APIanna ar féidir comhaid JRXML a oscailt agus a chruthú.",
  "title": "Formáid Comhaid JRXML",
  "linktitle": "JRXML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jrxm-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad JRXML ann?

Cruthaíonn JasperReports comhad JRXML agus tá sainmhíniú dearaidh ann i bhformáid chomhaid [XML](/web/xml/) a bhfuil an-tóir air. Stórálann sé na heilimintí dearaidh go léir ar nós leagan amach tuairiscí, réimsí téacs, íomhánna, cairteacha, paraiméadair, agus athróga. Is leabharlann Java í JasperReports a úsáidtear chun tuarascálacha a chruthú go ríomhchláraithe trí shonraí a aisghabháil ó bhunachair shonraí inneall agus ó mheáin stórála.

## Formáid Comhaid JRXML

Is comhaid gnáth-théacs iad comhaid JRXML a chruthaítear bunaithe ar fhormáid comhaid XML. Is féidir le creat JasperReport cineálacha éagsúla foinsí sonraí a láimhseáil. Nuair a chuirtear comhad .jrxml le chéile, bíonn comhad .jasper mar aschur mar thoradh air. Tá comhad jrxml comhdhéanta de shraith alt. Cuimsíonn roinnt rannóg faisnéis a bhaineann le tréithe fisiceacha an leathanaigh, mar shampla toise an leathanaigh, suíomh na réimsí, agus airde na mbannaí, agus baineann cuid acu le tréithe loighciúla amhail dearbhú na bparaiméadar agus na n-athróg agus an sainmhíniú ar cheist. le haghaidh roghnú sonraí.

### Sampla comhaid JRXML

Taispeántar sampla comhad simplí JRXML thíos.
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

Seo a leanas sonraí an tsampla.

`<queryString> ` - Tá sé seo folamh (mar táimid ag seoladh sonraí trí Pónairí Java). Go hiondúil tá an ráiteas SQL, a aisghabhann toradh na tuarascála.

`<field name> ` - Úsáidtear an eilimint seo chun sonraí ó fhoinsí sonraí nó ceisteanna a mhapáil, i dteimpléid tuairisce. athúsáidtear an t-ainm sa chomhlacht tuairisce agus tá sé cás-íogair.

`<fieldDescription> ` - Mapálann an eilimint seo ainm na páirce leis an eilimint chuí sa chomhad XML.

`<staticText> ` - Sainmhíníonn sé seo an téacs statach nach bhfuil ag brath ar aon fhoinsí sonraí, athróg, paraiméadair, nó nathanna tuairisce.

`<band> ` - Bíonn na sonraí i mbandaí, atá ar taispeáint sa tuarascáil.

## Tagairtí

 * [JRXML - Vicipéid]( https://ga.wikipedia.org/wiki/JasperReports#JRXML)
 * [Foinsí JRXML agus Comhaid Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

