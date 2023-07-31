{
  "date" : "2019-10-11",
  "keywords" :[ "archivo vsdm", "formato de archivo vsdm", "qué es un archivo vsdm", "archivo", "ejemplo de vsdm", "extensión de archivo vsdm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Formato de archivo de dibujo de Microsoft Visio",
  "description":"Obtenga información sobre el formato de archivo VSDM y las API que pueden crear y abrir archivos VSDM",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo VSDM?

Los archivos con la extensión .vsdm son archivos de dibujo creados con la aplicación Microsoft Visio que admite macros. Los archivos VSDM son dibujos OPC/XML que son similares a VSDX pero también brindan la capacidad de ejecutar macros cuando se abre el archivo. Las macros son acciones/pasos definidos por el usuario que se desarrollan en Visual Basic para aplicaciones (VBA) y se pueden usar para realizar tareas repetitivas. El formato de archivo VSDM se introdujo con el lanzamiento de Microsoft Visio 2013. Los archivos de Visio se utilizan para crear dibujos que contienen objetos visuales, diagramas de flujo, diagrama UML, flujo de información, organigramas, diagramas de software, diseño de red, modelos de base de datos, mapeo de objetos y otros. información similar. Los archivos generados con Visio también se pueden exportar a diferentes formatos de archivo, como [PNG](/es/image/png/), [BMP](/es/image/bmp/), [PDF](/es/pdf/) y otros.

## Formato de archivo VSDM

Los archivos VSDM se basan en las convenciones de empaquetado abierto y XML, y los desarrolladores pueden beneficiarse de este formato aprendiendo a trabajar con estos archivos mediante programación. El formato hereda muchas de las mismas estructuras XML que sus partes del formato de archivo de dibujo XML de Visio (.vdx). La interoperabilidad con los archivos de Visio aumenta considerablemente, ya que el software de terceros puede manipular los archivos de Visio a nivel de formato de archivo.

Cada archivo de Visio se denomina paquete que contiene otros archivos o partes. Una parte del paquete puede ser un archivo XML, una imagen o incluso una solución VBA. Las partes dentro del paquete se pueden dividir en partes de "documento" y "relación".

### Documento ###

Las partes del documento contienen el contenido real y los metadatos del archivo de Visio, como el nombre del archivo, la primera página y todas las formas que contiene, e incluso las conexiones de datos para las formas. Las imágenes y los archivos de texto dentro del paquete se consideran partes del documento.

### Relaciones ###

Las partes de relación de un archivo de Visio se almacenan en la carpeta "\_rels" y describen cómo se relacionan entre sí las partes dentro del paquete. También proporciona la estructura del archivo. Un documento XML independiente utiliza la relación padre/hijo de los elementos para determinar la relación de las entidades entre sí. Un formato de archivo válido de Visio 2013 contiene el conjunto correcto de partes y el paquete contiene las relaciones entre las partes.

Las partes de relación son documentos XML que describen las relaciones entre diferentes partes del documento dentro del paquete. Definen una asociación entre dos elementos: un origen específico (definido por el nombre y la ubicación del archivo de relación) y una parte del documento de destino específica. Por ejemplo, las partes de relación se utilizan para describir qué formas maestras están asociadas con el archivo, cómo se relacionan las páginas con el archivo y entre sí, o cómo se relacionan las imágenes y los objetos con una página específica.

## Referencias ##

* [Introducción al formato de archivo de Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

