{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "fichier jrxml", "format de fichier jrxml", "format de fichier", "programmation","téléchargement de fichier jrxml", "fichier .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier JRXML et les API qui peuvent ouvrir et créer des fichiers JRXML.",
  "title" :"Format de fichier JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier JRXML ?

Un fichier JRXML est créé par JasperReports et contient une définition de conception au format de fichier populaire [XML](/fr/web/xml/). Il stocke tous les éléments de conception tels que la mise en page du rapport, les champs de texte, les images, les graphiques, les paramètres et les variables. JasperReports est une bibliothèque Java utilisée pour créer des rapports par programme en récupérant des données à partir de bases de données principales et de supports de stockage.

## Format de fichier JRXML

Les fichiers JRXML sont des fichiers de texte brut créés sur la base du format de fichier XML. Le framework JasperReport peut gérer différents types de sources de données. Lorsqu'un fichier .jrxml est compilé, il en résulte un fichier .jasper en sortie. Un fichier jrxml se compose d'un ensemble de sections. Certaines sections contiennent des informations liées aux caractéristiques physiques de la page telles que la dimension de la page, le positionnement des champs et la hauteur des bandes, tandis que d'autres concernent les caractéristiques logiques telles que la déclaration des paramètres et des variables et la définition d'une requête pour la sélection des données.

### Exemple de fichier JRXML

Un exemple de fichier JRXML simple est présenté ci-dessous.
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

Voici les détails de l'exemple.

`<queryString> ` - Ceci est vide (car nous transmettons des données via des Java Beans). Contient généralement l'instruction SQL, qui récupère le résultat du rapport.

`<field name> ` − Cet élément est utilisé pour mapper des données à partir de sources de données ou de requêtes dans des modèles de rapport. name est réutilisé dans le corps du rapport et est sensible à la casse.

`<fieldDescription> ` − Cet élément mappe le nom du champ avec l'élément approprié dans le fichier XML.

`<staticText> ` - Ceci définit le texte statique qui ne dépend d'aucune source de données, variable, paramètre ou expression de rapport.

`<band> ` − Les bandes contiennent les données qui sont affichées dans le rapport.

## Références

* [JRXML - Wikipédia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Sources JRXML et fichiers Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

