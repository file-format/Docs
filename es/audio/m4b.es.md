{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "archivo", "extensión", "formato", "qué es el formato de archivo m4b", "música", "formato de archivo m4b", "M4b vs MP3", "especificación de formato de archivo m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo M4B y las API que pueden crear, convertir y abrir archivos M4B",
  "title" :"M4B - Formato de archivo de audiolibro MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## ¿Qué es un archivo M4B?

El archivo con extensión .m4b es un audiolibro generalmente utilizado por los libros de Apple e iTunes. El audio utilizado en este formato se almacena en MPEG-4 y se comprime mediante la codificación AAC. Un archivo M4B es muy similar a M4A, pero admite funciones relacionadas con audiolibros, como marcadores y saltos de capítulo. Los archivos M4B están disponibles tanto en versiones habilitadas para DRM como sin DRM. Los audiolibros encriptados con DRM suelen ser audiolibros de pago de iTunes Store. Mientras que, DRM gratis se puede encontrar fácilmente en Internet.

## Formato de archivo M4B

Los archivos de audiolibros que contienen metadatos, imágenes, marcadores e hipervínculos se pueden guardar con la extensión .m4a, pero generalmente se usa la extensión .m4b al guardar, solo para especificar que el archivo tiene un formato de archivo de audiolibro. Apply utiliza Fairplay DRM (Gestión de derechos digitales) para proteger sus archivos M4B. Por lo tanto, los archivos descargados de iTunes solo se pueden reproducir en dispositivos o computadoras autorizados.


## M4B frente a M4A

Tanto M4B como [MP3](https://docs.fileformat.com/audio/mp3/) son formatos de archivo de solo audio.

**M4B**: gana en comparación con MP3 en términos de calidad si se codifican ambos a la misma tasa de bits. El M4B es un archivo de audiolibro que se comprime mediante la codificación AAC. Básicamente está asociado con la "capa de audio MPEG-4", los archivos con extensión .m4b son la capa de audio de las películas MPEG-4 pero con características adicionales relacionadas con audiolibros. Su objetivo es superar al MP3 y convertirse en el nuevo estándar en compresión de audio. Es muy parecido al MP3 en muchos sentidos, pero desarrollado para tener una mejor calidad en un tamaño de archivo igual o incluso más pequeño. El formato M4B fue introducido por primera vez por Apple. El tipo de formato también se realiza como Apple Lossless Encoder (ALE).

Por lo tanto, actualmente el M4B no pudo obtener el éxito general del MP3 porque el formato de audio aún no se puede reproducir comúnmente.

**Mp3**: Un formato de audio digital muy familiar para todos. Un formato de compresión muy primero en la escena y se hizo muy famoso entre los oyentes de música. Su éxito generalizado es tan rápido que el tipo de archivo se puede reproducir universalmente y es compatible con casi cualquier cosa, hardware o software. En un sentido general, el M4A producirá una mejor calidad de sonido, pero muchos argumentarán que, sea cierto o no, la diferencia de sonido no es comparable y sería una pérdida de tiempo tratar de convertir archivos MP3 en archivos M4A. Finalmente, la conversión solo hará que pierdas la calidad de sonido original.

## Especificación de formato de archivo M4B

Al igual que [M4A](/es/audio/m4a/), los archivos M4B también constan de fragmentos consecutivos. Cada fragmento tiene un encabezado de 8 bytes y se subdivide como:
- Tamaño de fragmento de 4 bytes (big-endian, byte alto primero)
- Tipo de fragmento de 4 bytes: una de las firmas predefinidas: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "saltar", "jP2", "ancho", "cargar", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Similar a M4A, el primer fragmento en M4B será de tipo "ftype" y tiene un subtipo en el desplazamiento 8. El M4B definido por subtipo que debe ser "M4B_".

Iterando fragmentos, hasta que se detecte un fragmento de tipo desconocido, se compondrá un archivo M4B (audio MPEG-4).

## Referencias

* [MPEG-4 Parte 14 - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Ejemplo de formato y recuperación de audio MPEG-4 Parte 14 (M4A, M4B, M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

