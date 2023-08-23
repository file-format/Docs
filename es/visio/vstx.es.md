{
  "date" : "2019-10-11",
  "keywords" :[ "archivo vstx", "formato de archivo vstx", "qué es un archivo vstx", "archivo", "ejemplo vstx", "extensión de archivo vstx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Formato de archivo de Microsoft Visio",
  "description":"Obtenga información sobre el formato de archivo VSTX y las API que pueden crear y abrir archivos VSTX",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo VSTX?

Los archivos con extensiones .vstx son archivos de plantilla de dibujo creados con Microsoft Visio 2013 y superior. Estos archivos VSTX proporcionan un punto de partida para crear dibujos de Visio, guardados como archivos [.VSDX](/es/visio/vsdx/), con diseño y configuración predeterminados. En general, los archivos de Visio se utilizan para crear dibujos que contienen objetos visuales, diagramas de flujo, diagramas UML, flujo de información, organigramas, diagramas de software, diseño de red, modelos de bases de datos, mapeo de objetos y otra información similar. Los archivos generados con Visio también se pueden exportar a diferentes formatos de archivo, como [PNG](/es/image/png/), [BMP](/es/image/bmp/), [PDF](/es/pdf/) y otros. Los programas que abren archivos VSTX incluyen Microsoft Visio para Windows y Mac que le permiten abrir estos archivos para verlos y editarlos. También permite convertir formatos de archivo de Visio a otros formatos.

# Formato de archivo VSTX #

La "X" en la extensión de archivo hace referencia al formato de archivo de OpenOffice que introdujo Microsoft como un formato de archivo de almacenamiento [ZIP](/es/compression/zip/) para reemplazar los formatos de archivo binario admitidos anteriormente. Los archivos VSTX, por lo tanto, se basan en el formato de archivo XML de las especificaciones de OpenOffice, a diferencia del formato de archivo [.VST](/es/visio/vst/) que está en formato binario.

Los archivos VSDX se basan en las convenciones de empaquetado abierto y XML, y los desarrolladores pueden beneficiarse de este formato al aprender a trabajar con estos archivos mediante programación. El formato hereda muchas de las mismas estructuras XML que sus partes del formato de archivo de dibujo XML de Visio (.vdx). La interoperabilidad con los archivos de Visio aumenta considerablemente, ya que el software de terceros puede manipular los archivos de Visio a nivel de formato de archivo.

Ciertos otros tipos de archivos que comprenden el formato de archivo de Visio 2013 incluyen:

* .vsdm (dibujo habilitado para macros de Visio)
* .vssx (plantilla de Visio)
* .vssm (plantilla habilitada para macros de Visio)
* .vstx (plantilla de Visio)
* .vstm (plantilla habilitada para macros de Visio)

En el fondo, el formato de archivo de Visio 2013 utiliza un medio estructurado para almacenar datos de aplicaciones junto con recursos relacionados en un archivo como [ZIP](/es/compression/zip/). El archivo ZIP se puede extraer utilizando cualquier utilidad de extracción estándar donde también contiene otros tipos de archivos. Simplemente puede reemplazar la extensión de archivo .VSTX con .ZIP en la exploración de Windows para ver el contenido dentro del archivo VSTX.

Cada archivo de Visio se denomina paquete que contiene otros archivos o partes. Una parte del paquete puede ser un archivo XML, una imagen o incluso una solución VBA. Las partes dentro del paquete se pueden dividir en partes de "documento" y "relación".

### Documento ###

Las partes del documento contienen el contenido real y los metadatos del archivo de Visio, como el nombre del archivo, la primera página y todas las formas que contiene, e incluso las conexiones de datos para las formas. Las imágenes y los archivos de texto dentro del paquete se consideran partes del documento.

### Relaciones ###

Las partes de relación de un archivo de Visio se almacenan en la carpeta "_rels" y describen cómo se relacionan entre sí las partes dentro del paquete. También proporciona la estructura del archivo. Un documento XML independiente utiliza la relación padre/hijo de los elementos para determinar la relación de las entidades entre sí. Un formato de archivo válido de Visio 2013 contiene el conjunto correcto de partes y el paquete contiene las relaciones entre las partes.

Las partes de relación son documentos XML que describen las relaciones entre diferentes partes del documento dentro del paquete. Definen una asociación entre dos elementos: un origen específico (definido por el nombre y la ubicación del archivo de relación) y una parte del documento de destino específica. Por ejemplo, las partes de relación se utilizan para describir qué formas maestras están asociadas con el archivo, cómo se relacionan las páginas con el archivo y entre sí, o cómo se relacionan las imágenes y los objetos con una página específica.

## Referencias ##

* [Introducción al formato de archivo de Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

