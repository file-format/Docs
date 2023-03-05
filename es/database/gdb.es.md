{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo GDB: archivo de geodatabase de archivos ESRI",
  "description":"Obtenga información sobre el formato de archivo GDB y las API que pueden crear y abrir archivos GDB",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## ¿Qué es un archivo GDB?

La geodatabase de archivos ESRI (FileGDB) es una colección de archivos en una carpeta en un disco que contiene datos geoespaciales relacionados, como conjuntos de datos de entidades, clases de entidades y tablas asociadas. Requiere que otros archivos se mantengan junto con el archivo .gdb en el mismo directorio para que funcione. Las consultas se pueden ejecutar en el archivo .gdb para administrar datos espaciales y no espaciales.

## Formato de archivo GDB - Más información

Las geodatabases de archivos se componen de siete tablas del sistema más los datos del usuario. Los datos del usuario se pueden almacenar en los siguientes tipos de conjuntos de datos:

* Clase característica
* Conjunto de datos de características
* Conjunto de datos de mosaico
* Catálogo de ráster
* Conjunto de datos ráster
* Conjunto de datos esquemáticos
* Tabla (no espacial)
* Cajas de herramientas

Los datasets de entidades pueden contener clases de entidades, así como los siguientes tipos de datasets:

* Archivos adjuntos
* Anotación vinculada a características
* Redes geométricas
* Conjuntos de datos de red
* Telas de paquetería
* Clases de relación
* Terrenos
* Topologías

El tamaño máximo predeterminado de los datasets en las geodatabases de archivos es de 1 TB. El tamaño máximo se puede aumentar a 256 TB para grandes conjuntos de datos (generalmente ráster). Esto está controlado por una palabra clave de configuración. Consulte Palabras clave de configuración para geodatabases de archivos para obtener más información.

Las geodatabases de archivos también pueden contener subtipos y dominios y participar en la replicación de check-in/check-in y réplicas unidireccionales.

Varios usuarios pueden acceder simultáneamente a una geodatabase de archivos. Si los usuarios están editando, deben editar diferentes conjuntos de datos.

## Especificaciones del formato de archivo GDB ##

El archivo GDB es un formato propietario de ESRI y sus especificaciones no están disponibles públicamente. Por esta razón, los detalles del formato de archivo para FIle GDB no se pudieron documentar en ningún otro lugar que no sea algunas fuentes que lo han hecho [parcialmente](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) mediante ingeniería inversa. .

## Referencias ##

* [Especificaciones de FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

