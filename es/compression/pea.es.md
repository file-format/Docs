{
  "date" : "2021-04-21",
  "keywords" :[ "archivo de guisante", "formato de archivo de guisante", "qué es un archivo de guisante", "archivo", "ejemplo de guisante", "extensión de archivo de guisante","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - Formato de archivo de archivo PeaZip",
  "description":"Obtenga información sobre el formato de archivo PEA y las API que pueden crear y abrir archivos PEA",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## ¿Qué es un archivo PEA?

Un archivo con extensión .pea, acrónimo de Pack, Encrypt y Authenticate, es un archivo [zip](/es/compression/zip/) creado con la aplicación de software de archivo [PeaZip](https://peazip.github.io/). Cuenta con compresión y salida de múltiples volúmenes, y ofrece un modelo de seguridad flexible a través de cifrado autenticado y criptografía. Esto proporciona privacidad y autenticación de los datos. La utilidad PeaZip está disponible como motor de código abierto que se puede compilar para diferentes sistemas operativos según los requisitos.

## Formato de archivo PEA

Las [especificaciones de formato de archivo PEA](https://peazip.github.io/pea_help.pdf) están disponibles públicamente para referencia del desarrollador. Los archivos PEA son archivos binarios con un modelo de seguridad flexible y verificaciones de integridad redundantes que van desde sumas de verificación hasta hashes criptográficamente fuertes. Esto define tres niveles diferentes de comunicación a controlar:

* Flujos: el flujo de datos de salida real que está formado por múltiples archivos de entrada y se puede escribir en múltiples volúmenes de salida
* Objetos: archivos de entrada y carpetas enviados al archivo .pea
* Volúmenes: archivo de almacenamiento de salida que se puede expandir al tamaño definido por el usuario

Cada uno de estos son opcionales y se pueden incorporar según los requisitos del usuario. El formato de archivo PEA puede almacenar una secuencia única que contiene objetos ilimitados. Cada flujo tiene un tamaño de hasta 2^64 bytes.

Los archivos PEA ofrecen verificación de integridad opcional y cifrado autenticado usando AES en modo EAX o HMAC, como alternativa Twofish y Serpent en modo EAX.

### Encabezado del archivo PEA

El encabezado del archivo tiene 10 bytes y está estructurado de la siguiente manera.

|Bytes|Descripción|
---|---|
|1 | Campo de byte mágico para desambiguación de formato de archivo: $EA|
|1 | Número de versión|
|1 | Número de revisión|
|1 | Esquema de control de volumen|
|1 | Declarar el sistema operativo donde se creó la secuencia |
|1 | Declaración de codificación de fecha y hora del sistema operativo |
|1 | Declaración de codificación de caracteres de nombres de objetos |
|1 | Declaración del tipo de CPU (codificado en 7 bits) y endianness (en msb) |
|1 | Reservado para uso futuro|

## Referencias

* [Especificaciones del formato de archivo PEA](https://peazip.github.io/pea_help.pdf)
* [Formato de archivo PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

