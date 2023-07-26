{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo SQLITE y las API que pueden crear y abrir archivos SQLITE",
  "title" :"Formato de archivo SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## ¿Qué es un archivo SQLite?

Un archivo con extensión .sqlite es un archivo de base de datos SQL ligero creado con el software [SQLite](https://www.sqlite.org/index.html). Es una base de datos en un archivo en sí mismo e implementa un motor de base de datos [SQL](/es/database/sql/) autocontenido, completo y altamente confiable. Los archivos de la base de datos SQLite se pueden usar para compartir contenido enriquecido entre sistemas simplemente intercambiando estos archivos a través de la red. Casi todos los móviles y ordenadores utilizan SQLite para almacenar y compartir datos, y es el formato de archivo elegido para aplicaciones multiplataforma. Debido a su uso compacto y facilidad de uso, viene incluido dentro de otras aplicaciones. Los enlaces de SQLite existen para lenguajes de programación como C, [C#](/es/programming/cs), [C++](/es/programming/cpp), [Java](/es/programming/java/), [PHP](/es/programming/php/ ), y muchos otros.

## Formato de archivo SQLite

SQLite en realidad es una biblioteca de lenguaje C que implementa SQLite RDBMS utilizando el formato de archivo SQLite. Con la evolución de nuevos dispositivos todos los días, su formato de archivo se ha mantenido compatible con versiones anteriores para adaptarse a dispositivos más antiguos. El formato de archivo SQLite se considera un formato de archivo a largo plazo para los datos.

### El archivo de base de datos

Una base de datos SQLite se mantiene completamente a través de dos archivos.
* Archivo de base de datos principal: contiene el estado completo de la base de datos SQLite
* Rollback Journal: almacena información adicional en un segundo archivo y se utiliza durante la realización de transacciones. En caso de que SQLite esté en modo WAL, se mantiene un archivo de registro de cabeza de escritura.

#### archivo diario

Este archivo está destinado a mantener toda la información mantenida en caso de que la última transacción no se pueda completar en casos como un bloqueo de la computadora. Este archivo se utiliza para restaurar el archivo de la base de datos a un estado coherente.

#### Páginas

El archivo principal de la base de datos SQLite consta de una o más páginas. En cualquier momento, cada página de la base de datos principal tiene un único uso, que es uno de los siguientes:

* La página de bytes de bloqueo
* Una página de lista libre
* Una página troncal de lista libre
* Una página de hoja de lista libre
* Una página de árbol b
* Una página interior de tabla b-tree
* Una página de hoja de tabla b-tree
* Una página interior de índice b-tree
* Una página de hoja de índice b-tree
* Una página de desbordamiento de carga útil
* Una página de mapa de puntero

El tamaño de los archivos de la base de datos SQLite puede oscilar entre unos pocos kilobytes y unos pocos gigabytes.

### Encabezado SQLite

El encabezado de la base de datos SQLite se encuentra en los primeros 100 bytes del archivo de la base de datos. Cada archivo de base de datos SQLite válido comienza con 16 bytes (en hexadecimal): 53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Los detalles de los campos de encabezado se muestran en la siguiente tabla.

|Desplazamiento|Tamaño|Descripción|
---|---|---|
|0|16|La cadena de encabezado: "Formato SQLite 3\000"|
|16|2|El tamaño de página de la base de datos en bytes. Debe ser una potencia de dos entre 512 y 32768 inclusive, o el valor 1 que representa un tamaño de página de 65536.|
|18|1|Versión de escritura del formato de archivo. 1 por legado; 2 para WAL.|
|19|1|Versión de lectura del formato de archivo. 1 por legado; 2 para WAL.|
|20|1|Bytes de espacio "reservado" no utilizado al final de cada página. Usualmente 0.|
|21|1|Fracción máxima de carga útil integrada. Debe tener 64 años.|
|22|1|Fracción mínima de cabida útil integrada. Debe tener 32.|
|23|1|Fracción de carga útil de la hoja. Debe tener 32.|
|24|4|Contador de cambio de archivo.|
|28|4|Tamaño del archivo de base de datos en páginas. El "tamaño de la base de datos en el encabezado".|
|32|4|Número de página de la primera página troncal de lista libre.|
|36|4|Número total de páginas libres.|
|40|4|La cookie de esquema.|
|44|4|El número de formato del esquema. Los formatos de esquema admitidos son 1, 2, 3 y 4.|
|48|4|Tamaño de caché de página predeterminado.|
|52|4|El número de página de la página de árbol b raíz más grande cuando se encuentra en los modos de vacío automático o vacío incremental, o cero en caso contrario.|
|56|4|La codificación de texto de la base de datos. Un valor de 1 significa UTF-8. Un valor de 2 significa UTF-16le. Un valor de 3 significa UTF-16be.|
|60|4|La "versión de usuario" tal como la lee y establece el pragma user_version.|
|64|4|Verdadero (distinto de cero) para el modo de vacío incremental. Falso (cero) en caso contrario.|
|68|4|El "ID de la aplicación" establecido por PRAGMA application_id.|
|72|20|Reservado para ampliación. Debe ser cero.|
|92|4|La versión válida para el número.|
|96|4|SQLITE_VERSION_NUMBER|

## Referencias ##

* [Formato de archivo SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - Especificaciones del lenguaje C](https://www.sqlite.org/c3ref/intro.html)

