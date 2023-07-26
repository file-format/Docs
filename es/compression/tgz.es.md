{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo TGZ - Archivo Tar comprimido con Gzip",
  "description":"Obtenga información sobre el formato de archivo TGZ y las API que pueden crear y abrir archivos TGZ",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## ¿Qué es un archivo TGZ?

Un archivo con la extensión .tgz es un archivo TAR, que consta de varios archivos y carpetas, que se ha comprimido con el software de compresión Gnu Zip (gzip). Un archivo [TAR](/es/compression/tar/) generalmente combina varios archivos en un solo archivo para realizar copias de seguridad o distribuirlos a través de Internet. Es un archivo descomprimido hasta que se comprime con el software gzip, después de lo cual se convierte en el archivo TGZ. Los archivos TGZ, al ser archivos comprimidos, ocupan menos espacio en el disco y son fácilmente transferibles a través de Internet por correo electrónico. Algunas aplicaciones que pueden abrir archivos TGZ incluyen WinZip, Apple Archive Utility, 7-Zip y WinRAR. Los archivos TGZ se utilizan principalmente en los sistemas UNIX y Linux.

## Formato de archivo TGZ

Los archivos TGZ se guardan como archivos binarios comprimidos utilizando el algoritmo de compresión [GZ](/es/compression/gz/).

## Cómo descomprimir el archivo .tgz en Linux

En el sistema operativo Linux/Unix, el siguiente comando se puede usar para descomprimir archivos TGZ desde la línea de comandos.

```
tar zxvf tgzCompressedFile.tgz
```

El comando anterior descomprime el archivo TGZ comprimido y extrae sus archivos del archivo TAR al disco.
## Referencias ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

