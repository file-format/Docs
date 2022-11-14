{
  "date" : "2019-10-11",
  "keywords" :[ "archivo tar", "formato de archivo tar", "qué es un archivo tar", "archivo", "ejemplo de tar", "extensión de archivo tar","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Formato de archivo de archivo Unix",
  "description":"Obtenga más información sobre qué es un archivo Tar y las API que pueden crear y abrir archivos TAR",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo TAR?

Los archivos con extensión .tar son archivos creados con una utilidad basada en Unix para recopilar uno o más archivos. Varios archivos se almacenan en un formato sin comprimir con la posibilidad de agregar archivos y carpetas al archivo. La utilidad TAR en Unix está basada en comandos, pero los archivos creados por lo tanto son compatibles con la mayoría de los sistemas de archivado de archivos en casi todos los sistemas operativos. Fue creado por primera vez en 1979 por AT&T Bell Laboratories y se publicaron versiones posteriores con el paso del tiempo.

## Formato de archivo TAR

TAR es un formato de archivo abierto con especificaciones completas disponibles para referencia del desarrollador. Su estructura de archivos fue estandarizada en POSIX.1-1988 y posteriormente en POSIX.1-2001. Los conjuntos de datos creados por tar conservan información sobre los parámetros del sistema de archivos, como:

* Nombre
* Marcas de tiempo
* Propiedad
* Permisos de acceso a archivos
* Organización del Directorio

Un archivo Tar no tiene ningún número mágico. Contiene una serie de bloques donde cada bloque es de bytes BLOCKSIZE.

Cada archivo archivado está representado por un bloque de encabezado que describe el archivo, seguido de cero o más bloques que dan el contenido del archivo. Al final del archivo de almacenamiento hay dos bloques de 512 bytes llenos de ceros binarios como marcador de fin de archivo. Un sistema razonable debería escribir dicho marcador de fin de archivo al final de un archivo, pero no debe asumir que existe tal bloqueo al leer un archivo. En particular, GNU tar siempre emite una advertencia si no lo encuentra.

Los bloques pueden bloquearse para operaciones de E/S físicas. Cada registro de n bloques (donde n se establece mediante el factor de bloqueo = opción de tamaño 512 para tar) se escribe con una única operación de "escritura()". En las cintas magnéticas, el resultado de tal escritura es un único registro. Al escribir un archivo, el último registro de bloques debe escribirse en tamaño completo, con bloques después del bloque cero que contengan todos ceros. Al leer un archivo, un sistema razonable debe manejar adecuadamente un archivo cuyo último registro es más corto que el resto, o que contiene registros basura después de un bloque cero.

### Encabezado de alquitrán

Como cualquier otro encabezado de archivo, el registro de encabezado de archivo tar contiene metadatos sobre un archivo y se muestra en la siguiente tabla.


|Desplazamiento de campo|Tamaño de campo (Bytes)|Campo
---|---|---|
|0|100|Nombre de archivo
|100|8|Modo archivo
|108|8|ID de usuario numérico del propietario
|116|8|ID de usuario numérico del grupo
|124|12|Tamaño del archivo en bytes (base octal)
|136|12|Hora de última modificación en formato de hora numérico Unix (octal)
|148|8|Suma de comprobación para registro de encabezado
|156|1|Indicador de enlace (tipo de archivo)
|157|100|Nombre del archivo vinculado

Los campos no utilizados se rellenan con bytes NUL. Un encabezado consta de 257 bytes que se rellena con bytes NUL para que se llene hasta un registro de 512 bytes.

## Referencias ##

* [TAR - Por Wikipedia](https://en.wikipedia.org/wiki/Tar_(informática))
* [Formato básico TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

