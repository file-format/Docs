{
  "date" : "2019-10-11",
  "keywords" :[ "jrxml", "archivo jrxml", "formato de archivo jrxml", "formato de archivo", "programación", "descarga de archivo jrxml", "archivo .jrxml", ".jrxml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo JRXML y las API que pueden abrir y crear archivos JRXML",
  "title" :"Formato de archivo JRXML",
  "linktitle" : "JRXML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo JRXML?

JasperReports crea un archivo JRXML y contiene una definición de diseño en el popular formato de archivo [XML](/es/web/xml/). Almacena todos los elementos de diseño, como el diseño del informe, campos de texto, imágenes, gráficos, parámetros y variables. JasperReports es una biblioteca de Java que se utiliza para crear informes mediante programación mediante la recuperación de datos de bases de datos y medios de almacenamiento.

## Formato de archivo JRXML

Los archivos JRXML son archivos de texto sin formato que se crean en función del formato de archivo XML. El marco JasperReport puede manejar diferentes tipos de fuentes de datos. Cuando se compila un archivo .jrxml, da como resultado un archivo .jasper. Un archivo jrxml consta de un conjunto de secciones. Algunas secciones contienen información relacionada con las características físicas de la página, como la dimensión de la página, el posicionamiento de los campos y la altura de las bandas, mientras que algunas se refieren a las características lógicas, como la declaración de los parámetros y variables y la definición de una consulta. para la selección de datos.

### Ejemplo de archivo JRXML

A continuación se muestra un ejemplo de archivo JRXML simple.
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

Los siguientes son los detalles del ejemplo.

`<queryString> ` − Esto está vacío (ya que estamos pasando datos a través de Java Beans). Por lo general, contiene la instrucción SQL, que recupera el resultado del informe.

`<field name> ` − Este elemento se utiliza para asignar datos de fuentes de datos o consultas a plantillas de informes. El nombre se reutiliza en el cuerpo del informe y distingue entre mayúsculas y minúsculas.

`<fieldDescription> ` − Este elemento asigna el nombre del campo con el elemento apropiado en el archivo XML.

`<staticText> ` − Esto define el texto estático que no depende de fuentes de datos, variables, parámetros o expresiones de informe.

`<band> ` − Las bandas contienen los datos, que se muestran en el informe.

## Referencias

* [JRXML - Wikipedia](https://en.wikipedia.org/wiki/JasperReports#JRXML)
* [Fuentes JRXML y archivos Jasper](https://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v630/jrxml-sources-and-jasper-files)

