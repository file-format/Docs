{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml файл", "jrxml файлов формат", "файлов формат", "програмиране", "jrxml файл изтегляне", ".jrxml файл", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за файловия формат JRXML и API, които могат да отварят и създават JRXML файлове.",
  "title" :"Файлов формат JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е JRXML файл?

JRXML файл се създава от JasperReports и съдържа дефиниция на дизайна в популярен файлов формат [XML](/bg/web/xml/). Той съхранява всички елементи на дизайна като оформление на отчета, текстови полета, изображения, диаграми, параметри и променливи. JasperReports е библиотека на Java, използвана за програмно създаване на отчети чрез извличане на данни от бекенд бази данни и носители за съхранение.

## JRXML файлов формат

JRXML файловете са обикновени текстови файлове, които са създадени въз основа на XML файлов формат. Рамката JasperReport може да обработва различни видове източници на данни. Когато се компилира .jrxml файл, той води до .jasper файл като изход. Jrxml файлът се състои от набор от секции. Някои секции съдържат информация, свързана с физическите характеристики на страницата, като размери на страницата, позициониране на полетата и височина на лентите, докато други се отнасят до логическите характеристики, като деклариране на параметрите и променливите и дефиниране на заявка за избор на данни.

### Пример за JRXML файл

Пример за прост JRXML файл е показан по-долу.
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

Следват подробностите за примера.

`<queryString> ` − Това е празно (тъй като предаваме данни през Java Beans). Обикновено съдържа SQL оператора, който извлича резултата от отчета.

`<field name> ` − Този елемент се използва за картографиране на данни от източници на данни или заявки в шаблони на отчети. името се използва повторно в основния текст на отчета и е чувствително към главни и малки букви.

`<fieldDescription> ` − Този елемент съпоставя името на полето със съответния елемент в XML файла.

`<staticText> ` − Това дефинира статичния текст, който не зависи от никакви източници на данни, променливи, параметри или изрази за отчет.

`<band> ` − Лентите съдържат данните, които се показват в отчета.

## Препратки

* [JRXML - Уикипедия](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML източници и Jasper файлове](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

