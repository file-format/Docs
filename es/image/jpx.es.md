{
  "date" : "2021-02-10",
  "keywords" :[ "archivo jpx", "formato de archivo jpx", "qué es un archivo jpx", "archivo", "ejemplo jpx", "extensión de archivo jpx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Formato de archivo de imagen",
  "description":"Obtenga información sobre el formato de archivo JPX y las API que pueden crear y abrir archivos JPX",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## ¿Qué es un archivo JPX? ##

Un archivo con extensión .jpx es una extensión del formato de archivo JPEG 2000. Utiliza principalmente la compresión JPEG 2000 y también proporciona características avanzadas como múltiples capas para una imagen, varios espacios de color, opacidad y flujos de código fragmentados. JPX también permite otras compresiones como JBIG, CCITT Group3, CCITT Group4, etc. además de la compresión JPEG 2000. El formato de archivo JPX fue aprobado como estándar [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), pero no pudo recibir una buena acogida debido al uso extensivo de [JPEG ](/es/imagen/jpeg/) formato de archivo. Las aplicaciones que pueden abrir archivos JPX incluyen Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 y CorelDraw Graphics Suite 2020.

## Breve historia

En 2000, el comité del Grupo Conjunto de Expertos Fotográficos diseñó JP2 con el objetivo de mejorar su propio estándar JPEG basado en la transformada de coseno discreta con este nuevo método basado en wavelet. El comité de JPEG tenía como objetivo proporcionar sus métodos de referencia libres de tarifas de licencia. En la competencia de la licencia JP2 entre 20 empresas, ganaron por un pelo. JPEG 2000 ha sido declarado estándar ISO, aunque la mayoría de los navegadores web no están preparados para darle una mano a JPEG 2000 desde 2017. En 2004, el formato ISO/IEC 15444-2 se aceptó públicamente como extensión del formato de archivo JP2.

## Formato de archivo JPX

El formato de archivo JPX se formuló para cumplir con los requisitos de las aplicaciones que necesitaban estructuras de datos más allá de la funcionalidad definida por el formato de archivo [JP2](/es/image/jp2/). Un archivo JP2 con extensiones no compatibles podría generar confusión en el mercado donde algunos lectores pueden interpretar algunos archivos JP2 pero no otros. JPX es la respuesta para evitar este tipo de problemas en las aplicaciones.

### Identificación del archivo

Los archivos JPX se almacenan como [JPF](/es/image/jpf/) cuando se almacenan en un sistema de archivos informático tradicional. Es por eso que el término JPX se usa con menos frecuencia en comparación con el JPF. Un archivo JPX comienza con los siguientes bytes:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organización de archivos

Similar a JP2, un archivo JPX es una colección de casillas que tienen una estructura binaria con las casillas dispuestas en un orden contiguo. El primer cuadro da el inicio del archivo con su primer byte y el último byte del último cuadro representa el último byte del archivo.
La estructura binaria de un cuadro en un archivo JPX es idéntica a la definida en el formato de archivo [JP2](/es/image/jp2/).

### Almacenamiento de CodeStream en JPX

El formato de archivo JPX permite que el flujo de código de la imagen se divida en fragmentos. Esto hace posible modificar un solo mosaico de la imagen y escribir el mosaico modificado hasta el final del archivo sin volver a escribir todo el archivo. El formato de archivo original [JP2](/es/image/jp2/) restringe el almacenamiento de todo el flujo de código en una parte contigua del archivo, lo que puede ser problemático para las aplicaciones de edición de imágenes que deseen modificar un solo mosaico de la imagen y lograr la compatibilidad anterior con el formato de archivo JPX. La fragmentación del flujo de código de la imagen hace que el formato de archivo JPX sea superior al formato de archivo JP2. Además, el formato de archivo JPX permite combinar varios flujos de código y producir un resultado renderizado. Codestreams se pueden combinar como composición y animación.

## Referencias ##

* [Resumen de JPEG 2000](https://jpeg.org/jpeg2000)

