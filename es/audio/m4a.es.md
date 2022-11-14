{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "archivo", "extensión", "formato", "qué es el formato de archivo m4a", "música", "formato de archivo m4a", "M4A vs MP3", "especificación de formato de archivo m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo M4A y las API que pueden crear, convertir y abrir archivos M4A",
  "title" :"M4A - Archivo de audio MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## ¿Qué es un archivo M4A?

El **formato de archivo M4A** es un archivo de audio creado mediante AAC (Codificación de audio avanzada), que se conoce como compresión con pérdida. La palabra M4A abreviada como MPEG 4 Audio. Estos archivos de audio suelen tener la extensión de archivo .m4a. Esto es especialmente cierto en el caso del contenido no protegido. Puede almacenar varios tipos de contenido de audio, como audiolibros, canciones y podcasts. M4A generalmente se presenta como un formato más avanzado que MP3, que normalmente no se diseñó solo para audio. Es solo una capa de audio en archivos de video MPEG 1 o 2.

El formato M4A está encriptado por FairPlay Digital Rights Management, tal como se vendió a través de iTunes Store, use la extensión .m4p. Los iPhones de Apple usan audio MPEG-4 para sus tonos de llamada, pero esos archivos de audio usan la extensión .m4r.


## M4A frente a MP3

Tanto M4A como [MP3](https://docs.fileformat.com/audio/mp3/) son formatos de archivo de solo audio.

**M4A**: mejor que MP3 en términos de calidad y tamaño cuando se codifica a la misma tasa de bits. La extensión de archivo .m4a es tan común porque Apple la ha utilizado para su uso en iTunes Music Store. El M4A es un archivo de audio comprimido con tecnología MPEG-4; un algoritmo para la compresión con pérdida. Básicamente está asociado con la “capa de audio MPEG-4”, los archivos con extensión .m4a son la capa de audio de las películas MPEG-4. Pretende superar al MP3 y convertirse en el nuevo estándar en compresión de audio. Está muy cerca del MP3 en muchos sentidos, pero se introdujo para tener una mejor calidad en un tamaño de archivo igual o incluso más pequeño. Apple introdujo por primera vez el formato M4A. El tipo de formato también se realiza como Apple Lossless Encoder (ALE).

Por lo tanto, actualmente el M4A no pudo obtener el éxito general del MP3 porque el formato de audio aún no se puede reproducir en general. De alguna manera, está limitado solo a MacOS, iPod y otros productos de Apple.

**Mp3**: El formato de audio digital más famoso. También fue uno de los primeros formatos de compresión en la escena y se hizo muy popular entre los amantes de la música. Su éxito en la corriente principal es tan rápido que el tipo de archivo se puede reproducir universalmente y con casi cualquier cosa, hardware o software. En un sentido general, el M4A producirá una mejor calidad de sonido, pero muchos argumentarán que, sea cierto o no, la diferencia de sonido no es distinguible y sería una pérdida de tiempo tratar de convertir archivos MP3 en archivos M4A. Eventualmente, la conversión solo hará que pierdas la calidad de sonido original.

## Especificación de formato de archivo M4A

Los archivos M4A consisten en fragmentos consecutivos. Cada fragmento tiene un encabezado de 8 bytes y se subdivide como:
- Tamaño de fragmento de 4 bytes (big-endian, byte alto primero)
- Tipo de fragmento de 4 bytes: una de las firmas predefinidas: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "ancho", "carga", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

El primer fragmento será del tipo "ftype" y tiene un subtipo en el desplazamiento 8. El M4A definido por el subtipo que debe ser "M4A_", para el subtipo M4B debe ser "M4B_" y para el subtipo M4P debe ser "M4P_".

Iterando fragmentos, hasta que se detecte un fragmento de tipo desconocido, se compondrá un archivo M4A (audio MPEG-4).

## Referencias ##

* [MPEG-4 Parte 14 - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Ejemplo de formato y recuperación de audio MPEG-4 Parte 14 (M4A, M4B, M4P)] (https://www.file-recovery.com/m4a-signature-format.htm)

