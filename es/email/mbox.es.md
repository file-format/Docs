{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Archivo de buzón de correo electrónico",
  "description":"Obtenga información sobre el formato de archivo MBOX y las API que pueden crear y abrir archivos MBOX",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo MBOX?

El formato de archivo MBox es un término genérico que representa un contenedor para la recopilación de mensajes de correo electrónico. Los mensajes se almacenan dentro del contenedor junto con sus archivos adjuntos. Los mensajes de una carpeta completa se guardan en un solo archivo de base de datos y los mensajes nuevos se agregan al final del archivo. Numerosas aplicaciones y API brindan soporte para el formato de archivo MBox, como Apple Mail y Mozilla Thunderbird.

## Formato de archivo MBOX ##

El formato de archivo MBox permaneció sin estandarizar durante bastante tiempo hasta 2005, cuando la aplicación/mbox se estandarizó como [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Mensajes, en formato RFC 2822 , se concatenan dentro del formato de archivo MBox uno tras otro. Cada mensaje comienza con una línea de separación que identifica al remitente del mensaje y también identifica la fecha y la hora en que el destinatario final recibió el mensaje (ya sea el sistema de último salto en la ruta de transferencia o el sistema que sirve como el sistema del destinatario). almacén de correo). Cada mensaje normalmente termina con una línea vacía. El final de la base de datos generalmente se reconoce por la ausencia de datos adicionales o por la presencia de un marcador explícito de fin de archivo.

## Lectura de un mensaje del archivo MBox ##

Un lector escanea a través de un archivo mbox en busca de líneas From_. Cualquier línea From_ marca el comienzo de un mensaje. El lector no debe intentar aprovechar el hecho de que cada línea From_ (más allá del comienzo del archivo) es una línea en blanco. Una vez que el lector encuentra un mensaje, extrae un remitente del sobre (posiblemente corrupto) y la fecha de entrega de la línea From_. Luego lee hasta la siguiente línea From_ o el final del archivo, lo que ocurra primero. Elimina la última línea en blanco y elimina las comillas de las líneas >From_ y >>From_ y así sucesivamente. El resultado es un mensaje RFC 822.

## Consideraciones de codificación ##

El contenido de un archivo MBox puede mezclarse irreversiblemente cuando un correo electrónico recibido contiene un archivo Mbox como archivo adjunto y se guarda en otro archivo Mbox. Para evitar esto, los sistemas de mensajería deben codificar una base de datos mbox con codificación de transferencia no transparente (como BASE64 o Quoted-Printable) siempre que dicho objeto se transfiera a través de protocolos de mensajería. Los implementadores también deben estar preparados para codificar los datos de mbox localmente si se reciben datos no conformes.

## Referencias ##

* [MBox-RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

