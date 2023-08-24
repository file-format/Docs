{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PET - Archivo de paquete de instalación de Puppy Linux",
  "description":"Obtenga información sobre el formato de archivo PET y las API que pueden crear y abrir archivos PET",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## ¿Qué es un archivo PET de Linux?

Un archivo PET es un archivo de paquete de instalación de aplicaciones creado y utilizado con la variante PuppyLinux del sistema operativo Linux. Se crea como un archivo comprimido [TGZ](/es/compression/tgz/) que reduce el tamaño del archivo comprimido. La integridad del formato de archivo PET está garantizada por la suma de comprobación md5sum que se adjunta al final del archivo para su verificación en el extremo remoto. Los archivos PET se pueden extraer utilizando el extractor de archivos TGZ estándar y WinRAR. Los archivos PET reemplazaron los antiguos archivos de instalación del paquete [PUP](/es/compression/pup/).

## Formato de archivo PET

Los archivos PET se guardan en el disco como archivos comprimidos en formato de archivo binario. Sin embargo, no se conocen los detalles del formato de archivo interno del formato de archivo PET. Al igual que los archivos de instalación del paquete [.exe](/es/executable/exe/) y [.msi](/es/executable/msi/), los archivos PET inician una instalación cuando se ejecutan.

## Referencias

* [CachorroLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Índice de paquetes PET de PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

