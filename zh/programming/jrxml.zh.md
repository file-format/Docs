{
  "date" : "2019-10-11",
  "keywords" :["jrxml","jrxml 文件","jrxml 文件格式","文件格式","编程","jrxml 文件下载",".jrxml 文件",".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 JRXML 文件格式和可以打开和创建 JRXML 文件的 API。",
  "title" :"JRXML 文件格式",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .JRXML 文件？

JRXML 文件由 JasperReports 创建，包含流行的 [XML](/zh/web/xml/) 文件格式的设计定义。它存储所有设计元素，例如报表布局、文本字段、图像、图表、参数和变量。 JasperReports 是一个 Java 库，用于通过从后端数据库和存储媒体检索数据以编程方式创建报告。

## JRXML 文件格式

JRXML 文件是基于 XML 文件格式创建的纯文本文件。 JasperReport 框架可以处理不同类型的数据源。编译 .jrxml 文件时，会生成 .jasper 文件作为输出。一个 jrxml 文件由一组部分组成。一些部分包含与页面物理特征相关的信息，例如页面尺寸、字段位置和条带高度，而一些部分涉及逻辑特征，例如参数和变量的声明以及查询的定义用于数据选择。

### JRXML 文件示例

下面显示了一个简单的 JRXML 文件示例。
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
        <reportElement x="65" y="13" width "424" height="35"/>
        <textElement textAlignment="Center">
          <font size="26" isBold="true"/>
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

以下是示例的详细信息。

`<queryString> ` - 这是空的（因为我们正在通过 Java Beans 传递数据）。通常包含检索报表结果的 SQL 语句。

`<field name> ` - 此元素用于将来自数据源或查询的数据映射到报告模板中。名称在报告正文中重复使用并且区分大小写。

`<fieldDescription> ` - 此元素将字段名称映射到 XML 文件中的适当元素。

`<staticText> ` - 这定义了不依赖于任何数据源、变量、参数或报告表达式的静态文本。

`<band> ` - 波段包含数据，显示在报告中。

## 参考

* [JRXML - 维基百科](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML 源和 Jasper 文件](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

