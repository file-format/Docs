{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo SHSH2 - Formato de archivo blob SHSH de iOS",
  "description":"Aprenda qué es un archivo SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## ¿Qué es un archivo SHSH2?

Un archivo SHSH2, también conocido como blob SHSH o ECID SHSH, es una firma digital utilizada por Apple para autenticar y verificar actualizaciones de firmware para dispositivos iOS como iPhone, iPad y iPod. Contiene un identificador único para el dispositivo que se conoce como ECID (Exclusive Chip ID). También contiene información sobre la versión de firmware instalada en el dispositivo.

## Formato de archivo SHSH2 - Más información

Los archivos SHSH2 se guardan en el disco en formato de archivo binario y los detalles de la estructura de archivos interna de este formato de archivo no están disponibles públicamente.

Cuando se instala una nueva versión de iOS en un dispositivo Apple como iPhone, iPad o Mac, se genera un archivo SHSH2. Este archivo SHSH2 se envía a los servidores de Apple, que leen y verifican este archivo de firma digital. En base a esta información, el servidor permite o impide la instalación.

Lo mismo ocurre cuando se solicita una actualización. Cuando un usuario solicita una actualización o restauración de su dispositivo a través de iTunes u otro software, los servidores de Apple verificarán que el archivo SHSH2 coincida con el ECID y la versión de firmware del dispositivo antes de permitir que continúe la actualización.

## Referencias

* [SHSH Blob - Por Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Ahorro TSS](https://tsssaver.1conan.com/v2/)

