{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo QT - Archivo de película rápida",
  "keywords" :[ "QT", "Video QuickTime", "formato qt", "cómo reproducir archivos qt", "Archivo de película rápida", "QTFF", "video", "Apple" ],
  "description":"Obtenga más información sobre el formato de archivo QT y las API que pueden crear y abrir archivos QT",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## ¿Qué es un archivo QT?

Un archivo con una extensión .qt es un archivo contenedor multimedia que utiliza el marco QuickTime para almacenar contenidos de archivos multimedia. Desarrollado por Apple Inc., el formato de archivo QuickTime (QTFF) es un archivo contenedor multimedia que contiene audio, video o texto para su reproducción posterior. Es el formato elegido para el intercambio de medios digitales entre dispositivos, aplicaciones y sistemas operativos. Los archivos QT también se guardan en formato [MOV](/es/video/mov/) que también fue desarrollado por Apple Inc. Algunas de las aplicaciones que pueden abrir archivos QT incluyen Apple QuickTime player, VLC media player y Media Player Classic con K- Paquete de códecs Lite.

## Formato de archivo QT

El QTFF está orientado a objetos que expone una colección flexible de objetos para facilitar el análisis y la expansión. Cada pista en un archivo QT contiene un flujo de medios codificado digitalmente o una referencia de datos al flujo de medios ubicado en otro archivo. La estructura de datos jerárquica que consta de objetos llamados átomos actúa como contenedores de pistas. Las especificaciones de formato de archivo para [formato de archivo QT](https://developer.apple.com/documentation/quicktime-file-format) están oficialmente disponibles por Apple Inc para referencia del desarrollador.

### Descripción de los medios

La descripción multimedia de un archivo QuickTime se almacena por separado de los datos multimedia. La información como el número de pistas, el formato de compresión de video y la información de tiempo se almacena en la descripción del medio (también conocido como recurso de película, átomo de película o simplemente la película). Los datos de medios están referenciados por un índice en esta estructura de medios. Los datos multimedia son los datos de muestra reales, como fotogramas de video y muestras de audio, que se usan en la película.

### Átomos

Atom es la unidad básica del archivo QuickTime. Hay dos campos principales en cualquier átomo antes que cualquier otro campo: los campos Tamaño y Tipo. El campo de tamaño muestra el tamaño del átomo, mientras que el campo de tipo indica el tipo de datos almacenados en el átomo. Por naturaleza, los átomos son jerárquicos, lo que significa que un átomo puede contener otros átomos que aún pueden contener otros. El diseño de un átomo de muestra se muestra en la siguiente imagen.

Cada átomo tiene dos partes, encabezado y datos. El encabezado contiene los campos de tamaño y tipo y la parte de datos contiene los datos reales. Además, cada campo se explica a continuación:

#### Tamaño del átomo

El encabezado y el contenido del átomo se indican mediante un número entero de 32 bits conocido como el tamaño del átomo. El campo de tamaño contiene el tamaño del átomo en bytes, expresado en un número entero sin signo de 32 bits.

#### Tipo de átomo

El tipo de átomo también se muestra mediante un número entero de 32 bits, que generalmente se trata como un campo de cuatro caracteres con valor knemonic, como 'moov' (0x6D6F6F76) para un átomo de película, o 'trak' (0x7472616B) para un átomo de pista. Una vez que se conoce el tipo de átomo, permite interpretar sus datos.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Estructura de archivo ##

Los archivos QT/MOV constan de fragmentos consecutivos. Cada fragmento tiene un encabezado de 8 bytes: tamaño de fragmento de 4 bytes (big-endian, byte alto primero) y tipo de fragmento de 4 bytes: una de las firmas predefinidas: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "gratis", "saltar", "jP2", "ancho", "cargar", "ctab", "imap", "mate", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". El primer fragmento es de tipo "ftype" y tiene un subtipo en el desplazamiento 8. MOV definido por subtipo que debe ser "qt". Para componer un archivo MOV, es necesario iterar fragmentos hasta que se detecte un tipo desconocido.

Aquí hay un ejemplo de muestra: al inspeccionar los datos binarios de un archivo MOV de muestra, es evidente que comienza con una firma **ftyp** (hexadecimal: 66 74 79 70) en el desplazamiento 4, que define el tipo de archivo contenedor de QuickTime. El subtipo de archivo es **qt~_~_** (hex: 71 74 20 20) que apunta al tipo de archivo MOV. El tamaño del primer bloque es 32 (hex: 00 00 00 20, big-endian, byte alto primero), tamaño ubicado en el desplazamiento 0. En el desplazamiento 32 (hex: 20) se encuentra el segundo fragmento, que tiene un tamaño de 8 y escriba **mdat** (hexadecimal: 6D 64 61 74).

El siguiente bloque está ubicado en el desplazamiento 32+8#40 (hex: 28) y tiene un tamaño de 3,263,028 (hex: 00 31 CA 34) y tipo **mdat** (hex: 6D 64 61 74) en el desplazamiento 44 (hex : 2C). El siguiente fragmento se encuentra en el desplazamiento 40 + 3263028#3263068 (hex: 00 31 CA 5C) y tiene un tamaño de 21 189 (hex: 00 00 52 C5) y tipo **moov** (hex: 6D 6F 6F 76) en el desplazamiento 1.836.019.574 (hex: 00 31 CA 60). Este es el último fragmento, por lo que el tamaño total del archivo es 3 263 068+21 189#3 284 257 bytes.

## Referencias ##

* [Formato de archivo QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [Formato de archivo QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

