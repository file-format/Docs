{
  "date" : "2020-01-10",
  "keywords" :[ "archivo dib", "formato de archivo dib", "qué es un archivo dib", "archivo", "ejemplo de dib", "extensión de archivo dib","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Obtenga más información sobre el formato de archivo DIB y las API que pueden crear y abrir archivos DIB",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## ¿Qué es un archivo DIB?

Un mapa de bits independiente del dispositivo (DIB) es un archivo de imagen de trama que tiene una estructura similar a los archivos de mapa de bits estándar ([BMP]()/image/bmp/)). Contiene una tabla de colores que describe la asignación de colores RGB a los valores de píxeles. Esto permite que DIB represente la imagen en cualquier dispositivo. Se puede abrir con casi todas las aplicaciones que pueden abrir un archivo BMP estándar en Windows y macOS. DIB son archivos binarios y tienen un formato de archivo complejo similar a BMP. Las imágenes DIB son independientes de las capacidades de salida de los dispositivos de representación en términos de profundidad de color y píxel por pulgada.

## Especificaciones del formato de archivo DIB ##
Un DIB contiene la siguiente información de color y dimensión:

* El formato de color del dispositivo en el que se creó la imagen rectangular.
* La resolución del dispositivo en el que se creó la imagen rectangular.
* La paleta para el dispositivo en el que se creó la imagen.
* Una matriz de bits que asigna tripletes rojos, verdes y azules (RGB) a píxeles en la imagen rectangular.
* Un identificador de compresión de datos que indica el esquema de compresión de datos (si lo hay) utilizado para reducir el tamaño de la matriz de bits.

### Formato de bloque de datos DIB ###

DIB viene en el contexto del bloque de memoria en comparación con los archivos .DIB almacenados en el disco. El bloque de memoria se compone de una estructura que está de acuerdo con las especificaciones de la API de Windows para DIB. El DIB real consta de:
* Un encabezado
* Paleta de color
* Datos de píxeles

En la práctica, trabajar con datos de paleta, encabezado e imagen se realiza como si fueran tres bloques de memoria separados. Se asigna un identificador a este bloque de memoria común mediante GlobalAlloc y se conoce como HDIB, que se utiliza para extraer y trabajar con el encabezado, la tabla de colores y los datos de píxeles.

### Estructuras ###
La información contenida en un DIB está representada por diferentes estructuras. Éstos incluyen:

BITMAPInfo: define la información de dimensión y color para un DIB.
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Consiste en un BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
seguido de dos o más estructuras RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bits de datos ###
|Bits|Descripción|
---|---|
|Formato de 1 bit (monocromo)|Los mapas de bits monocromáticos constan de dos colores (blanco y negro). Debido a este número limitado de colores, estos mapas de bits ocupan menos espacio en el disco. bitBitCount devuelve verdadero o falso para la representación de ambos colores. La mayoría de las aplicaciones se saltan la paleta por completo si bitBitCount==1.
|Formato de 4 bits (VGA o 16 colores)|Cada byte de datos de imagen representa dos píxeles y bitBitCount==4. Estos bits representan el color del píxel en orden descendente.
|Formato de 8 bits (256 colores)|Este formato de 8 bits puede representar un máximo de 256 colores. Cada byte en la matriz de datos de mapa de bits de la imagen representa un solo píxel. El valor de ese byte es el número de la entrada de la paleta de colores que se usará de las 256 entradas representadas por bmciColors.
|Formato de 24 bits (TrueColor)|Estos mapas de bits pueden tener un máximo de 2^24 colores (biBitCount == 24). Cada secuencia de tres bytes en la matriz de datos de mapa de bits representa las intensidades relativas de los tres tonos primarios de un píxel. Los tonos se describen como valores que van de 0 a 255 y se almacenan en los tres bytes en el orden Azul, Verde y Rojo. Esta es una distinción importante, porque la mayoría de las referencias a colores en Windows usan el orden opuesto: rojo/verde/azul, así que piense en "BGR" cuando trabaje con imágenes TrueColor en lugar de "RGB". Se puede especificar una paleta de colores para acelerar el proceso de dibujo para Windows, en cuyo caso biClrUsed no será 0. Pero como puede ver, no es necesario, ya que los datos de píxeles contienen la información de color.
|Formato de 32 bits|Las imágenes de 32 bits tienen un máximo de 2^24 colores (biBitCount == 24).

## Referencias ##
* [Mapas de bits independientes del dispositivo: de Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

