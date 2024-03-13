{
  "date": "2019-10-11",
  "keywords": [
"jrxml",
"jrxml faylı",
"jrxml fayl formatı",
"fayl formatı",
"proqramlaşdırma",
"jrxml faylı yükləyin",
".jrxml faylı",
".jrxml"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "JRXML fayl formatı və JRXML fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "JRXML fayl formatı",
  "linktitle": "JRXML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jrxm-azl"
}
},
  "lastmod": "2019-09-10"
}

## JRXML faylı nədir?

JRXML faylı JasperReports tərəfindən yaradılmışdır və məşhur [XML](/web/xml/) fayl formatında dizayn tərifini ehtiva edir. O, hesabat tərtibatı, mətn sahələri, şəkillər, diaqramlar, parametrlər və dəyişənlər kimi bütün dizayn elementlərini saxlayır. JasperReports, backend verilənlər bazalarından və saxlama mediasından məlumat əldə etməklə proqramlı şəkildə hesabatlar yaratmaq üçün istifadə olunan Java kitabxanasıdır.

## JRXML fayl formatı

JRXML faylları XML fayl formatı əsasında yaradılmış düz mətn fayllarıdır. JasperReport çərçivəsi müxtəlif növ məlumat mənbələrini idarə edə bilər. .jrxml faylı tərtib edildikdə, o, çıxış kimi .jasper faylı ilə nəticələnir. jrxml faylı bir sıra bölmələrdən ibarətdir. Bəzi bölmələr səhifənin ölçüsü, sahələrin yerləşdirilməsi və zolaqların hündürlüyü kimi səhifənin fiziki xüsusiyyətləri ilə bağlı məlumatları ehtiva edir, bəziləri isə parametrlərin və dəyişənlərin elanı və sorğunun tərifi kimi məntiqi xüsusiyyətlərə aiddir. məlumat seçimi üçün.

### JRXML fayl nümunəsi

Sadə bir JRXML fayl nümunəsi aşağıda göstərilmişdir.
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

Aşağıda nümunənin təfərrüatları verilmişdir.

`<queryString> ` − Bu boşdur (məlumatları Java Beans vasitəsilə ötürdükdən sonra). Adətən hesabat nəticəsini alan SQL ifadəsini ehtiva edir.

`<field name> ` − Bu element məlumat mənbələrindən və ya sorğulardan verilənləri hesabat şablonlarına uyğunlaşdırmaq üçün istifadə olunur. ad hesabat orqanında təkrar istifadə olunur və hərf-həssasdır.

`<fieldDescription> ` − Bu element sahə adını XML faylında müvafiq elementlə əlaqələndirir.

`<staticText> ` − Bu, heç bir məlumat mənbələrindən, dəyişənlərdən, parametrlərdən və ya hesabat ifadələrindən asılı olmayan statik mətni müəyyən edir.

`<band> ` − Qruplar hesabatda göstərilən məlumatları ehtiva edir.

## İstinadlar

 * [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
 * [JRXML Mənbələri və Jasper Faylları](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

