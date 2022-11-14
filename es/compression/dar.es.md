{
  "date" : "2021-04-08",
  "keywords" :[ "archivo dar", "formato de archivo dar", "qué es un archivo dar", "archivo", "ejemplo de dar", "extensión de archivo dar","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Formato de archivo del archivador de disco",
  "description":"Obtenga información sobre el formato de archivo DAR y las API que pueden crear y abrir archivos DAR",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## ¿Qué es un archivo DAR?

Un archivo con la extensión .dar es un archivo comprimido creado con el archivo DAR Disk. Puede crear una copia de seguridad/archivo para un disco completo o un grupo de archivos. Fue creado para reemplazar el formato de archivo [TAR](/es/compression/tar/) en el sistema operativo UNIX y se puede crear como archivos divididos para una gran cantidad de archivos. El archivo DAR admite la opción de eliminar archivos del sistema que están vinculados a los archivos principales del archivo. Sus capacidades de proporcionar copias de seguridad diferenciales, incrementales y decrementales lo hacen superior a los archivos TAR.

## Formato de archivo DAR

Los archivos DAR son archivos comprimidos que pueden usar cualquier compresión por archivo como [gzip](/es/compression/gz/), [bzip2](/es/compression/bz2/), lzo, xz o lzma. El formato de archivo exacto de un archivo DAR depende del tipo de formato que se utilice para comprimir el contenido del archivo. También permite el cifrado opcional Blowfish, Twofish, AES, Serpent, Camellia y el cifrado y firma de clave pública (OpenPGP).

### Características de DAR

Algunas de las características del formato de archivo DAR son las siguientes.

* Se encarga de cualquier tipo de inodo (directorio, archivos sin formato, enlaces simbólicos, dispositivos especiales, canalizaciones con nombre, sockets, puertas, ...)
* Se encarga de los inodos con enlaces fijos (archivos planos con enlaces duros, dispositivos char, dispositivos de bloque, enlaces simbólicos con enlaces duros)
* Se encarga de archivos dispersos
* Se encarga de los atributos extendidos del archivo Linux,
* Se encarga del archivo ACL de Linux
* Se encarga de las bifurcaciones de archivos de Mac OS X
* Se encarga de algunos atributos específicos del sistema de archivos, como la fecha de nacimiento del sistema de archivos HFS+ y los atributos inmutables, de diario de datos, eliminación segura, fusión sin cola, imborrable, noatime del sistema de archivos ext2/3/4.
* Compresión por archivo con gzip, bzip2, lzo, xz o lzma (en lugar de comprimir todo el archivo). Una persona puede elegir no comprimir archivos ya comprimidos según el sufijo de su nombre de archivo.
* Extracción rápida de archivos desde cualquier lugar del archivo
* Listado rápido de los contenidos del archivo guardando el catálogo de archivos en el archivo
* Copia de seguridad del sistema de archivos en vivo: detecta cuándo se modificó un archivo mientras se leía para la copia de seguridad y puede volver a intentar guardarlo hasta un número máximo de reintentos determinado
* Archivo hash (MD5, SHA1 o SHA-512) generado sobre la marcha para cada segmento, el archivo resultante es compatible con md5sum o sha1sum, para poder verificar rápidamente la integridad de cada segmento
* Independiente del sistema de archivos: se puede usar para restaurar un sistema a una partición de un tamaño diferente y/o a una partición con un sistema de archivos diferente[5]

## Referencias

* [DAR](http://dar.linux.free.fr/)
* [Archivador de disco DAR](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

