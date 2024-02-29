{
  "date": "2019-10-11",
  "keywords": [
"jrxml",
"فایل jrxml",
"فرمت فایل jrxml",
"فرمت فایل",
"برنامه نويسي",
"دانلود فایل jrxml",
"فایل jrxml",
"jrxml"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل JRXML و APIهایی که می توانند فایل های JRXML را باز کرده و ایجاد کنند، بیاموزید.",
  "title": "فرمت فایل JRXML",
  "linktitle": "JRXML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jrxm-fal"
}
}،
  "lastmod": "2019-09-10"
}

## فایل JRXML چیست؟

یک فایل JRXML توسط JasperReports ایجاد شده است و حاوی تعریف طراحی در قالب فایل محبوب [XML](/web/xml/) است. تمام عناصر طراحی مانند طرح گزارش، فیلدهای متنی، تصاویر، نمودارها، پارامترها و متغیرها را ذخیره می کند. JasperReports یک کتابخانه جاوا است که برای ایجاد گزارش به صورت برنامه‌نویسی با بازیابی داده‌ها از پایگاه‌های اطلاعاتی و رسانه‌های ذخیره‌سازی استفاده می‌شود.

## فرمت فایل JRXML

فایل های JRXML فایل های متنی ساده ای هستند که بر اساس فرمت فایل XML ایجاد می شوند. چارچوب JasperReport می تواند انواع مختلفی از منابع داده را مدیریت کند. هنگامی که یک فایل .jrxml کامپایل می شود، فایل jasper. را به عنوان خروجی می دهد. یک فایل jrxml از مجموعه ای از بخش ها تشکیل شده است. برخی از بخش ها حاوی اطلاعات مربوط به ویژگی های فیزیکی صفحه مانند ابعاد صفحه، موقعیت فیلدها و ارتفاع باندها هستند، در حالی که برخی از بخش ها مربوط به ویژگی های منطقی مانند اعلام پارامترها و متغیرها و تعریف یک پرس و جو هستند. برای انتخاب داده ها

### مثال فایل JRXML

یک مثال ساده از فایل JRXML در زیر نشان داده شده است.
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

در ادامه جزئیات نمونه آورده شده است.

`<queryString> ` - این خالی است (زیرا ما در حال انتقال داده از طریق جاوا Beans هستیم). معمولا حاوی عبارت SQL است که نتیجه گزارش را بازیابی می کند.

`<field name> ` - این عنصر برای نگاشت داده ها از منابع داده یا پرس و جوها در قالب های گزارش استفاده می شود. نام مجدداً در متن گزارش استفاده می شود و به حروف کوچک و بزرگ حساس است.

`<fieldDescription> ` - این عنصر نام فیلد را با عنصر مناسب در فایل XML ترسیم می کند.

`<staticText> ` - این متن ثابتی را تعریف می کند که به هیچ منبع داده، متغیر، پارامتر یا عبارت گزارشی وابسته نیست.

`<band> ` - باندها حاوی داده هایی هستند که در گزارش نمایش داده می شوند.

## منابع

 * [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
 * [منابع JRXML و فایل‌های جاسپر](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

