{
  "date" : "2019-12-09",
  "keywords" :[ "archivo zip", "formato de archivo zip", "qué es un archivo zip", "archivo", "ejemplo zip", "extensión de archivo zip","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CÓDIGO POSTAL",
  "description":"¿Qué es un archivo ZIP y las API que pueden crear y abrir archivos ZIP?",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## ¿Qué es un archivo ZIP? ##

Un archivo con extensión .zip es un archivo que puede contener uno o más archivos o directorios. El archivo puede tener compresión aplicada a los archivos incluidos para reducir el tamaño del archivo ZIP. El formato de archivo ZIP se hizo público en febrero de 1989 por Phil Katz para lograr el archivado de archivos y carpetas. El formato se hizo parte de la utilidad [PKZIP](https://www.pkware.com/pkzip), creada por PKWARE, Inc. Inmediatamente después de la disponibilidad de [especificaciones disponibles](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT), muchas compañías hicieron que el formato de archivo ZIP fuera parte de sus utilidades de software, incluidas Microsoft (desde Windows 7), Apple (Mac OS X) y muchas otras.

## Breve historia del formato de archivo ZIP

La historia del formato de archivo ZIP se remonta al caso de una demanda presentada por System Enhancement Associates (SEA) contra PKWARE por usar su utilidad ARC sin permisos para su marca comercial y los derechos de autor de la apariencia del producto y la interfaz de usuario. Antes de esto, Phil Katz había reescrito el código fuente de SEA y lanzó PKXARC, un extractor ARC, y PKARC, un compresor de archivos, como software gratuito para sistemas basados en MS-DOS. Al perder en la demanda, PKWARE ya no pudo usar nada relacionado con ARC. Aquí es donde surgió la creación de una nueva compresión de archivos, denominada ZIP, que se convirtió en parte de la utilidad PKZIP en PKWARE, Inc.

Katz lanzó las especificaciones del formato de archivo ZIP al dominio público, al tiempo que retuvo los derechos de propiedad sobre su utilidad de compresión y extracción, es decir, PKZIP. El sistema de compresión ZIP fue (y es) capaz de archivar archivos en una carpeta por medio de un algoritmo de comprobación de redundancia cíclica de 32 bits ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) para comprimir archivos tamaños A diferencia de ARC, las carpetas .ZIP incluían un archivo de directorio que desempeñaba el papel de libro de códigos de un criptógrafo y contenía la información necesaria para procesar los archivos comprimidos.

## Métodos de compresión admitidos en ZIP

Según las especificaciones del formato de archivo .ZIP, se admiten los siguientes métodos de compresión.

* Almacenar - no implica compresión
* Encogerse
* Reducción (Esto implica factores de compresión que van desde el nivel 1 hasta el nivel 4)
* Implosión
* Desinflar
* Desinflado64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd versión I, Rev 1

DEFLATE es el método de compresión comúnmente utilizado, que es un algoritmo de compresión de datos sin pérdidas que utiliza una combinación de la codificación LZ77 y Huffman y se detalla en [RFC 1951] (https://tools.ietf.org/html/rfc1951).

## Especificaciones del formato de archivo ZIP

Los archivos ZIP tienen la capacidad de almacenar varios archivos utilizando diferentes técnicas de compresión y, al mismo tiempo, admiten el almacenamiento de un archivo sin ningún tipo de compresión. Cada archivo se almacena/comprime individualmente, lo que ayuda a extraerlos o agregar nuevos, sin aplicar compresión o descompresión a todo el archivo.

### Formato de archivo ZIP general

Cada archivo Zip está estructurado de la siguiente manera:


|Formato de archivo ZIP
---|
|Encabezado de archivo local 1
|Datos de archivo 1
|Descriptor de datos 1
|Encabezado de archivo local 2
|Datos de archivo 2
|Descriptor de datos 2
| ....
| ....
|Encabezado de archivo local N
|Datos de archivo N
|Descriptor de datos N
|Encabezado de descifrado de archivo
|Archivar registro de datos adicionales
|Directorio central

El formato de archivo ZIP utiliza un algoritmo CRC de 32 bits para fines de archivo. Para procesar los archivos comprimidos, un archivo ZIP tiene un directorio en su extremo que guarda la entrada de los archivos contenidos y su ubicación en el archivo de almacenamiento. Por lo tanto, desempeña el papel de codificación para encapsular la información necesaria para procesar los archivos comprimidos. Los lectores ZIP usan el directorio para cargar la lista de archivos sin leer todo el archivo ZIP. El formato mantiene copias duales de la estructura del directorio para brindar una mayor protección contra la pérdida de datos.

Cada archivo en un archivo ZIP se representa como una entrada individual donde cada entrada consta de un encabezado de archivo local seguido de los datos del archivo comprimido. El directorio al final del archivo contiene las referencias a todas estas entradas de archivo. Los lectores de archivos ZIP deben evitar leer los encabezados de los archivos locales y todo tipo de listado de archivos debe leerse desde el Directorio. Este directorio es la única fuente de entradas de archivos válidas en el archivo, ya que los archivos también se pueden agregar hacia el final del archivo. Es por eso que si un lector lee los encabezados locales de un archivo ZIP desde el principio, también puede leer entradas no válidas (eliminadas) que no forman parte del Directorio que se está eliminando del archivo.

El orden de las entradas del archivo en el directorio central no tiene por qué coincidir con el orden de las entradas del archivo en el archivo.

### Entradas de archivos ZIP

Las entradas en el archivo ZIP se organizan una tras otra, donde cada entrada consta de:

* Encabezado de archivo local
* Campos de datos adicionales opcionales
* Datos de usuario (opcionalmente comprimidos/opcionalmente encriptados)

El encabezado de archivo local de cada entrada representa información sobre el archivo, como comentario, tamaño de archivo y nombre de archivo. Los campos de datos adicionales (opcionales) pueden acomodar información para las opciones de extensibilidad del formato ZIP.

#### Encabezado de archivo local

El encabezado del archivo local tiene una estructura de campo específica que consta de valores de varios bytes. Todos los valores se almacenan en orden de bytes little-endian donde la longitud del campo cuenta la longitud en bytes. Todas las estructuras de un archivo ZIP utilizan firmas de 4 bytes para cada entrada de archivo. El final de la firma del directorio central es 0x06054b50 y se puede distinguir mediante su propia firma única. A continuación se muestra el orden de la información almacenada en el encabezado del archivo local.


|Compensación|Bytes|Descripción
---|---|---|
|0|4|Firma de encabezado de archivo local # 0x04034b50 (leído como un número little-endian)
|4|2|Versión necesaria para extraer (mínimo)
|6|2|Indicador de bit de propósito general
|8|2|Método de compresión
|10|2|Hora de última modificación del archivo
|12|2|Fecha de última modificación del fichero
|14|4|CRC-32
|18|4|Tamaño comprimido
|22|4|Tamaño sin comprimir
|26|2|Longitud del nombre del archivo (n)
|28|2|Longitud de campo adicional (m)
|30|n|Nombre de archivo
|30+n|m|Campo adicional

#### Encabezado del archivo del directorio central


|Compensación|Bytes|Descripción
---|---|---|
|0|4|Firma del encabezado del archivo del directorio central # 0x02014b50
|4|2|Versión realizada por
|6|2|Versión necesaria para extraer (mínimo)
|8|2|Indicador de bit de propósito general
|10|2|Método de compresión
|12|2|Hora de última modificación del archivo
|14|2|Fecha de última modificación del fichero
|16|4|CRC-32
|20|4|Tamaño comprimido
|24|4|Tamaño sin comprimir
|28|2|Longitud del nombre del archivo (n)
|30|2|Longitud de campo adicional (m)
|32|2|Longitud de comentario de archivo (k)
|34|2|Número de disco donde comienza el archivo
|36|2|Atributos de archivos internos
|38|4|Atributos de archivos externos
|42|4|Desplazamiento relativo del encabezado del archivo local. Este es el número de bytes entre el inicio del primer disco en el que se encuentra el archivo y el inicio del encabezado del archivo local. Esto permite que el software lea el directorio central para ubicar la posición del archivo dentro del archivo ZIP.
|46|n|Nombre de archivo
|46+n|m|Campo adicional
|46+n+m|k|Comentario de archivo

#### Fin del registro del directorio central


|Compensación|Bytes|Descripción
---|---|---|
|0|4|Fin de la firma del directorio central # 0x06054b50
|4|2|Número de este disco
|6|2|Disco donde comienza el directorio central
|8|2|Número de registros del directorio central en este disco
|10|2|Número total de registros del directorio central
|12|4|Tamaño del directorio central (bytes)
|16|4|Desplazamiento del inicio del directorio central, relativo al inicio del archivo
|20|2|Longitud del comentario (n)
|22|n|Comentario

## Referencias

* [Especificaciones del formato de archivo ZIP PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Estructura del archivo PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

