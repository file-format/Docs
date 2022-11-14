{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","archivo", "formato", "tipo de archivo", "extensión","¿qué es un archivo DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"Obtenga información sobre el formato de archivo DOCX y las API que pueden crear y abrir archivos DOCX",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## ¿Qué es un archivo DOCX? ##

DOCX es un formato muy conocido para documentos de Microsoft Word. Introducido a partir de 2007 con el lanzamiento de Microsoft Office 2007, la estructura de este nuevo formato de documento se cambió de binario simple a una combinación de XML y archivos binarios. Los archivos Docx se pueden abrir con Word 2007 y versiones laterales, pero no con las versiones anteriores de MS Word que admiten extensiones de archivo DOC.

## Breve historia ##

Después de que Microsoft abrió las especificaciones para el formato de archivo DOC, fue fácil para sus competidores aplicar ingeniería inversa al formato y proporcionar el mismo soporte en sus propias aplicaciones. Además, la competencia de Open Office en forma de formato de documento abierto obligó a Microsoft a adoptar estándares más abiertos y amplios. Fue a principios de 2000 cuando Microsoft decidió apostar por el cambio para adaptarse al estándar de **Office Open XML**. Los documentos bajo este nuevo estándar recibieron [extensión .docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), la "X" siendo para XML. En 2007, este nuevo formato de archivo pasó a formar parte de Office 2007 y también se mantiene en las nuevas versiones de Microsoft Office. El nuevo tipo de archivo ha agregado ventajas de tamaño de archivo pequeño, menos cambios de corrupción y representación de imágenes con buen formato.

## Especificaciones del formato de archivo DOCX: más información

Un archivo Docx se compone de una colección de archivos XML que se encuentran dentro de un archivo ZIP. El contenido de un nuevo documento de Word se puede ver descomprimiendo su contenido. La colección contiene una lista de archivos XML que se clasifican como:

* Archivos de metadatos: contiene información sobre otros archivos disponibles en el archivo
* Documento: contiene el contenido real del documento

### Archivos de metadatos ###

Microsoft Word usa estos archivos para encontrar la relación entre los archivos y ubicar el contenido del documento. Cuando se extrae un archivo de documentos de Word, contiene varios de estos archivos, como se detalla a continuación.

#### Relaciones - \_rels/.rels ####

Este archivo contiene información que le indica a MS Word dónde buscar el contenido del documento y otras referencias. Cada relación se identifica mediante una identificación de relación única y especifica el archivo XML al que se hace referencia como destino. Un archivo de relación de muestra se muestra a continuación:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Tipos de contenido ####

Un documento puede contener varios tipos de medios en su interior, como imágenes, temas, arte de palabras, etc. [Content_Types].xml contiene información sobre dichos tipos de medios presentes en el documento. El contenido de un archivo XML de este tipo se muestra a continuación:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Referencias a recursos - \_rels/document.xml.rels ####

En este archivo XML se hace referencia a la información sobre los recursos, como las imágenes incrustadas en el documento.

#### Contenido del documento principal ####

Esto se refiere al archivo XML principal del archivo que contiene el contenido de texto del documento. Este contenido está representado por una variedad de nodos según las especificaciones XML de OpenOffice. La mayoría de los contenidos de este archivo consisten en párrafos y tablas, aunque también pueden ser otros nodos.

### Nodos de formato de archivo ###

El archivo principal document.xml es una colección de nodos para la representación del contenido general de un archivo. Cada nodo tiene un inicio y un final que encapsula otros nodos o el contenido. Un ejemplo simplificado de un archivo xml de este tipo es el siguiente:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

A continuación se muestra la información sobre algunos de los nodos contenidos en un archivo DOCX para la representación de contenidos.

`<w:document> ` - Representa el elemento raíz del contenido principal del archivo.

`<w:body> ` - Representa el cuerpo del documento que puede comprender muchos otros nodos de elementos, como párrafos, tablas y secciones.

#### Párrafos ####

Un párrafo es el titular del contenido principal dentro de un documento. Está representado por **<w:p> ** elemento dentro de un documento. Un párrafo consta además de una o más carreras **<w:r> ** que contiene el texto real del párrafo. Además de las ejecuciones, los párrafos también pueden contener otros elementos del documento, como hipervínculos, comentarios, etc. A continuación se muestra una estructura de párrafo de ejemplo:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Referencias ##

* [MS - Formato de archivo DOCX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

