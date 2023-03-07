{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "archivo", "extensión", "formato", "Libro electrónico", "Libro digital" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo EPUB y las API que pueden crear y abrir archivos EPUB",
  "title" :"¿Qué es un archivo EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## ¿Qué es un archivo EPUB?

Los archivos con extensión .epub son un formato de archivo de libro electrónico que proporciona un formato de publicación digital estándar para editores y consumidores. El formato ha sido tan común ahora que es compatible con muchos lectores electrónicos y aplicaciones de software. Por ejemplo, en Mac OS, el software **Books** preinstalado brinda soporte para abrir dichos archivos. Además, hay una gran cantidad de software compatible disponible para teléfonos inteligentes, tabletas y computadoras. Los estándares de archivos EPUB son mantenidos por el [Foro Internacional de Publicaciones Digitales](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). La versión EPUB 3 también cuenta con el respaldo del Grupo de Estudio de la Industria del Libro (BISG), una asociación líder en el comercio de libros para mejores prácticas estandarizadas, investigación, información y eventos, para empaquetar contenido.

## Breve historia del formato de archivo EPUB

* **Octubre 2007** - EPUB 2.0 fue aprobado
* **Septiembre de 2010**: se lanzó una actualización de mantenimiento
* **Octubre de 2011** - Las especificaciones EPUB 3.0 entraron en vigor
* **Junio de 2014**: se lanzó una actualización de mantenimiento menor para reemplazar la versión 3.0
* **Enero de 2017** - EPUB 3.1 entró en vigor

## Formato de archivo EPUB

El formato de archivo EPUB es un archivo que se puede renombrar a la extensión [ZIP](/es/compression/zip/) y su contenido se puede ver extrayendo el archivo con cualquier extractor de archivos. Es un formato abierto basado en XML y consta de archivos HTML, imágenes, hojas de estilo CSS y otros elementos. También se puede convertir a PDF, Mobi y varios otros formatos de archivo a través de varias aplicaciones de software y API.

{{< figure src="../epub.png" alt="Formato de archivo EPUB" >}}

**EPUB E-Book abierto con la aplicación Mac OS Books**

El formato de archivo EPUB se basa en los siguientes tres estándares abiertos.

### Estructura Pública Abierta (OPS) ###

Un archivo EPUB 2.0 usa XHTML 1.1 para construir el contenido de una publicación. En esencia, esto significa que un archivo EPUB consta de una o más páginas web. Aunque podría incluir todo el contenido de un libro o periódico en una sola página, es mejor que dicho archivo no supere los 300K, tanto por razones de rendimiento como de compatibilidad. Al igual que con las páginas web normales, el estilo y el diseño se definen mediante hojas de estilo en cascada (CSS). En los archivos EPUB, se debe usar un subconjunto (serie limitada de comandos) de CSS2. Muchas de las nuevas funciones de CSS3, como los cuadros redondeados o las sombras paralelas, aún no están disponibles. Para compatibilidad con versiones anteriores, un creador también puede usar DTBook en lugar de XHTML para codificar el contenido.

### Formato de empaquetado abierto (OPF) ###

Esta parte de las especificaciones se ocupa de la información estructural, como los metadatos (quién es el autor y el editor, cuál es el título,...), el manifiesto (una lista de todos los archivos dentro de un archivo epub) y la tabla de contenido. Todos estos datos están incrustados mediante XML.

### Formato de contenedor abierto (OCF) ###

Como las descripciones anteriores deberían haber dejado claro, un documento EPUB consta de una serie de archivos. Las especificaciones de OCF definen cómo todos esos archivos terminan siendo empaquetados en un solo archivo contenedor. La compresión ZIP se utiliza para esto.

## Formatos de archivo de imagen admitidos ##

El formato de archivo EPUB admite los siguientes formatos de archivo de imagen.

* [GIF](/es/image/gif/)
* [JPG](/es/image/jpeg/)
* [PNG](/es/image/png/)
* [SVG](/es/page-description-language/svg/)

## Referencias ##

* [EPUB - Por Wikipedia](https://en.wikipedia.org/wiki/EPUB)
