{
  "date" : "2021-09-08",
  "keywords" :[ "archivo rel", "formato de archivo rel", "qué es un archivo rel", "archivo", "ejemplo rel", "extensión de archivo rel","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo REL y las API que pueden crear y abrir archivos REL",
  "title" :"REL - Archivo de módulo reubicable",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ¿Qué es un archivo REL?
Un archivo con extensión .rel se puede utilizar para varios tipos de propósitos. Por lo tanto, en términos de clasificación de juegos, se conoce como un archivo de módulo reubicable utilizado por algunos juegos de Nintendo Wii, como Brawl, Super Smash Bros y Mario Kart Wii. Comprende los datos del juego, incluidos los modelos de personajes y las etapas. Los archivos REL funcionan de manera similar a los archivos .DLL utilizados por Microsoft Windows.

## formato de archivo REL
En un formato de archivo REL, el archivo se divide en varias secciones, agrupadas por acceso similar, por ejemplo, datos de solo lectura en una sección, todo el código ejecutable se coloca en otra, etc. El archivo comienza con una sección de encabezado, seguida de:
- Tabla que contiene la información de la sección.
- Los datos de la sección.
- Información de reubicación.

### Encabezado del archivo
El archivo comienza con un encabezado de hasta 0x4C bytes:
| Compensación | Tamaño | Nombre de campo | Descripción |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | identificación | Número de identificación arbitrario. Debe ser único entre todos los NIR utilizados por un juego. No debe ser 0. |
| 0x04 | 4 | siguiente | Puntero al siguiente módulo, rellenado en tiempo de ejecución. |
| 0x08 | 4 | anterior | Puntero al módulo anterior, rellenado en tiempo de ejecución. |
| 0x0c | 4 | númSecciones | Número de secciones en el archivo. |
| 0x10 | 4 | secciónInfoOffset | Desplazamiento al inicio de la tabla de sección. |
| 0x14 | 4 | nombreOffset | Desplazamiento a cadena ASCII que contiene el nombre del módulo. Puede ser NULL. Relativo al inicio del archivo REL. |
| 0x18 | 4 | nombreTamaño | Tamaño del nombre del módulo en bytes. |
| 0x1c | 4 | versión | Número de versión del formato de archivo REL. |
| 0x20 | 4 | bssTamaño | Tamaño de la sección '.bss'. |
| 0x24 | 4 | relOffset | Desplazamiento a la tabla de reubicación. |
| 0x28 | 4 | impOffset | Desplazamiento a la tabla imp. |
| 0x2c | 4 | tamañoimp | Tamaño de la tabla imp en bytes. |
| 0x30 | 1 | prologSection | Índice en la tabla de sección a la que se refiere el prólogo. Omitir si este campo es 0. |
| 0x31 | 1 | epilogSection | Índice en la tabla de sección a la que se refiere el epílogo. Omitir si este campo es 0. |
| 0x32 | 1 | sección no resuelta | Índice en la tabla de la sección con la que no resuelto es relativo. Omitir si este campo es 0. |
| 0x33 | 1 | bssSección | Índice en la tabla de sección a la que se refiere bss. Lleno en tiempo de ejecución! |
| 0x34 | 4 | prólogo | Desplazamiento en la sección especificada de la función _prolog. |
| 0x38 | 4 | epílogo | Desplazamiento en la sección especificada de la función _epilog. |
| 0x3c | 4 | sin resolver | Compensación en la sección especificada de la función _unresolved. |
| 0x40 | 4 | alinear | Solo versión ≥ 2. Restricción de alineación en todas las secciones, expresada como potencia de 2. |
| 0x44 | 4 | bssAlinear | Solo versión ≥ 2. Restricción de alineación en toda la sección '.bss', expresada como potencia de 2. |
| 0x48 | 4 | arreglarTamaño | Solo versión ≥ 3. Si REL está vinculado con OSLinkFixed (en lugar de OSLink), el espacio después de esta dirección se puede usar para otros fines (como BSS). |

### Tabla de información de la sección
La tabla de información de la sección contiene entradas **numSections** cada una de 0x8 bytes de largo:
| Compensación | Tamaño | Descripción |
-------|------------|-------------|
| 0x0 | 30 bits | Desplazamiento desde el comienzo del REL hasta la sección. Si es cero, la sección es una sección no inicializada (es decir, .bss). |
| 0x3.6 | 1 bit | Desconocido. |
| 0x3.7 | 1 bit | Bandera ejecutable; si es 1, la sección es ejecutable. |
| 0x4 | 4 | Longitud en bytes de la sección. Si es cero, esta entrada se omite. |
| 0x8 | Siguiente entrada | Siguiente entrada |

### Datos de reubicación
Los datos de reubicación son una o más listas de estructuras de 0x8 bytes. El final de cada lista está marcado por el código de tipo especial 203:
| Compensación | Nombre | Tamaño | Descripción |
-------|------------|------------|-----|
| 0x0 | compensación | 2 | Compensación en bytes desde la reubicación anterior a esta. Si esta es la primera reubicación en la sección, esto es relativo al inicio de la sección. |
| 0x2 | tipo | 1 | El tipo de traslado. Descrito abajo. |
| 0x3 | sección | 1 | La sección del símbolo contra la que se va a reubicar. Para el tipo de reubicación especial 202, este es en cambio el número de la sección en este archivo a la que se aplican las siguientes entradas de reubicación. |
| 0x4 | sumando | 4 | Desplazamiento en bytes del símbolo contra el que se va a reubicar, en relación con el inicio de su sección. Esta es una dirección absoluta en lugar de reubicaciones contra main.dol. |
| 0x8 | Siguiente entrada | Siguiente entrada | Siguiente entrada |


 




## Referencias


* [Formato de módulo de objeto reubicable](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


