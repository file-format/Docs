{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo DXL y las API que pueden crear y abrir archivos DTSX.",
  "title" :"Formato de archivo DXL - Formato de archivo en lenguaje XML de Domino",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## ¿Qué es un archivo DXL?

Un archivo DXL es un archivo de almacenamiento de datos basado en XML creado para el software de colaboración empresarial de nivel empresarial, Lotus Domino. Contiene datos relacionados con una base de datos de Lotus Domino, como esquemas, elementos de diseño, vistas, formularios, documentos y los datos de la base de datos en sí. [XML](/es/web/xml/) es un formato de archivo universal que pueden leer las aplicaciones de software escritas en cualquier lenguaje de programación. También es legible por humanos y se puede abrir con cualquier editor de texto. Es por eso que los archivos DXL brindan la capacidad de exportar datos en formatos de archivo intercambiables.

## Formato de archivo DXL

Los archivos DXL se guardan en formato de archivo XML y son fácilmente legibles por aplicaciones escritas en cualquier lenguaje de programación. Estos archivos almacenan datos y configuraciones en etiquetas XML que clasifican los datos y los organizan en el orden adecuado.

### Ejemplo de salida DXL

A continuación se muestra el extracto del texto de salida de un documento de Notes.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## Referencias

* [Formato DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

