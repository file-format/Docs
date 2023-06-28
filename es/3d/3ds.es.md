{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","archivo", "formato", "tipo de archivo", "extensión","¿qué es un archivo 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo 3DS y las API que pueden abrir y crear archivos 3DS",
  "title" :"Formato de archivo 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es el archivo 3DS?

Un archivo con la extensión .3ds representa el formato de archivo de malla 3D Sudio (DOS) utilizado por Autodesk 3D Studio. Autodesk 3D Studio ha estado en el mercado de formatos de archivo 3D desde la década de 1990 y ahora ha evolucionado a 3D Studio MAX para trabajar con modelado, animación y renderizado 3D. Un archivo 3DS contiene datos para la representación 3D de escenas e imágenes y es uno de los formatos de archivo populares para la importación y exportación de datos 3D. Considera información como ubicaciones de cámaras, datos de malla, información de iluminación, configuraciones de ventanas gráficas, datos de grupos de suavizado, referencias de mapas de bits y atributos para crear vértices y polígonos para renderizar una escena.

## Formato de archivo 3DS - Más información
Básicamente, 3DS es un formato de archivo binario y sigue una estructura predefinida para almacenar y recuperar datos. El formato de archivo binario permite que el formato de archivo 3DS sea más rápido y más pequeño en comparación con los formatos de archivo basados en texto. Los datos dentro de un archivo 3DS se almacenan en forma de fragmentos.

### Fragmento de 3DS

Cada parte de un archivo 3DS es un bloque de datos que contiene una identificación, la longitud del bloque para la ubicación del siguiente bloque y los datos en sí. El ID de fragmento permite a los lectores de formato de archivo 3DS omitir los bloques que no reconocen. También ayuda en la extensibilidad del formato. Cada fragmento almacena información relacionada con las formas, la iluminación y la información de visualización que, en conjunto, representan la escena. Los fragmentos se organizan en una estructura jerárquica en un archivo 3DS y se asemejan a un árbol de objetos de documento XML en la representación.

**ID de fragmento:** Los primeros dos bytes de un fragmento representan un identificador de fragmento que le permite al lector de archivos decidir si considerarlo durante la lectura u omitirlo.

**Longitud del fragmento:** El ID del fragmento va seguido de un número entero de 4 bytes (en little-endian) que representa la longitud del fragmento. Esta longitud también incluye la longitud de los datos, la longitud de sus subbloques y el encabezado de 6 bytes.

**Carga útil:** La longitud del fragmento va seguida de bytes reales de datos para el fragmento, seguidos de sus subfragmentos en la misma estructura jerárquica que se puede extender a varios niveles de profundidad.

### Estructura de un trozo

La estructura jerárquica de un trozo simple es como se muestra a continuación:

**Un trozo**

|inicio|final|tamaño|nombre
--- | --- | --- | ---
|0|1|2|ID de fragmento
|2|5|4|Siguiente trozo

Los trozos tienen una jerarquía impuesta sobre ellos que se identifica por su ID. Un archivo 3ds tiene el ID de fragmento principal 4D4Dh. Esta es siempre la primera parte del archivo. En el fragmento primario están los fragmentos principales.

**Trozos principales**

|id|Descripción
--- | ---
|3D3D|Inicio de datos de malla de objetos.
|B000|Inicio de los datos del fotograma clave.

El puntero de Siguiente fragmento después del bloque de ID apunta al siguiente fragmento principal.
Directamente después de un trozo principal hay otro trozo. Este podría ser cualquier otro tipo de fragmento permitido dentro de su ámbito principal de fragmentos.
Para la descripción de malla (3D3D) podrían ser múltiplos de.

**Subfragmentos de 3D3D - Bloque de malla**


|id|Descripción
--- | ---
|1100|desconocido
|1200|Color de fondo.
|1201|desconocido
|1300|desconocido
|1400|desconocido
|1420|desconocido
|1450|desconocido
|1500|desconocido
|2100|Bloque de color ambiental
|2200|niebla?
|2201|niebla?
|2210|niebla?
|2300|desconocido
|3000|desconocido
|4000|Bloque de objetos
|7001|desconocido
|AFFF|desconocido

**Subfragmentos de 4000 - Bloque de descripción de objeto**
El primer elemento de Subchunk 4000 es una cadena ASCIIZ del nombre de los objetos.
Recuerda que un objeto puede ser una malla, una luz o una cámara.

|id|Descripción
--- | ---
|4010|desconocido
|4012|sombra?
|4100|Objeto de polígono triangular
|4600|Luz
|4700|Cámara

## Referencias

* [Formatos de archivo de geometría - Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)
* [3DS - Por Wikipedia](https://en.wikipedia.org/wiki/.3ds)
