{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","qué es un archivo xsd","cómo abrir un archivo xsd","extensión", "archivo", "archivo xsd","formato de archivo xsd", "extensión .xsd" ,"ejemplo de archivo xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Obtenga información sobre el formato de archivo XSD y las API que pueden crear y abrir un archivo XSD.",
  "title" :"Formato de archivo XSD: archivo de definición de esquema XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## ¿Qué es un archivo de esquema XSD?

Un archivo XSD es un archivo de definición que especifica los elementos y atributos que pueden formar parte de un documento XML. Esto garantiza que los datos se interpreten correctamente y que se detecten los errores, lo que da como resultado una validación XML adecuada. Los archivos XSD garantizan que los datos introducidos sigan la misma estructura definida en el archivo. Los archivos XSD se almacenan en formato de archivo [XML](/es/web/xml/) y se pueden abrir o editar en cualquier editor de texto como Microsoft Notepad, Notepad++ o [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Formato de archivo XSD

Los archivos XSD se almacenan en el disco en formato de archivo de texto sin formato que es legible por humanos. Un XSD define los elementos que se pueden utilizar en los documentos, en relación con los datos reales con los que se va a codificar.

## Ejemplo de archivo XSD

Un archivo XSD simple que tiene un esquema de orden de compra define los elementos usando etiquetas como se muestra en el siguiente [ejemplo XSD de Microsoft] (https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -esquema-simple?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

Aquí, se utilizan las siguientes etiquetas.

* `xs:element` - Define un elemento.
* `xs:sequence`: indica que los elementos secundarios solo aparecen en el orden mencionado.
* `xs:complexType`: indica que contiene otros elementos.
* `xs:simpleType`: indica que no contienen otros elementos.
* `tipo` - cadena, decimal, entero, booleano, fecha, hora,

## Referencias ##

- [Bloc de notas XML de Microsoft](https://microsoft.github.io/XmlNotepad/)
- [Ejemplo de muestra de XSD](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

