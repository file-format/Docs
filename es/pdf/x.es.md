{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PDF/X",
  "description":"Obtenga más información sobre el formato de archivo PDF/X y las API que pueden crear y abrir archivos PDF/X",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# ¿Qué es un archivo PDF/X? #

PDF/X es un estándar ISO 15930 publicado en 2001 con un subconjunto de funciones PDF. El estándar se estableció y publicó en base a requisitos específicos de las industrias de impresión y publicación. Todos los requisitos para esta norma se diseñaron de acuerdo con las diversas necesidades de las industrias de impresión y publicación. PDF/X requiere que los archivos conformes estén completos, es decir, autónomos. Esto requiere que elementos como las fuentes utilizadas en la página formen parte del documento. Contenidos como 3D o video no pueden ser parte de un documento PDF/X. La información contenida en el documento PDF/X requiere que sea precisa.

## Estándares y revisiones de PDF/X ##

La familia de estándares PDF/X consta de varias versiones, cada una diseñada para un resultado especializado. El desarrollo de estos estándares tuvo como objetivo abordar las diversas necesidades de las industrias de impresión y publicación.

* `PDF/X-1a`: también conocido como el primer estándar de la familia PDF/X, PDF/X-1a requiere que todo el contenido forme parte del documento PDF para poder imprimirlo. No se permiten elementos del documento como fuentes, formularios, protección con contraseña y anotaciones visibles. PDF/X-1a tiene sus propios requisitos específicos, así como los relacionados con la transparencia y las capas permitidas. Estos también requieren que los elementos de impresión usen solo CMYK, escala de grises o colores directos, lo que da como resultado que no se usen espacios de color RGB o independientes del dispositivo. es para intercambios en los que todos los archivos deben entregarse en CMYK (y/o colores directos), sin datos RGB ni de gestión de color. PDF/X-1a también se conoce como Intercambio completo debido a la integridad de la información requerida por
* `PDF/X-3`: se introdujo en 2002 y eliminó muchas restricciones de PDF/X-1a. Esto permitió que los gráficos en un PDF/X-3 usaran espacios de color basados en CMYK, grescale, RGB, Lab e ICC. En realidad, se basa en los estándares de PDF 1.3 con [perfil ICC] (https://en.wikipedia.org/wiki/ICC_Profile). También se conoce como Gestión del color debido a la flexibilidad y las reglas que presenta en relación con los colores incluidos en un documento PDF.
* `PDF/X-4`: admite transparencias, por lo que PDF-X/4 contiene todos los datos necesarios para la salida sin acoplar.
* `PDF/X-5`: se basa en PDF/X-4 y agrega soporte para gráficos externos a través de XObjects de referencia, así como perfiles de n-colorant externos para la interpretación. Úselo para el intercambio parcial de datos de impresión utilizando la versión 1.6 de PDF

## Referencias ##

* [PDF/X - Por Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

