{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "jrxml 파일", "jrxml 파일 형식", "파일 형식", "프로그래밍","jrxml 파일 다운로드", ".jrxml 파일", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"JRXML 파일을 열고 생성할 수 있는 API와 JRXML 파일 형식에 대해 알아보세요.",
  "title" :"JRXML 파일 형식",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .JRXML 파일이란?

JRXML 파일은 JasperReports에 의해 생성되며 널리 사용되는 [XML](/ko/web/xml/) 파일 형식의 디자인 정의를 포함합니다. 보고서 레이아웃, 텍스트 필드, 이미지, 차트, 매개변수 및 변수와 같은 모든 디자인 요소를 저장합니다. JasperReports는 백엔드 데이터베이스 및 저장 매체에서 데이터를 검색하여 프로그래밍 방식으로 보고서를 작성하는 데 사용되는 Java 라이브러리입니다.

## JRXML 파일 형식

JRXML 파일은 XML 파일 형식을 기반으로 생성된 일반 텍스트 파일입니다. JasperReport 프레임워크는 다양한 종류의 데이터 소스를 처리할 수 있습니다. .jrxml 파일이 컴파일되면 .jasper 파일이 출력됩니다. jrxml 파일은 섹션 세트로 구성됩니다. 일부 섹션에는 페이지의 차원, 필드의 위치, 밴드의 높이와 같은 페이지의 물리적 특성과 관련된 정보가 포함되고 일부는 매개변수 및 변수 선언 및 쿼리 정의와 같은 논리적 특성에 관한 정보를 포함합니다. 데이터 선택을 위해.

### JRXML 파일 예

간단한 JRXML 파일 예가 아래에 나와 있습니다.
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

다음은 예제의 세부 사항입니다.

`<queryString> ` − 이것은 비어 있습니다(Java Beans를 통해 데이터를 전달하기 때문에). 일반적으로 보고서 결과를 검색하는 SQL 문을 포함합니다.

`<field name> ` - 이 요소는 데이터 소스 또는 쿼리의 데이터를 보고서 템플릿으로 매핑하는 데 사용됩니다. 이름은 보고서 본문에서 재사용되며 대소문자를 구분합니다.

`<fieldDescription> ` - 이 요소는 필드 이름을 XML 파일의 적절한 요소와 매핑합니다.

`<staticText> ` - 이것은 데이터 소스, 변수, 매개변수 또는 보고서 표현식에 의존하지 않는 정적 텍스트를 정의합니다.

`<band> ` − 밴드에는 보고서에 표시되는 데이터가 포함됩니다.

## 참고문헌

* [JRXML - 위키백과](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML 소스 및 Jasper 파일](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

