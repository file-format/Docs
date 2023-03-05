{
  "date" : "2019-10-11",
  "keywords" :[ "archivo mng", "formato de archivo mng", "qué es un archivo mng", "archivo", "ejemplo de mng", "extensión de archivo mng","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo MNG: formato de archivo de gráficos de red de imágenes múltiples",
  "description":"Obtenga información sobre el formato de archivo MNG y las API que pueden crear y abrir archivos MNG",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo MNG?

Un archivo con la extensión .mng es un formato de archivo de gráficos de red de múltiples imágenes que es similar al formato de imagen [PNG](/es/image/png/) pero admite imágenes animadas. Fue desarrollado para evitar sobrecargar el formato PNG con características adicionales de animaciones. MNG también es similar a los archivos [GIF](/es/image/gif/) pero usa más compresión y es compatible con la función alfa completa. El tipo de medio MIME no oficial para archivos MNG es video/x-mng. Los archivos MNG se pueden abrir en aplicaciones como ImageMagik e IrfanView.

## Formato de archivo MNG

El formato de archivo MNG es similar al de PNG y utiliza la misma estructura de fragmentos definida en las especificaciones de PNG. Un decodificador MNG debe poder decodificar los flujos de datos PNG sin especificar ningún indicador especial para las instrucciones de decodificación. MNG agrupa múltiples imágenes en un "marco", con algunas imágenes utilizadas como sprite para moverse de un lugar a otro. El mecanismo permite reutilizar datos de imágenes sin retransmitirlos. Se pueden consultar las [especificaciones de MNG](http://www.libpng.org/pub/mng/spec/) para referencia del desarrollador.

### Firma MNG

El flujo de datos MNG comienza con una firma de 8 bytes que contiene:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Esto es similar a la firma PNG pero contiene MNG en lugar de PNG.

Marco ### MNG

Un marco MNG consiste en una imagen bidimensional de imágenes más pequeñas. Se puede acceder a cada imagen pequeña usando la combinación de índice de fila y columna. El formato es capaz de almacenar datos de "vóxeles" tridimensionales que se organizan en una serie de planos bidimensionales. Cada plano está representado por un flujo de datos PNG o Delta-PNG. Cada flujo de datos Delta-PNG define una imagen como las diferencias de la imagen PNG principal. Esto proporciona una forma mucho más compacta de representar imágenes posteriores que usar un flujo de datos PNG completo para cada una.

## Referencias ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Formato MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

