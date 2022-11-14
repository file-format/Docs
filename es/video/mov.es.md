{
  "date" : "2019-10-11",
  "keywords" :[ "archivo mov", "formato de archivo mov", "qué es un archivo mov", "archivo", "ejemplo de mov", "extensión de archivo mov", "extensión", "formato", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo MOV - Formato de archivo de película Apple QuickTime",
  "description":"Obtenga información sobre el formato de archivo MOV y las API que pueden crear y abrir archivos MOV",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## ¿Qué es un archivo MOV?

Un archivo MOV es un tipo de archivo de video, desarrollado por Apple Inc., que contiene una o más pistas. Cada pista almacena una película, audio, clips de película y subtítulos. Es un contenedor multimedia que puede almacenar diferentes tipos de elementos multimedia. El formato de video MOV es compatible con los sistemas Windows y Macintosh. Utiliza codificación MPEG-4 para la compresión y las pistas se mantienen en objetos llamados átomos que se colocan en una estructura de datos jerárquica.

## Breve historia del formato de archivo MOV

El formato de archivo MPEG-4 ha evolucionado a partir de la especificación del formato de archivo QuickTime (**QTFF**) en 2001. La Organización Internacional de Normalización aprobó el formato y las especificaciones del sistema MPEG-4 Parte 1 se publicaron en 1999. En 2001, se publicó un archivo de revisión Se publicó el formato [MP4](/es/video/mp4/).

La primera versión de MP4 se revisó en 2003 como MPEG-4 Parte 14 (ISO/IEC 14496-14:2003). En 2004, MP4 se generalizó para definir una estructura general para todos los archivos multimedia basados en el tiempo. Por lo tanto, ahora se utiliza como base para varios otros formatos de archivos multimedia.

## Formato de archivo QuickTime (QTFF) - Más información

Para trabajar con multimedia digital, QTFF puede contener muchos tipos de datos. Es un formato ideal para el intercambio de medios digitales, ya que el formato define los estándares para describir cualquier tipo de estructura de medios. El formato de archivo consta de una colección flexible de objetos orientados a objetos. Para el almacenamiento de películas en discos, QuickTime utiliza dos estructuras, es decir, `átomos` y `átomos QT`.

### Átomos

Atom es la unidad básica del archivo QuickTime. Hay dos campos principales en cualquier átomo antes que cualquier otro campo: los campos Tamaño y Tipo. El campo de tamaño muestra el tamaño del átomo, mientras que el campo de tipo indica el tipo de datos almacenados en el átomo. Por naturaleza, los átomos son jerárquicos, lo que significa que un átomo puede contener otros átomos que aún pueden contener otros. El diseño de un átomo de muestra se muestra en la siguiente imagen.

Cada átomo tiene dos partes, `encabezado` y `datos`. El encabezado contiene los campos de tamaño y tipo y la parte de datos contiene los datos reales. Además, cada campo se explica a continuación:

### Tamaño del átomo

El encabezado y el contenido del átomo se indican mediante un número entero de 32 bits conocido como el tamaño del átomo. El campo de tamaño contiene el tamaño del átomo en bytes, expresado en un número entero sin signo de 32 bits.

### Tipo de átomo

El tipo de átomo también se muestra mediante un número entero de 32 bits, que generalmente se trata como un campo de cuatro caracteres con valor knemonic, como 'moov' (0x6D6F6F76) para un átomo de película, o 'trak' (0x7472616B) para un átomo de pista. Una vez que se conoce el tipo de átomo, permite interpretar sus datos.

### Átomos QT y contenedores Atom

Los átomos QT proporcionan un formato de almacenamiento de propósito general y tienen un encabezado extendido que consta de campos de tamaño, tipo, ID de átomo y recuento de átomos secundarios. Los átomos QT están envueltos en un contenedor de átomos, una estructura de datos única que tiene un encabezado con un número de bloqueos. Hay un átomo raíz en cada contenedor de átomos que es el átomo QT. El diseño del átomo QT se muestra en la siguiente figura.

El encabezado del contenedor QT atom tiene los siguientes datos:

Reservado: un elemento de 10 bytes con un valor de 0.

Lock Count: número entero de 16 bits con un valor de 0.

Los encabezados de átomos QT tienen los siguientes datos:

**Tamaño -** El encabezado y el contenido del átomo QT se indican en bytes mediante un número entero de 32 bits. En el caso de un átomo de hoja, este campo contiene el tamaño de un solo átomo.

**Tipo -** El tipo del átomo se indica mediante un número entero de 32 bits. En caso de que sea el átomo raíz, el valor se establece en 'sean'.

**ID del átomo:** es un número entero de 32 bits que muestra el ID del átomo y debe ser único para todos los hermanos. Átomo raíz siempre el valor del ID del átomo como 1.

**Reservado -** Un entero de 16 bits que debe establecerse en 0.

**Número de hijos -** Un número entero de 16 bits que indica el número de átomos hijos de un átomo.

**Reservado -** Un número entero de 32 bits que debe establecerse en 0.

## Estructura de archivos de archivos MOV

Los archivos MOV consisten en fragmentos consecutivos. Cada fragmento tiene un encabezado de 8 bytes: tamaño de fragmento de 4 bytes (big-endian, byte alto primero) y tipo de fragmento de 4 bytes: una de las firmas predefinidas: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "gratis", "saltar", "jP2", "ancho", "cargar", "ctab", "imap", "mate", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". El primer fragmento es de tipo "ftype" y tiene un subtipo en el desplazamiento 8. MOV definido por subtipo que debe ser "qt". Para componer un archivo MOV, es necesario iterar fragmentos hasta que se detecte un tipo desconocido.

Aquí hay un `ejemplo de muestra`: Al inspeccionar los datos binarios de un archivo MOV de muestra, es evidente que comienza con una firma **ftyp** (hexadecimal: 66 74 79 70) en el desplazamiento 4, que define el tipo de archivo contenedor de QuickTime. El subtipo de archivo es **qt~_~_** (hex: 71 74 20 20) que apunta al tipo de archivo MOV. El tamaño del primer bloque es 32 (hex: 00 00 00 20, big-endian, byte alto primero), tamaño ubicado en el desplazamiento 0. En el desplazamiento 32 (hex: 20) se encuentra el segundo fragmento, que tiene un tamaño de 8 y escriba **mdat** (hexadecimal: 6D 64 61 74).

El siguiente bloque está ubicado en el desplazamiento 32+8#40 (hex: 28) y tiene un tamaño de 3,263,028 (hex: 00 31 CA 34) y tipo **mdat** (hex: 6D 64 61 74) en el desplazamiento 44 (hex : 2C). El siguiente fragmento se encuentra en el desplazamiento 40 + 3263028#3263068 (hex: 00 31 CA 5C) y tiene un tamaño de 21 189 (hex: 00 00 52 C5) y tipo **moov** (hex: 6D 6F 6F 76) en el desplazamiento 1.836.019.574 (hex: 00 31 CA 60). Este es el último fragmento, por lo que el tamaño total del archivo es 3 263 068+21 189#3 284 257 bytes.

## ¿Cómo convertir archivos MOV?

Hay muchos reproductores multimedia y editores de video de software disponibles para convertir archivos MOV a otros formatos de archivo de video populares. Algunos de los reproductores multimedia que pueden convertir archivos MOV a otros formatos incluyen:

* Reproductor multimedia VideoLAN VLC
* Reproductor Eltima Elmedia

Varios reproductores multimedia y editores de video, incluido el reproductor multimedia VideoLAN VLC y Eltima Elmedia Player, pueden convertir archivos MOV a otros formatos. Este software puede convertir archivos MOV a los siguientes formatos de video.

* Vídeo MPEG-4 - [MP4](/es/video/mp4/)
* Vídeo WebM - [WEBM](/es/video/webm/)
* Flujo de transporte de video - [TS](/es/video/ts/)
* Formato de sistemas avanzados - [ASF](/es/video/ts/)
* Audio Ogg Vorbis - [OGG](/es/audio/ogg/)
* Audio MP3 - [MP3](/es/audio/mp3/)
* Códec de audio sin pérdida gratuito - [FLAC](/es/audio/flac/)
* Audio ONDA - [WAV](/es/audio/wav/)

## API de código abierto para archivos MOV

* [React Native API para convertir MOV a MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API de Python para reparar archivos MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API de Ruby para convertir MOV a GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referencias

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

