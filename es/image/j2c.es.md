{
  "date" : "2019-10-11",
  "keywords" :[ "archivo j2c", "formato de archivo j2c", "qué es un archivo j2c", "archivo", "ejemplo j2c", "extensión de archivo j2c","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Obtenga más información sobre el formato de archivo J2C y las API que pueden crear y abrir archivos J2C",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## ¿Qué es un archivo J2C?

Un archivo con la extensión .j2c es una variante del formato de archivo JPEG y se comprime con la compresión wavelet. Tiene un sistema de marcadores y segmentos casi idéntico al formato de archivo JPEG 2000. El formato de archivo J2C es como se define en la Parte 1 de la base JPEG 2000 que admite compresión con pérdida y sin pérdida. El flujo de código JPEG 2000 se diseñó para incorporarse en [JP2](/es/image/jp2/) u otro formato de archivo, aunque puede aparecer en un archivo por sí mismo. Un archivo J2C se puede abrir con Adobe Photoshop 2020, Adobe Illustrator 2020 y Corel Paintshop Pro.

## Formato de archivo J2C

El formato de archivo J2C es el mismo que el de JPEG 2000, que a menudo se guarda como .jp2 y .jpc. Esto hace que los archivos J2C sigan el mismo enfoque de codificación de metadatos en formato XML donde se utiliza el estándar 12234-1 como referencia entre las etiquetas Exif y los componentes XML. Se mejora aún más con la extensión JPEG 2000 parte 2 que combina el mecanismo de animación y las configuraciones de flujo de código en una sola imagen. Dichos archivos con formato de archivo extendido se guardan como [.jpx](/es/image/jpx/).

### Diseño de un archivo JPEG2000

JPEG2000 admite una variedad de aplicaciones basadas en la conformidad para formatos de archivo extensibles. Aunque el tipo más simple puede contener una sola imagen, los tipos más complejos pueden incluir una serie de imágenes, apiladas una encima de otra o secuenciadas en función del tiempo.

#### Caja JP2
Es el bloque de construcción de nivel superior del formato de archivo JP2 y contiene campos de tipo y longitud en el encabezado y una sección de datos. El tipo de caja más notable es la caja de tren codificado contiguo. Este cuadro almacena en su sección de datos el código de flujo JPEG2000.

#### JPEG2000 CodeStream

El CodeStream JPEG2000 es una secuencia de bytes que se requiere para decodificar la imagen comprimida JPEG2000. En caso de que el archivo no tenga nada más que este flujo de código, se denomina archivo de flujo de código sin procesar. Por lo general, un flujo de código JPEG es la aplicación del algoritmo de compresión JPEG2000 en una imagen, aunque no es la única forma.

#### Piezas de baldosas ####

Una imagen codificada en JPEG2000 es una colección de unidades de datos llamadas paquetes. Estos paquetes se mantienen en el tren codificado dentro de grupos de paquetes denominados piezas de mosaico. Antes de codificar una imagen, el codificador divide la imagen en una cuadrícula rectangular de bloques, llamados mosaicos, donde cada mosaico se codifica por separado, independientemente de los demás mosaicos.

{{< figure src="../JPEG2000_Codestream.png" alt="Formato de archivo JPEG2000" >}}

## Compresión J2C
JPEG 2000 utiliza la tecnología de compresión wavelet, lo que lo hace rápido debido al hecho de que se muestran relativamente pocos píxeles en cualquier ventana o ventana en la que el espectador muestre la imagen. Esto se puede enfatizar por el hecho de que solo unos pocos megabytes de píxeles aparecerán en la pantalla para imágenes de gran tamaño (en gigabytes). Esto ayuda a obtener y renderizar rápidamente solo la parte de los datos de la imagen que se requiere para llenar los píxeles de la pantalla. Esto también requiere tecnología de descompresión de alta velocidad para acelerar el mecanismo de obtención de imágenes para crear las imágenes requeridas sobre la marcha.

J2C aprovecha la descompresión rápida y obtiene solo la información necesaria para que los datos de píxeles representen parte de las imágenes visibles rápidamente en las pantallas. J2C está diseñado principalmente para la visualización de datos y no para editarlos.

## Identificación J2C
Los archivos JPEG 2000 tienen bytes de firma `FF 4F FF 51`.

### Tipos de mimos
Los tipos Mime registrados para archivos JPEG 2000 incluyen:
* imagen/j2c
* imagen/jpx
* imagen/jpm
* vídeo/mj2

## Mejoras sobre el estándar JPEG
Las mejoras sobre el estándar JPEG incluyen:
* Rendimiento de compresión superior
* Representación de resolución múltiple
* Transmisión progresiva por píxel y precisión de resolución
* Opción de compresión sin pérdida o con pérdida
* Resiliencia de errores, formato de archivo flexible
* Soporte de alto rango dinámico
* Información espacial del canal lateral

## Referencias ##
* [Taubman, David; Marcelino, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

