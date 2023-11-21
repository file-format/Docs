{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo SHSH - Formato de archivo SHSH Blob de iPhone/iPod Touch",
  "description":"Aprenda qué es un archivo SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## ¿Qué es un archivo SHSH?

Un archivo SHSH, también conocido como Signature HaSH, es una firma digital utilizada por Apple para autenticar y verificar actualizaciones de firmware para dispositivos iOS como iPhone, iPad y iPod.

## Diferencia entre formatos de archivo SHSH y SHSH2

Al igual que un archivo SHSH2, el archivo SHSH contiene un identificador único para el dispositivo llamado "ECID" (ID de chip exclusivo), así como información sobre la versión de firmware instalada en el dispositivo. Sin embargo, los archivos SHSH se usaban en versiones anteriores de iOS (anteriores a iOS 10) y desde entonces han sido reemplazados por archivos SHSH2.

## Formato de archivo SHSH - Más información

Los archivos SHSH se guardan en el disco en formato de archivo binario. Los detalles de la estructura de archivos interna de este formato de archivo no están disponibles públicamente.

Los archivos SHSH son importantes para los usuarios que desean degradar el firmware de su dispositivo a una versión anterior que ya no está firmada por Apple. Al guardar los archivos SHSH para una versión de firmware específica cuando Apple todavía está firmada, los usuarios pueden usarlos más tarde para evitar la verificación de firma de Apple e instalar esa versión de firmware en su dispositivo. Este proceso también se conoce como "jailbreaking".

## Referencias

* [SHSH Blob - Por Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Ahorro TSS](https://tsssaver.1conan.com/v2/)

