{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "archivo", "extensión", "formato", "MPEG-4", "Administración de derechos digitales", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Obtenga información sobre el formato de archivo M4V y las API que pueden crear y abrir archivos M4V",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## ¿Qué es un archivo M4V?

El formato de archivo **M4V**, desarrollado por Apple, es un contenedor de video protegido opcionalmente con protección de copia de Digital Rights Management (DRM) para proteger la privacidad o la copia. Los videos y las pistas de audio se envuelven en archivos contenedores para indexar y organizar las secuencias de reproducción. Además, los contenedores también brindan la función de capítulos similares a los de los DVD. Apple usa M4V para codificar videos en su iTunes Store. Protege la reproducción no autorizada a través de la protección de copia FairPlay de Apple al permitir que los archivos M4V se reproduzcan solo en computadoras autorizadas que tengan las cuentas utilizadas para comprar el video. Sin embargo, si se elimina la protección DRM de los archivos M4V, estos archivos se pueden reproducir en otros reproductores de video cambiando la extensión de .m4v a .mp4, razón por la cual los archivos M4V están asociados con MPEG-4. M4V usa H.264 para video y **[AAC](/es/audio/aac/)** y Dolby Digital para codificación y decodificación de audio.

## Estructura de archivo M4V ##

Los archivos M4V tienen fragmentos continuos con un encabezado de 8 bytes, un tamaño de fragmento de 4 bytes y un tipo de fragmento de 4 bytes en cada fragmento. El primer fragmento es "ftype" y tiene un subtipo en el desplazamiento 8. M4V definido por subtipo que debe ser "M4V_". Otros tipos de fragmentos son firmas predefinidas: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "cargar", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sincronización", "chap", "tmcd", "scpt", "ssrc", " PICTO". Iterando fragmentos, hasta que se detecta un tipo desconocido, creamos un archivo M4V.

Aquí hay un examen de una muestra: los datos binarios de un archivo m4v de muestra se inspeccionan a través de Hex Viewer y se puede observar que comienza con una firma **ftyp** (hexadecimal: 66 74 79 70) en el desplazamiento 4, que define QuickTime Tipo de archivo contenedor. El subtipo de archivo es **M4V_** (hex: 4D 34 56 20) que apunta al tipo de archivo M4V (MPEG-4). El tamaño del primer bloque es 32 (hex: 00 00 00 20, big-endian, byte alto primero), tamaño ubicado en el desplazamiento 0. En el desplazamiento 32 (hex: 20) se encuentra el segundo fragmento, que tiene un tamaño de 30,322 (hex : 00 00 76 72, big-endian, byte inferior primero) y escriba **moov** (hexadecimal: 6D 6F 6F 76). El siguiente fragmento se encuentra en el desplazamiento 32+30,322#30,354 (hex: 00 00 76 92) y tiene un tamaño 8 (hex: 00 00 00 08) y tipo **libre** (hex: 66 72 65 65).
### Códecs utilizados en M4V ###

#### Códec de vídeo H.264 ####

H.264 es un estándar de compresión de video que convierte el video digital en un formato que requiere menos espacio cuando se requiere transmisión o almacenamiento. M4V usa H.264 para la compresión de video. Su aplicación abarca desde DVD, TV, videoconferencia y transmisión de video por Internet. H.264 consta de dos partes principales: codificador, que comprime el video, decodificador, que descomprime el video comprimido. En la figura a continuación, se destacan los procesos de codificación y decodificación, y otros procesos están cubiertos en el estándar H.264.

##### Proceso de codificación y decodificación de video en H.264 #####

Para el flujo de bits H.264 comprimido, el codificador de video lleva a cabo el proceso de predicción, transformación y codificación. Al mismo tiempo, el decodificador lleva a cabo el proceso inverso de decodificación, transformación inversa y reconstrucción para producir el archivo de video. H.264 ocupa la mitad del tamaño de MPEG.

#### Códec de audio ####

La codificación de audio avanzada (AAC) es un códec de audio para la compresión de audio digital con pérdida y se utiliza en un contenedor M4V. AAC es el sucesor del formato [MP3](/es/audio/mp3/) y logra una mejor calidad que MP3 con la misma tasa de bits. El formato AAC desecha cierta información durante el proceso de compresión, que es de menor importancia. AAC es un códec basado en bloques de tasa de bits variable (VBR) en el que cada bloque se decodifica en 1024 muestras en el dominio del tiempo.

### Referencias ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

