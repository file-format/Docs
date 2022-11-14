{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "extensión", "archivo cdb", "formato de archivo cdb", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "qué es un archivo cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo CDB y las API que pueden crear y abrir archivos CDB",
  "title" :"CDB - Archivo de base de datos constante",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## ¿Qué es un archivo CDB?
Los archivos CDB se utilizan en aplicaciones de misión crítica como el correo electrónico. CDB significa "base de datos constante", un paquete rápido, confiable y simple para crear o leer bases de datos constantes. El reemplazo de la base de datos es seguro contra fallas del sistema. Los usuarios no tienen que hacer una pausa durante una reescritura. CDB funciona como una matriz asociativa (en disco), asigna claves a valores y permite que se almacenen múltiples valores en una sola clave.

## Formato de archivo CDB
El formato de archivo CDB almacena números, compensaciones, longitudes y valores hash en formato little endian como enteros de 32 bits sin signo. Se cree que las claves y los datos son cadenas de bytes opacas sin ningún tratamiento especial. Al comienzo de la base de datos, el encabezado de tamaño fijo representa 256 tablas hash enumerando su posición dentro del archivo y su longitud en ranuras. Por lo general, los datos se almacenan como una secuencia de registros, cada registro almacena la longitud de la clave, la longitud de los datos, la clave y los datos. No hay reglas de clasificación o alineación. Los registros son seguidos por un conjunto de 256 tablas hash de diferentes longitudes. Dado que cero es una longitud válida, puede haber menos de 256 tablas hash almacenadas físicamente en la base de datos, pero no se considera que sean 256 tablas. Las tablas hash consisten en una serie de ranuras, cada una de las cuales contiene un valor hash y un desplazamiento de registro. Las "ranuras vacías" tienen un desplazamiento de cero.

### Estructura
La base de datos CDB consta de un conjunto de datos completo en un solo archivo de computadora. Contiene tres partes:
- Un encabezado de tamaño fijo
- Datos
- Un conjunto de tablas hash.

Las búsquedas están disponibles solo para claves exactas. Las búsquedas actúan utilizando el siguiente algoritmo:

- Hash la clave.
- Determine en qué tabla hash y ranura debe ubicarse este registro.
- Pruebe la ranura indicada en la tabla hash.

Para búsquedas de claves con más de un valor, se pueden encontrar valores adicionales simplemente reanudando la búsqueda en el siguiente espacio.

#### Características

La estructura de la base de datos CDB proporciona varias características:

##### Búsquedas rápidas
Una búsqueda exitosa en una base de datos enorme normalmente requiere solo dos accesos al disco y una búsqueda fallida requiere solo uno.
##### Gastos indirectos bajos
Una base de datos utiliza 2048 bytes, 24 bytes por registro y el espacio para claves y datos.
##### Sin límites aleatorios
CDB puede administrar cualquier base de datos de hasta 4 gigabytes. Dado que no hay otras restricciones, los registros ni siquiera tienen que caber en la memoria. Las bases de datos se almacenan en un formato independiente de la máquina.
##### Reemplazo rápido de la base de datos atómica
El comando **cdbmake** puede reescribir una base de datos completa en dos órdenes de magnitud, más rápido que otros paquetes hash.
##### Vuelcos rápidos de bases de datos
**cdbdump** puede imprimir el contenido de una base de datos en formato compatible con cdbmake.


## Referencias ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [Especificación CDB](http://cr.yp.to/cdb.html)

