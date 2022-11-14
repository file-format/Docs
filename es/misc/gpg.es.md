{
  "date" : "2022-02-17",
  "keywords" :["archivo gpg", "formato de archivo gpg", "qué es un archivo gpg", "archivo", "ejemplo gpg", "extensión de archivo gpg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo GPG - Archivo de claves públicas de GNU Privacy Guard",
  "description":"Obtenga información sobre el archivo GPG y las API que pueden crear y abrir archivos GPG",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## ¿Qué es un archivo GPG?

Un archivo GPG es un archivo de clave de cifrado/descifrado que utiliza el programa de cifrado GNU Privacy Guard (GnuPG). El programa GnuPC en sí está basado en el estándar OpenPGP como se define en RFC4880 y también se conoce como PGP. La clave para el uso exitoso de GPG en un sistema operativo moderno es su versátil sistema de administración de claves. La utilidad de línea de comandos de GPG le permite integrarse fácilmente con otras aplicaciones.

## Formato de archivo GPG

Los archivos GPG se guardan como archivos binarios encriptados y, por supuesto, no son legibles por humanos. Para descifrar un archivo GPG encriptado, debe usar la misma clave segura. Y es por eso que se desconoce el formato de archivo interno de estos archivos.

## Cifrar y descifrar archivos con GPG en Linux

La utilidad de línea de comandos GPG se puede utilizar para cifrar y descifrar archivos en Linux.

### Cifrado de un archivo

Un archivo se puede cifrar usando el comando gpg con la opción -c (crear) como se muestra a continuación.

```
gpg -c file1.txt
```
Ejecutar este comando solicita una frase clave con la que cifrar el contenido del archivo original `file1.txt`. Esto da como resultado la creación del archivo cifrado file1.txt.gpg.

### Descifrar y extraer un archivo

Para descifrar y extraer un archivo cifrado, se puede utilizar el siguiente comando.

```
gpg cfile.txt.gpg
```

## Referencias

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

