{
  "date" : "2021-07-29",
  "keywords" :[ "archivo shx", "formato de archivo shx", "qué es un archivo shx", "archivo", "ejemplo de shx", "extensión de archivo shx","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Formato de índice de forma de archivo Shapefile",
  "description":"Obtenga información sobre el formato de archivo SHX y las API que pueden crear y abrir archivos SHX",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## ¿Qué es un archivo SHX?
El archivo SHX pertenece al formato de índice de forma, que es un índice posicional de la geometría característica para permitir buscar hacia adelante y hacia atrás rápidamente. El SHX es un archivo de compensación de acceso directo. No hay datos en este archivo, solo una copia duplicada de los primeros cien bytes, el número de registro y el desplazamiento al byte inicial de ese registro en el shp. Tenga en cuenta que el archivo con la extensión .shx no vincula [SHP](/es/gis/shp) y [DBF](/es/database/dbf).

## formato de archivo SHX
El formato SHX contiene un índice posicional de la geometría característica y un encabezado de 100 bytes similar al archivo SHP, seguido de cualquier número de registros de longitud fija de 8 bytes que contienen los dos campos siguientes:
| bytes | Tipo | Endianidad | Uso |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | grande | Compensación de registro (en palabras de 16 bits) |
| 4–7 | int32 | grande | Longitud del registro (en palabras de 16 bits) |

Este índice hace posible buscar hacia atrás en el archivo de forma, primero, buscando hacia atrás en el índice de forma y luego leyendo el desplazamiento del registro. Ese desplazamiento se puede usar para buscar la posición correcta en el archivo SHP. También puede buscar hacia adelante; un número arbitrario de registros usando el mismo método. Aunque es posible generar un índice completo junto con un archivo SHP, puede aumentar las posibilidades de corromper el archivo SHP rápidamente.


## Referencias

* [Shapefile - por Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


