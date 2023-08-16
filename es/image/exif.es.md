{
  "date" : "2019-10-11",
  "keywords" :[ "archivo exif", "formato de archivo exif", "qué es un archivo exif", "archivo", "ejemplo exif", "extensión de archivo exif","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Obtenga información sobre el formato de archivo EXIF y las API que pueden crear y abrir archivos EXIF",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo EXIF?
EXIF significa "Formato de archivo de imagen intercambiable", la definición dada por primera vez por [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) en 1985. El estándar es administrado por Japan Electronics y Asociación de Industrias de Tecnologías de la Información (JEITA) a partir de hoy. EXIF es un estándar para las especificaciones de formatos de imagen y sonido utilizados principalmente por cámaras digitales y escáneres.

El estándar EXIF incluye la información de etiquetado y metadatos con el archivo de imagen. Los metadatos pueden contener información como el modelo de la cámara, la velocidad del obturador, la fecha y la hora, la apertura, el fabricante, el tiempo de exposición, la resolución X, la resolución Y, etc. Normalmente, los datos EXIF están ocultos de forma predeterminada. Para ver los datos EXIF, uno tiene que seleccionar las propiedades de visualización dentro de la aplicación de visualización de imágenes. Los metadatos Exif también pueden incluir miniaturas junto con datos técnicos y de imágenes primarias en un solo archivo de imagen.

## Historial y Versiones ##

* En octubre de 1995, JEIDA estableció la Versión 1. En esta versión, JEIDA definió la estructura, que consiste en formato de datos de imagen e información de atributos, y etiquetas básicas.
* Noviembre de 1997, se introdujo la versión 1.1 con la mayoría de las etiquetas de la versión 1, pero también se agregaron disposiciones para información de atributos opcionales y operación de formato.
* Junio de 1998, versión 2 con espacio de color sRGB, miniaturas comprimidas y archivos de audio.
* Diciembre de 1998, Versión 2.1 con información mejorada de atributos y almacenamiento.
* Febrero de 2002, Versión 2.2, versión 2.1 mejorada con la adición de acabado de impresión.
* Septiembre de 2003, versión 2.21 con espacio de color opcional conocido como adobe RGB.

## Formato de archivo EXIF

EXIF utiliza los siguientes formatos de archivo con la adición de metadatos específicos.

1. [JPEG](/es/image/jpeg/) - transformada de coseno discreta (DCT) para archivos de imagen comprimidos.
1. [TIFF](/es/image/tiff/) Rev. 6.0 (RGB o YCbCr) para archivos de imagen sin comprimir.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) para archivos de audio (Lineal [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) o ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM para datos de audio sin comprimir, y [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) para datos de audio comprimido).

### Marcador utilizado por EXIF ###

El marcador 0xFFE0~~0xFFEF es "Marcador de aplicación", utilizado por la aplicación del usuario. Por ejemplo, las cámaras digitales más antiguas utilizan JFIF (formato de intercambio de archivos JPEG) para almacenar imágenes. JFIF utiliza el marcador APP0 (0xFFE0) para insertar datos de configuración de cámara digital e imágenes en miniatura. Además, EXIF también usa un marcador de aplicación para insertar datos, pero EXIF usa el marcador APP1 (0xFFE1) para evitar un conflicto con el formato JFIF. Todos los formatos de archivo EXIF comienzan con este formato.


|Marcador SOI|Marcador APP1|Datos APP1|Otro marcador
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Comienza desde el marcador SOI (0xFFD8), por lo que es un archivo JPEG. Entonces el Marcador APP1 sigue inmediatamente. Todos los datos de EXIF se almacenan en esta área de datos APP1. La parte de "SSSS" en la tabla superior significa el tamaño del área de datos APP1 (área de datos EXIF). Tenga en cuenta que el tamaño "SSSS" también incluye el tamaño del descriptor. Después de "SSSS", se inician los datos de APP1. La primera parte es un dato especial para la identificación si EXIF o no, se utilizan caracteres ASCII "EXIF" y 2 bytes de 0x00. Después del área del marcador APP1, siguen los otros marcadores JPEG.

### Estructura de datos Exif ###

Una estructura aproximada de datos EXIF (APP1) se muestra a continuación. Como se discutió anteriormente, los datos EXIF comienzan con el carácter ASCII "EXIF" y 2 bytes de 0x00, luego siguen los datos EXIF. EXIF utiliza el formato TIFF para almacenar datos.


|FFE1|APP1 Marcador
---|---|
|SSSS|Datos de APP1|Tamaño de datos de APP1
|45786966 0000|Encabezado Exif
|49492A00 08000000|Encabezado TIFF
|XXXX. . . .|IFD0 (imagen principal)|Directorio
|LLLLLLLL|Enlace a IFD1
|XXXX. . . .|Área de datos de IFD0
|XXXX. . . .|Exif SubIFD|Directorio
|00000000|Fin del enlace
|XXXX. . . .|Área de datos de Exif SubIFD
|XXXX. . . .|IFD1(imagen en miniatura)|Directorio
|00000000|Fin del enlace
|XXXX. . . .|Área de datos de IFD1
|FFD8XXXX. . . XXXXFFD9|Imagen en miniatura

#### Encabezado TIFF ####

El encabezado del archivo [TIFF](/es/image/tiff/) de 8 bytes contiene la siguiente información:

`Bytes 0-1:` El orden de bytes utilizado en el archivo. Los valores legales son: “II” (4949.H) “MM” (4D4D.H).

En el formato "II", el orden de los bytes es siempre del byte menos significativo al byte más significativo, tanto para enteros de 16 bits como de 32 bits. Esto se denomina orden de bytes little-endian. En el formato "MM", el orden de los bytes siempre es del más significativo al menos significativo, tanto para enteros de 16 bits como de 32 bits. Esto se denomina orden de bytes big-endian.

`Bytes 2-3:` Un número arbitrario pero cuidadosamente elegido (42) que identifica aún más el archivo como un archivo TIFF. El orden de los bytes depende del valor de los bytes 0-1.

`Bytes 4-7:` El desplazamiento (en bytes) del primer IFD. El directorio puede estar en cualquier ubicación del archivo después del encabezado, pero debe comenzar en un límite de palabra. En particular, un directorio de archivos de imagen puede seguir los datos de imagen que describe. Los lectores deben seguir los punteros donde sea que los lleven. El término desplazamiento de bytes siempre se usa en este documento para referirse a una ubicación con respecto al comienzo del archivo TIFF. El primer byte del archivo tiene un desplazamiento de 0.

#### Directorio de archivos de imágenes ####

Un IFD contiene información sobre la imagen, así como punteros a los datos reales de la imagen. Consiste en un recuento de 2 bytes del número de entradas del directorio (es decir, el número de campos), seguido de una secuencia de entradas de campo de 12 bytes. , seguido de un desplazamiento de 4 bytes del siguiente IFD (o 0 si no hay ninguno). Debe haber al menos 1 IFD en un archivo TIFF y cada IFD debe tener al menos una entrada.

##### Entrada IFD #####

Cada entrada IFD de 12 bytes tiene el siguiente formato.


|Bytes|Descripción
---|---|
|0-1|La etiqueta que identifica el campo
|2-3|El tipo de campo
|4-7|Recuento del tipo indicado
|8-11|La compensación de valor, la compensación de archivo (en bytes) del valor para el campo. Se espera que el valor comience en un límite de palabra; la compensación de valor correspondiente será, por lo tanto, un número par. Este desplazamiento de archivo puede apuntar a cualquier parte del archivo, incluso después de que los datos de la imagen

Un campo TIFF es una entidad lógica que consta de una etiqueta TIFF y su valor. Este concepto lógico se implementa como una Entrada IFD, más el valor real si no encaja en la parte de valor/compensación, los últimos 4 bytes de la Entrada IFD. Los términos campo TIFF y entrada IFD son intercambiables en la mayoría de los contextos.

#### Imagen en miniatura ####

El formato Exif contiene una miniatura de la imagen (excepto Ricoh RDC-300Z). Por lo general, se encuentra al lado del IFD1. Hay 3 formatos para miniaturas; Formato JPEG (JPEG usa YCbCr), formato RGB TIFF, formato YCbCr TIFF.

##### Miniatura en formato JPEG #####

Si el valor de la etiqueta de compresión (0x0103) en IFD1 es '6', el formato de imagen en miniatura es JPEG. La mayor parte de la imagen Exif usa el formato JPEG para la miniatura. En ese caso, puede obtener el desplazamiento de la miniatura con la etiqueta JpegIFOffset(0x0201) en IFD1, el tamaño de la miniatura con la etiqueta JpegIFByteCount(0x0202). El formato de datos es el formato JPEG ordinario, comienza en 0xFFD8 y termina en 0xFFD9. Parece que el formato JPEG y el tamaño de 160x120 píxeles son el formato de miniatura recomendado para Exif2.1 o posterior.

##### Miniatura en formato TIFF #####

Si el valor de la etiqueta de compresión (0x0103) en IFD1 es '1', el formato de imagen en miniatura no tiene compresión (llamada imagen TIFF). El punto de inicio de los datos de la miniatura es la etiqueta StripOffset(0x0111), el tamaño de la miniatura es la suma de la etiqueta StripByteCounts(0x0117).

## Referencias ##

* [EXIF - Por Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [Formato de archivo EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

