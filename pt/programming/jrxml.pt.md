{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "arquivo jrxml", "formato de arquivo jrxml", "formato de arquivo", "programação", "baixar arquivo jrxml", "arquivo .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo JRXML e APIs que podem abrir e criar arquivos JRXML.",
  "title" :"Formato de arquivo JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo JRXML?

Um arquivo JRXML é criado pelo JasperReports e contém a definição de design no formato de arquivo popular [XML](/pt/web/xml/). Ele armazena todos os elementos de design, como layout de relatório, campos de texto, imagens, gráficos, parâmetros e variáveis. JasperReports é uma biblioteca Java usada para criar relatórios programaticamente recuperando dados de bancos de dados de back-end e mídia de armazenamento.

## Formato de arquivo JRXML

Os arquivos JRXML são arquivos de texto simples criados com base no formato de arquivo XML. A estrutura JasperReport pode lidar com diferentes tipos de fontes de dados. Quando um arquivo .jrxml é compilado, ele resulta em um arquivo .jasper como saída. Um arquivo jrxml consiste em um conjunto de seções. Algumas seções contêm informações relacionadas às características físicas da página, como dimensão da página, posicionamento dos campos e altura das faixas, enquanto outras dizem respeito às características lógicas, como declaração dos parâmetros e variáveis e definição de uma consulta para seleção de dados.

### Exemplo de arquivo JRXML

Um exemplo simples de arquivo JRXML é mostrado abaixo.
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

Seguem os detalhes do exemplo.

`<queryString> ` − Este está vazio (já que estamos passando dados através de Java Beans). Geralmente contém a instrução SQL, que recupera o resultado do relatório.

`<field name> ` − Este elemento é usado para mapear dados de fontes de dados ou consultas, em modelos de relatório. name é reutilizado no corpo do relatório e diferencia maiúsculas de minúsculas.

`<fieldDescription> ` − Este elemento mapeia o nome do campo com o elemento apropriado no arquivo XML.

`<staticText> ` − Isso define o texto estático que não depende de nenhuma fonte de dados, variáveis, parâmetros ou expressões de relatório.

`<band> ` − As bandas contêm os dados, que são exibidos no relatório.

## Referências

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Fontes JRXML e arquivos Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

