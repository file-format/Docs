{
  "date" : "2021-08-09",
  "keywords" :[ "archivo cso", "formato de archivo cso", "qué es un archivo cso", "archivo", "ejemplo cso", "extensión de archivo cso","extensión", "formato", "iso", "compresión DAX " ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo CSO y las API que pueden crear y abrir archivos CSO",
  "title" :"CSO - Imagen de disco ISO comprimida",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## ¿Qué es un archivo CSO?

Un archivo con la extensión .cso es un archivo de imagen ISO comprimido. El CSO es una alternativa al método de compresión DAX; también conocido como CISO; fue el primer método para comprimir los archivos [ISO](/es/compression/iso/) y suele ser el método preferido para archivar material de PlayStation Portable. Este formato utiliza la compresión Deflate, que puede incluir hasta nueve capas de compresión. Se utilizan programas como Prometheus y YACC para crear las imágenes.

## formato de archivo CSO

El formato de archivo CSO fue el primer método de compresión para ISO para ahorrar más espacio en la memoria. Las mejoras se hicieron de vez en cuando para una mejor compresión. El CSO está utilizando la compresión Deflate que tiene nueve niveles de preajustes, por lo general, cada nivel puede manejar bloques de 2 KiB individualmente. Si bien los niveles más altos de compresión pueden ralentizar y prolongar los tiempos de carga en el software que depende en gran medida de la transmisión de discos, también los niveles más bajos pueden realizar una compresión sustancial.

### Estructura del archivo CSO

El formato de archivo CSO contiene un encabezado de 24 bytes, bloques de datos y una tabla de índice. Little-endian se asume para campos más grandes que un byte. La arquitectura final de PlayStation Portable se muestra a continuación.

#### Encabezado

| Desplazamiento (bytes) | Nombre | Tamaño (bytes) | Propósito |
----------|----------|--------------|---------|
| 0x0 | Magia | 4 | Siempre CISO, o 0x4F534943 cuando se lee como un número entero de 32 bits. Este campo se utiliza para identificar un archivo CSO. Tenga en cuenta que este campo puede ser diferente para los otros derivados de CSO, por ejemplo, ZSO usó el código mágico ZISO. |
| 0x4 | Tamaño del encabezado | 4 | Para el formato de archivo CSO "v1" original, este campo se ignora y, por lo tanto, no es necesario que sea preciso. Sin embargo, el formato "v2" y ZSO requiere que este campo sea siempre 0x18 (24 bytes). |
| 0x8 | Tamaño sin comprimir | 8 | El tamaño del ISO original sin comprimir en bytes. |
| 0x10 | Tamaño de bloque | 4 | El tamaño de cada bloque de datos en bytes antes de la compresión. Por lo general, 2048 bytes, lo mismo que el tamaño de cada sector ISO 9660. |
| 0x14 | Versión | 1 | La versión del formato de archivo en uso. Para el formato "v1", el valor puede ser 0 o 1. Para el formato "v2", debe ser 2. Además, el formato ZSO requiere que sea 1. |
| 0x15 | Alineación del índice | 1 | La alineación de cada entrada de índice, especificada en bits. |
| 0x16 | Reservado | 2 | Este campo no se utiliza. En el formato "v1", este campo se ignora y puede contener valores arbitrarios. En el formato "v2", este campo debe ser cero. |

#### Tabla de índice

La tabla de índice contiene varias entradas de 4 bytes, que indican la posición de cada bloque de datos, y una última entrada adicional que apunta al final del archivo.
El contenido de cada entrada es el siguiente:
| poco | Longitud | Máscara | Nombre | Propósito |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Posición | Este campo, cuando se desplaza a la izquierda por la alineación del índice dada en el encabezado, emite la posición donde comienza el bloque de datos. |
| 31 | 1 | 0x80000000 | Tipo de compresión | El formato ZSO tiene una semántica similar, solo que 0 representa LZ4 en lugar de Deflate. En el formato "v2". Se considera implícitamente que el bloque no está comprimido si el tamaño del bloque es igual o mayor que el tamaño del bloque especificado en el encabezado del archivo. |

#### Bloques de datos

Los bloques de datos se componen de datos comprimidos o sin comprimir. El tamaño de un bloque se calcula obteniendo su posición y luego restándola de la posición del siguiente bloque. Si la alineación del índice es mayor que cero, es probable que el tamaño del bloque sea mayor que los datos que contiene.


## Referencias

* N/A

