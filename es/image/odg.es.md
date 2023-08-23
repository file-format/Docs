{
  "date" : "2019-10-11",
  "keywords" :[ "archivo odg", "formato de archivo odg", "qué es un archivo odg", "archivo", "ejemplo odg", "extensión de archivo odg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo ODG",
  "description":"Obtenga información sobre el formato de archivo ODG y las API que pueden crear y abrir archivos ODG",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo ODG?

El formato de archivo ODG es utilizado por la aplicación Draw de Apache OpenOffice para almacenar elementos de dibujo como una imagen vectorial. Sigue las especificaciones de formato de archivo basadas en XML descritas por Advancement of Structural Information Standards (OASIS). ODG representa dibujos como imágenes vectoriales utilizando puntos, líneas y curvas. Además de OpenOffice, LibreOffice y otras aplicaciones también brindan soporte para trabajar con el formato de archivo ODG. Otros formatos admitidos por OpenOffice, por ejemplo, incluyen [ODT](/es/word-processing/odt/), ODF, [ODP](/es/presentation/odp/) y [ODS](/es/spreadsheet/ods/).


## Especificaciones del formato de archivo ODG

El formato de archivo ODG se basa en el formato OpenDocument, que es un formato de documento XML estructurado con un esquema bien definido.
Cada componente estructural de un formato OpenDocument está representado por un elemento que tiene atributos asociados. La estructura basada en XML es común para todos los tipos de documentos, como documentos de texto, hojas de cálculo o archivos de dibujo. Un documento puede contener diferentes estilos. Una estructura de archivo OpenDocument consta de los siguientes elementos.
* Raiz del documento
* Metadatos del documento
* Elemento de cuerpo y tipos de documentos
* Configuraciones de la aplicación
* Guiones
* Declaraciones de cara de fuente
* Estilos
* Estilos de página y diseños

## Raíces del documento ##

Un elemento raíz de documento contiene todo el documento y es el elemento principal de un archivo en formato OpenDocument. Los mismos tipos de elementos raíz de documentos son aplicables a todos los tipos de documentos, como texto, documentos, hojas de cálculo y documentos de dibujo.

### Elementos raíz ###
Un solo documento XML está representado por su propio elemento raíz. Los cinco diferentes elementos raíz admitidos son los siguientes.

`<office:document>` - Documento de oficina completo en un solo documento XML.
`<office:document-content>` - Contenido del documento y estilos automáticos utilizados en el contenido.
`<office:document-styles>` - Estilos usados en el contenido del documento y estilos automáticos usados en los propios estilos.
`<office:document-meta>` - Metainformación del documento, como el autor o la hora de la última acción de guardado.
`<office:document-settings>` - Configuración específica de la aplicación, como el tamaño de la ventana o la información de la impresora.

### Metadatos del documento ODG ###
El OpenDocument contiene todos los elementos de metadatos en el \<office:meta> elemento. Esta información general sobre un documento se encuentra al comienzo del documento y las aplicaciones pueden actualizar varias instancias de los mismos elementos.

### Elemento del cuerpo y tipos de documentos ###
El cuerpo del documento indica el tipo de contenido contenido en el documento utilizando el elemento de tipo de documento. Estos tipos de documentos son:
* documentos de texto
* documentos de dibujo
* documentos de presentación
* documentos de hoja de cálculo
* documentos gráficos
* documentos de imagen

### Configuraciones de la aplicación ###
La configuración de las aplicaciones de oficina representa diferentes configuraciones que están relacionadas con la configuración del documento o la apariencia visual del documento. Cada categoría está representada por un `<config:config-item-set>`. Ejemplos de tales categorías de configuración incluyen:
* Configuración del documento, por ejemplo, impresora predeterminada
* Ver configuración, por ejemplo, nivel de zoom

### Guiones ###
Es común que un documento contenga varios scripts. Cada script en un archivo OpenDocument está representado por un `<office:script>` elemento. Estos elementos del script están contenidos en un solo `<office:scripts>` elemento. Los scripts no actualizan un documento mientras se carga el documento.
### Declaraciones de cara de fuente ###

Una declaración de tipo de fuente contiene información sobre las fuentes utilizadas por el autor de un documento. Esta información ayuda a localizar estas fuentes en otros sistemas.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Estilos ###
Los siguientes estilos son compatibles con el formato OpenDocument.

`Estilos comunes`: las representaciones XML de dichos estilos se denominan estilos.
`Estilos automáticos`: contiene propiedades de formato que, en la vista de la interfaz de usuario de un documento, se asignan a un objeto como un párrafo.
`Estilos mater`: un estilo común que contiene información de formato y contenido adicional que se muestra con el contenido del documento cuando se aplica el estilo. Un ejemplo de un estilo maestro son las páginas maestras.

## Referencias ##
* [Formato de documento abierto de OASIS para aplicaciones de Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

