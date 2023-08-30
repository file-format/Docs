{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo HDR - ¿Qué es un archivo de imagen HDR?",
  "description":"Obtenga información sobre el formato de archivo HDR y las API que pueden crear y abrir archivos HDR",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## ¿Qué es un archivo HDR?

Un archivo HDR es un formato de archivo de imagen ráster de alto rango dinámico (HDR) para almacenar fotos de cámaras digitales. Permite a los editores de fotos mejorar el color y el brillo de las imágenes digitales que tienen un rango dinámico limitado. Esta modificación puede mejorar el brillo alrededor de las esquinas, dando como resultado una imagen casi natural. Los archivos HDR generalmente se guardan como imágenes rasterizadas de 32 bits. Adobe Photoshop puede crear y abrir archivos HDR.

Los archivos HDR también se conocen como HDRI.

## Formato de archivo HDR - Más información

El formato de archivo HDR se basa en el formato de archivo Radiance Picture (.pic) original. Los datos de píxeles de un archivo HDR generalmente se almacenan sin comprimir, pero en algunos casos se comprimen mediante un sistema de codificación de longitud de ejecución sencillo.

### Estructura del archivo HDR

Un archivo de imagen HDR consta de las siguientes tres secciones:

* **Encabezado:** Un archivo HDR se identifica por los primeros bytes del archivo de imagen, es decir, "#?RADIANCE".
* **Cadena de resolución:** El encabezado va seguido de una sola línea de resolución que consta de 4 valores; una etiqueta X e Y, cada una seguida de un valor numérico entero. El orden de las X e Y indican la rotación. La combinación de X e Y con valores positivos y negativos cubre todas las orientaciones y rotaciones posibles de la imagen.
* **Datos de píxeles:** Los datos de píxeles de un archivo HDR se descomprimen o se comprimen mediante una codificación de longitud de ejecución estándar.

## API HDR/HDRI de código abierto

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Biblioteca [C++](/es/programming/cpp/) de encabezado único súper rápido multiplataforma para obtener el tamaño y el formato de la imagen sin cargar/decodificar.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Biblioteca Rust para obtener el tamaño y el formato de la imagen sin cargar/decodificar. Admite [.avif](/es/image/avif/), [.bmp](/es/image/bmp/), [.cur](/es/image/cur/), [.dds](/es/image/dds/), [. gif](/es/image/gif/), hdr (imagen), [heic (heif)](/es/image/heic/), [.icns](/es/image/icns/), [.ico](/es/image/ico /), [.jp2](/es/image/jp2/), [jpeg (jpg)](/es/image/jpeg/), [jpx](/es/image/jpx/), ktx, [png](/es/image/png /), [psd](/es/image/psd/), qoi, tga, tiff (tif) y webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Implementación Java de HdrHistogram.

## Referencias

* [Resplandor HDR](http://paulbourke.net/dataformats/pic/)
* [info de la imagen](https://github.com/xiaozhuai/imageinfo)

