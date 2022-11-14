{
  "date" : "2021-04-08",
  "keywords" :[ "archivo deb", "formato de archivo deb", "qué es un archivo deb", "archivo", "ejemplo deb", "extensión de archivo deb","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Archivo de alquitrán comprimido Bzip",
  "description":"Obtenga información sobre el formato de archivo DEB y las API que pueden crear y abrir archivos DEB",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## ¿Qué es un archivo DEB?

Un archivo con extensión .deb es un formato de archivo de paquete binario de Debian disponible para la distribución de paquetes de software en el sistema operativo Linux. Consta de dos archivos de almacenamiento [TAR](/es/compression/tar/). El DPKG proporciona el mecanismo para leer e instalar los paquetes DEB. Los paquetes DEB se pueden instalar mediante la interfaz de administración de software de paquetes APT. Los archivos DEB tienen un tipo de medio de Internet como `application/vnd.debian.binary-package`.

## Formato de archivo DEB

Un archivo DEB consta de dos archivos de almacenamiento [TAR](/es/compression/tar/). Un archivo contiene la información de control y otro contiene los datos instalables.

### Organización del paquete

El archivo DEB es un archivo **ar** que tiene un valor mágico de `!<arch> `. Desde Debian 0.93, el mecanismo de archivo de los archivos DEB contiene tres archivos en un orden específico.

1. `Debian Binary` - Está destinado a tener una serie de líneas, separadas por saltos de línea. Actualmente, solo hay una línea que describe el número de versión. El número de versión actual es 2.0.
1. `Archivo de control`: contiene un archivo control.tar que tiene secuencias de comandos del mantenedor y metainformación sobre el paquete, como el nombre del paquete, la versión, las dependencias y el mantenedor.
1. `Archivo de datos`: es un archivo tar llamado data.tar y contiene los archivos multimedia instalables reales. El archivo se puede comprimir con gz, bz2, lzma o xz, y la extensión del archivo del archivo de datos cambia en consecuencia.

### Archivo de control

El archivo de control puede incluir contenidos de la siguiente manera.

* `control`: contiene una breve descripción del paquete, así como otra información, como sus dependencias.
* `md5sums`: contiene sumas de comprobación MD5 de todos los archivos del paquete para detectar archivos corruptos o incompletos.
* `conffiles` - Lista los archivos del paquete que deben ser tratados como archivos de configuración. Los archivos de configuración no se sobrescriben durante una actualización a menos que se especifique.
* `preinst`, postinst, prerm y postrm - Scripts opcionales que se ejecutan antes o después de instalar o eliminar el paquete
* `config` es un script opcional que admite el mecanismo de configuración de debconf.
* `shlibs` - Es una lista de dependencias de bibliotecas compartidas.

## Referencias

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(formato_de_archivo))
* [formato del paquete binario de Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

