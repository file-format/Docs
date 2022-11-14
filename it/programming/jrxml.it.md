{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "file jrxml", "formato file jrxml", "formato file", "programmazione", "download file jrxml", "file .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file JRXML e le API che possono aprire e creare file JRXML.",
  "title" :"Formato file JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file JRXML?

Un file JRXML viene creato da JasperReports e contiene la definizione del progetto nel popolare formato di file [XML](/it/web/xml/). Memorizza tutti gli elementi di progettazione come layout del report, campi di testo, immagini, grafici, parametri e variabili. JasperReports è una libreria Java utilizzata per creare report a livello di codice recuperando dati da database back-end e supporti di memorizzazione.

## Formato file JRXML

I file JRXML sono file di testo semplice creati in base al formato di file XML. Il framework JasperReport può gestire diversi tipi di origini dati. Quando un file .jrxml viene compilato, risulta in un file .jasper come output. Un file jrxml è costituito da un insieme di sezioni. Alcune sezioni contengono informazioni relative alle caratteristiche fisiche della pagina come la dimensione della pagina, il posizionamento dei campi e l'altezza delle fasce, mentre altre riguardano le caratteristiche logiche come la dichiarazione dei parametri e delle variabili e la definizione di una query per la selezione dei dati.

### Esempio di file JRXML

Di seguito è mostrato un semplice esempio di file JRXML.
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

Di seguito sono riportati i dettagli dell'esempio.

`<queryString> ` − Questo è vuoto (poiché stiamo passando i dati attraverso Java Beans). Di solito contiene l'istruzione SQL, che recupera il risultato del report.

`<field name> ` − Questo elemento viene utilizzato per mappare i dati da origini dati o query, in modelli di report. name viene riutilizzato nel corpo del report e distingue tra maiuscole e minuscole.

`<fieldDescription> ` − Questo elemento associa il nome del campo con l'elemento appropriato nel file XML.

`<staticText> ` − Definisce il testo statico che non dipende da origini dati, variabili, parametri o espressioni di report.

`<band> ` − Le bande contengono i dati che vengono visualizzati nel report.

## Riferimenti

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Sorgenti JRXML e file Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

