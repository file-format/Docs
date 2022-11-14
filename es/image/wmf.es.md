{
  "date" : "2019-10-11",
  "keywords" :[ "archivo wmf", "formato de archivo wmf", "qué es un archivo wmf", "archivo", "ejemplo de wmf", "extensión de archivo wmf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF: formato de metarchivo de Microsoft Windows",
  "description":"Obtenga más información sobre el formato de archivo WMF y las API que pueden crear y abrir archivos WMF",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo WMF?

Los archivos con la extensión WMF representan el metarchivo de Microsoft Windows (WMF) para almacenar datos de imágenes en formato vectorial y de mapa de bits. Para ser más precisos, WMF pertenece a la categoría de formato de archivo vectorial de formatos de archivo de gráficos que es independiente del dispositivo. La interfaz de dispositivo gráfico de Windows (GDI) utiliza las funciones almacenadas en un archivo WMF para mostrar una imagen en la pantalla. Posteriormente se publicó una versión más mejorada de WMF, conocida como Enhanced Meta Files (EMF), que hace que el formato sea más rico en funciones. Prácticamente, WMF son similares a SVG.

## Especificaciones del formato de archivo WMF ##

Un archivo WMF se refería a un formato de archivo de 16 bits en el momento de su lanzamiento con Windows 3.0. El formato de archivo consta de una serie de registros de longitud variable que contienen comandos de dibujo de gráficos, definiciones de objetos y propiedades. Dado que los archivos WMF se basan en comandos presentados a GDI para dibujar la imagen, también se conocen como una grabación digital de la imagen que se puede reproducir para reproducir esa imagen. Las especificaciones completas de formato de archivo de WMF están disponibles en línea y deben consultarse para el desarrollo de aplicaciones que trabajen con archivos WMF. Un archivo WMF está organizado en:

* Registro de encabezado WMF
* Registro(s) WMF
* Registro de fin de archivo WMF

### Registro de encabezado WMF ###

El **Registro META_HEADER** contiene información que define las características del metarchivo, incluyendo:

* El tipo de metarchivo
* La versión del metarchivo
* El tamaño del metarchivo
* El número de objetos definidos en el metarchivo
* El tamaño del registro único más grande en el metarchivo

### Registro de encabezado colocable WMF ###

El **Registro META_PLACEABLE** contiene información ampliada sobre la imagen, que incluye:

* Un rectángulo delimitador
* Tamaño de unidad lógica, para escalar
* Una suma de comprobación, para la validación

### Registro WMF ###

Los registros WMF tienen un formato genérico, que se especifica en el documento de especificaciones. Cada registro WMF contiene la siguiente información:

* El tamaño del registro
* La función de registro
* Parámetros, si los hay, para la función de registro

## Referencias ##

* [[MS-WMF]: formato de metarchivo de Windows](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Metaarchivo de Windows - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

