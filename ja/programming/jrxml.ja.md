{
  "date" : "2019-10-11",
  "keywords" :["jrxml","jrxmlファイル","jrxmlファイル形式","ファイル形式","プログラミング","jrxmlファイルダウンロード",".jrxmlファイル",".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"JRXML ファイル形式と,JRXML ファイルを開いて作成できる API について学びます。",
  "title" :"JRXMLファイル形式",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .JRXML ファイルとは?

JRXML ファイルは JasperReports によって作成され、一般的な [XML](/web/xml/) ファイル形式のデザイン定義が含まれています。レポート レイアウト、テキスト フィールド、画像、グラフ、パラメーター、変数などのすべての設計要素が格納されます。 JasperReports は、バックエンド データベースとストレージ メディアからデータを取得することにより、プログラムでレポートを作成するために使用される Java ライブラリです。

## JRXMLファイル形式

JRXML ファイルは、XML ファイル形式に基づいて作成されたプレーン テキスト ファイルです。 JasperReport フレームワークは、さまざまな種類のデータ ソースを処理できます。 .jrxml ファイルをコンパイルすると、.jasper ファイルが出力されます。 jrxml ファイルは、一連のセクションで構成されています。一部のセクションには、ページの寸法、フィールドの配置、バンドの高さなど、ページの物理的特性に関連する情報が含まれていますが、一部のセクションには、パラメーターと変数の宣言、およびクエリの定義などの論理的特性に関する情報が含まれています。データ選択用。

### JRXML ファイルの例

簡単な JRXML ファイルの例を以下に示します。
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

例の詳細は次のとおりです。

`<queryString> ` - これは空です (Java Beans を介してデータを渡しているため)。通常、レポート結果を取得する SQL ステートメントが含まれます。

`<field name> ` - この要素は、データ ソースまたはクエリからレポート テンプレートにデータをマップするために使用されます。 name はレポート本文で再利用され、大文字と小文字が区別されます。

`<fieldDescription> ` - この要素は、フィールド名を XML ファイル内の適切な要素にマップします。

`<staticText> ` - これは、データソース、変数、パラメーター、またはレポート式に依存しない静的テキストを定義します。

`<band> ` - バンドには、レポートに表示されるデータが含まれます。

## 参考文献

* [JRXML - ウィキペディア](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [JRXML ソースと Jasper ファイル](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

