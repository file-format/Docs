{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Formato de archivo de imagen de disco",
  "description":"¿Qué es un archivo ISO y las API que pueden crear y abrir archivos ISO?",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## ¿Qué es un archivo ISO?

Un archivo con extensión .iso es un archivo de imagen de disco de archivo sin comprimir que representa el contenido de datos completos en un disco óptico como un CD o DVD. Basado en el estándar [ISO-9660](https://www.iso.org/standard/17505.html), el formato de archivo de imagen ISO contiene los datos del disco junto con la información del sistema de archivos que se almacena en él. La capacidad de los archivos ISO para contener una réplica exacta del contenido los convierte en el tipo de archivo perfecto para crear copias de CD/DVD y se utilizan principalmente para almacenar datos de arranque para la instalación. La mayoría de las veces, los archivos ISO se graban en USB/CD/DVD como contenido de arranque para arrancar la máquina para su instalación. Los archivos ISO tienen el tipo MIME application/x-iso9660-image.

## Formato de archivo ISO

El formato de archivo ISO no es como otros formatos de archivo de contenedor, aunque archiva el contenido de datos especificado. El archivo se crea como un archivo binario con la estructura exacta del contenido y la información del sistema de archivos. El formato de archivo ISO se describe en [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) de la siguiente manera.

### Estructura de nivel superior del archivo ISO

La estructura general del archivo consta de:

* `Área del sistema` - 32,768 bytes y no es utilizado por ISO_9660
* `Área de datos`: consiste en un conjunto de descriptores de volumen y tablas, directorios y archivos de ruta

### Conjunto de descriptores de volumen

El área de datos comienza con el conjunto de descriptores de volumen, un conjunto de uno o más descriptores de volumen terminados con un terminador de conjunto de descriptores de volumen. Estos actúan colectivamente como un encabezado para el área de datos, describiendo su contenido (similar al bloque de parámetros del BIOS utilizado por los discos con formato FAT, HPFS y NTFS).

Un conjunto de descriptores de volumen es como se muestra a continuación.

|Conjunto de descriptores de volumen|
---|
|Descriptor de volumen #1|
|...|
|Descriptor de volumen #N|
|Terminador de conjunto de descriptores de volumen|

#### Descriptor de volumen

Cada descriptor de volumen tiene un tamaño de 2048 bytes y tiene la siguiente estructura:

|Parte |Tipo |Identificador |Versión |Datos|
---|---|---|---|---|
|Tamaño |1 byte |5 bytes (siempre 'CD001') |1 byte (siempre 0x01) |2041 bytes|

## Referencias

* [Imagen de disco óptico - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Firmas de archivos](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

