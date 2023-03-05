{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "archivo", "extensión", "formato", "qué es el formato de archivo m4p", "música", "formato de archivo m4p", "M4b vs MP3", "especificación de formato de archivo m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo M4P y las API que pueden crear, convertir y abrir archivos M4P",
  "title" :"M4P - Formato de archivo de audiolibro MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## ¿Qué es un archivo M4P?
El archivo con extensión .m4p es un archivo de audio que generalmente está disponible en la tienda iTunes de Apple para descargar. En otras palabras, podemos decir que M4P es un archivo AAC pero protegido contra copia mediante el uso de una gestión de derechos digitales (DRM). Significa que los archivos M4P solo se pueden reproducir en sistemas o dispositivos autorizados. Por lo general, los archivos M4P son específicos de los dispositivos multimedia de Apple. Por lo tanto, estos archivos solo se pueden reproducir en macbooks, podcasts y teléfonos inteligentes de Apple como iPhone 6 o iPhone 7.

## Formato de archivo M4P
El M4P significa MPEG 4 Protegido (audio), y codifica el audio con un códec de audio avanzado (AAC) y protege el archivo del uso no autorizado del archivo. Este formato de archivo generalmente se considera como un formato de archivo de audio de iTunes Music Store. Apple utiliza su sistema FairPlay Digital Rights Management (DRM) para proteger los archivos M4P. FairPlay DRM se basa en la tecnología desarrollada por Veridisc. Su mecanismo de protección funciona cifrando el flujo de audio AAC mediante el cifrado AES. El usuario recibe una clave maestra que se asigna a su cuenta para el descifrado. Este formato de archivo se introdujo como reemplazo del formato de archivo MP3, porque el MP3 no se pensó originalmente como un archivo de audio, sino como capa III en un archivo de video MPEG 1 o 2.


## Especificaciones del formato de archivo M4P

Al igual que [M4A](/es/audio/m4a/), los archivos M4P también constan de fragmentos consecutivos. Cada fragmento tiene un encabezado de 8 bytes y se subdivide como:
- Tamaño de fragmento de 4 bytes (big-endian, byte alto primero)
- Tipo de fragmento de 4 bytes: una de las firmas predefinidas: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "ancho", "carga", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

Similar a M4A, el primer fragmento en M4P será de tipo "ftype" y tiene un subtipo en el desplazamiento 8. El M4P definido por subtipo que debe ser "M4P_".

Iterando fragmentos, hasta que se detecte un fragmento de tipo desconocido, se compondrá un archivo M4P (audio MPEG-4).

## Referencias ##

* [MPEG-4 Parte 14 - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Ejemplo de formato y recuperación de audio MPEG-4 Parte 14 (M4A, M4B, M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

