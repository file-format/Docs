{
  "date" : "2019-12-13",
  "keywords" :[ "MP3", "archivo", "extensión", "formato", "Audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MP3 y las API que pueden abrir y crear archivos MP3",
  "title" :"MP3 - Formato de archivo de audio",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## ¿Qué es un archivo MP3?

Los archivos con la extensión .mp3 son formatos de archivo codificados digitalmente para archivos de audio que se basan formalmente en MPEG-1 Audio Layer III o MPEG-2 Audio Layer III. Fue desarrollado por el Grupo de expertos en imágenes en movimiento (MPEG) que utiliza compresión de audio de capa 3. La compresión lograda por el formato de archivo MP3 es 1/10 del tamaño de los archivos .WAV o .AIF. El formato brinda ventajas de transmitir dichos archivos de audio a través de Internet para escuchar en línea que antes no era posible debido al gran tamaño de los archivos de audio. La calidad del sonido de un archivo de audio MP3 se puede controlar mediante la configuración de parámetros como la velocidad de bits, la frecuencia de muestreo, el estéreo común o normal.

## Breve historia del formato de archivo MP3

El formato MP3 fue inventado y desarrollado por una empresa alemana, Fraunhofer-Gesellshart. El algoritmo tiene patentes con licencia para la tecnología de compresión que utiliza. Aquí hay una línea de tiempo útil de MP3:

• **1987**: el Instituto Fraunhofer de Alemania comenzó a investigar la codificación de audio de baja tasa de bits de alta calidad. Se llamó proyecto EUREKA EU147, Digital Audio Broadcasting.

• **Enero de 1988** - Se estableció el Grupo de expertos en imágenes en movimiento, o MPEG.

• **Abril de 1989** - Fraunhofer recibió una patente en Alemania para MP3.

• **1992** - Dieter Seitzer, quien ayudó a Fraunhofer con su investigación, integró su codificación de audio con MPEG-1.

• **1993** - Se publicó el estándar MPEG-1.

• **1994**: se desarrolló el estándar MPEG-2 y luego se publicó un año después.

• **Nov. 26 de enero de 1996** - Se emitió la patente estadounidense para MP3.

• **Septiembre de 1998**: Fraunhofer comenzó a hacer cumplir los derechos de patente. Quien haya utilizado la codificación de audio MP3 pagó una tarifa de licencia a Fraunhofer.

• **Febrero de 1999** - SubPop, una compañía discográfica, distribuyó música en formato MP3, la primera compañía de este tipo en hacerlo.

• **1999** - Aparecen los primeros reproductores de MP3 portátiles.

## Formato de archivo MP3

Un archivo MP3 consiste en cuadros MP3 donde cada cuadro consta de un encabezado y un bloque de datos. Los marcos no son independientes y, por lo general, no se pueden extraer en límites de marco arbitrarios. Los bloques de datos del archivo contienen información sobre el audio en términos de frecuencias y amplitudes. La palabra de sincronización en el encabezado identifica el comienzo de un marco válido. A esto le siguen 3 bits donde el primer bit muestra que es un estándar MPEG y los 2 bits restantes muestran que se usa la capa 3; por lo tanto, MPEG-1 Audio Layer 3 o MP3. Después de esto, los valores serán diferentes, dependiendo del archivo MP3.

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 define el rango de valores para cada sección del encabezado junto con la especificación del encabezado. La mayoría de los archivos MP3 actuales contienen [ID3](https://en.wikipedia.org/wiki/ID3) [metadatos](https://en.wikipedia.org/wiki/Metadata), que precede o sigue a los marcos MP3, como se indica en el diagrama. El flujo de datos puede contener una suma de comprobación opcional.

## Referencias ##

* [MP3 - Por Wikipedia](https://en.wikipedia.org/wiki/MP3)

