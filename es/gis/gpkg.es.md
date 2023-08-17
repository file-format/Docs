{
  "date" : "2021-07-29",
  "keywords" :[ "archivo gpkg", "formato de archivo gpkg", "qué es un archivo gpkg", "archivo", "ejemplo de gpkg", "extensión de archivo gpkg","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Archivos de formato GeoPackage",
  "description":"Obtenga información sobre el formato de archivo GPKG y las API que pueden crear y abrir archivos GPKG",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## ¿Qué es un archivo GPKG?
Un archivo con extensión .gpkg consiste en un sistema de información geográfica implementado como un contenedor de base de datos SQLite que contiene tablas de datos y metadatos con definiciones típicas, limitaciones de formato, afirmaciones de integridad y restricciones de contenido. Fue publicado en 2014; definido por el OGC (Open Geospatial Consortium) en nombre del ejército de EE. UU. Varios gobiernos, organizaciones comerciales y de código abierto apoyan ampliamente el GeoPackage.

## formato de archivo GPKG
Un GeoPackage se compone de un archivo de base de datos SQLite 3 extendido; un estándar define un conjunto de reglas (convenciones requeridas) para:
- Almacenamiento de conjuntos de imágenes de matriz de teselas
- Características vectoriales
- Mapas ráster a varias escalas
- Metadatos y esquema

Puede extender un GeoPackage usando las reglas de extensión como se define en la cláusula 2.3 del estándar. El propósito de diseñar un GeoPackage fue hacer una base de datos lo más liviana posible e incluirla en un solo archivo listo para usar. Esto lo hace ideal para aplicaciones móviles en modo fuera de línea y uso compartido rápido en almacenamiento en la nube o dispositivos de almacenamiento USB, etc.

### Contenido de GPKG
Los GeoPackages contienen varias tablas, como otras bases de datos relacionales. Estas tablas pueden ser definidas por el usuario o tablas de metadatos. Los GeoPackages constan de dos tablas de metadatos obligatorias:

#### contenido_gpkg
Una tabla de contenido para un GeoPackage. Las columnas obligatorias en esta tabla son:

- **table_name**: el nombre real de la tabla de datos definida por el usuario;
- **tipo_de_datos**: el tipo de datos, por ejemplo, títulos, características y atributos;
- **identificador y descripción**: texto legible por humanos;
- **last_change**: la fecha informativa del último cambio, en formato ISO 8601;
- **min_x, min_y, max_x y max_y**: las extensiones espaciales del contenido. ;
- **srs_id**: sistema de referencia espacial.

#### gpkg_spatial_ref_sys
Para contenido de referencia espacial; incluyendo pero no limitado a mosaicos y características, cada fila en el contenido debe hacer referencia a un sistema de referencia de coordenadas; almacenado en la tabla **gpkg_spatial_ref_sys**. Las columnas obligatorias en esta tabla son:

- **srs_name, descripción**: un nombre legible por humanos y una descripción para el SRS;
- **srs_id**: un identificador único para el SRS; también la clave principal de la tabla;
- **organización**: nombre de la organización definidora que no distingue entre mayúsculas y minúsculas.
- **organization_coordsys_id**: ID numérico del SRS asignado por la organización;
- **definición**: Definición de texto conocido del SRS.


## Referencias

* [GeoPackage - por Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)
* [Primeros pasos con GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

