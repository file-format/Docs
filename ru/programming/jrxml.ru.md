{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "файл jrxml", "формат файла jrxml", "формат файла", "программирование", "загрузка файла jrxml", "файл .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файлов JRXML и API, которые могут открывать и создавать файлы JRXML.",
  "title" :"Формат файла JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .JRXML вариант №

Файл JRXML создается JasperReports и содержит определение дизайна в популярном формате файла [XML](/ru/web/xml/). В нем хранятся все элементы дизайна, такие как макет отчета, текстовые поля, изображения, диаграммы, параметры и переменные. JasperReports — это библиотека Java, используемая для программного создания отчетов путем извлечения данных из серверных баз данных и носителей.

## Формат файла JRXML

Файлы JRXML представляют собой простые текстовые файлы, созданные на основе формата файла XML. Фреймворк JasperReport может обрабатывать различные виды источников данных. Когда файл .jrxml компилируется, на выходе получается файл .jasper. Файл jrxml состоит из набора разделов. Некоторые разделы содержат информацию, относящуюся к физическим характеристикам страницы, такой как размер страницы, расположение полей и высота полос, а некоторые касаются логических характеристик, таких как объявление параметров и переменных и определение запроса. для выбора данных.

### Пример файла JRXML

Ниже показан простой пример файла JRXML.
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

Ниже приведены подробности примера.

`<queryString> ` — Это пусто (поскольку мы передаем данные через Java Beans). Обычно содержит оператор SQL, который извлекает результат отчета.

`<field name> ` — Этот элемент используется для сопоставления данных из источников данных или запросов в шаблоны отчетов. имя повторно используется в тексте отчета и чувствительно к регистру.

`<fieldDescription> ` — Этот элемент сопоставляет имя поля с соответствующим элементом в файле XML.

`<staticText> ` — определяет статический текст, который не зависит ни от каких источников данных, переменных, параметров или выражений отчета.

`<band> ` − Бэнды содержат данные, которые отображаются в отчете.

## использованная литература

* [JRXML — Википедия] (https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Исходники JRXML и файлы Jasper] (https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

