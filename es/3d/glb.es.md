{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","archivo", "formato", "tipo de archivo", "extensión","¿qué es un archivo GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Obtenga información sobre el formato de archivo GLB y las API que pueden abrir y crear archivos GLB",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## ¿Qué es un archivo GLB?

GLB es la representación en formato de archivo binario de modelos 3D guardados en el formato de transmisión GL ([glTF](/es/3d/gltf/)). Información sobre modelos 3D como jerarquía de nodos, cámaras, materiales, animaciones y mallas en formato binario. Este formato binario almacena el recurso glTF (JSON, .bin e imágenes) en un blob binario. También evita el problema del aumento del tamaño del archivo que ocurre en el caso de glTF. El formato de archivo GLB da como resultado tamaños de archivo compactos, carga rápida, representación de escena 3D completa y extensibilidad para un mayor desarrollo. El formato usa model/gltf-binary como tipo MIME.

## Formato de archivo GLB - Más información

Los métodos de entrega de contenido utilizados por glTF dan como resultado un procesamiento adicional para decodificar los datos binarios codificados en base 64 y también aumentan el tamaño del archivo en un 33 %. Estos métodos de entrega, que contribuyeron a la formación del formato de archivo GLB, incluyen:

* glTF JSON apunta a datos binarios externos (geometría, fotogramas clave, máscaras) e imágenes.
* glTF JSON incorpora datos binarios codificados en base64 e imágenes en línea utilizando URI de datos.

GLB como formato de contenedor se introdujo como formato de archivo binario para la representación de activos glTF en un blob binario para evitar los problemas causados por glTF. Se debe consultar el formato de archivo GLB [especificaciones] (https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) para cualquier implementación de lector/escritor del mismo para el desarrollo de aplicaciones .

## Estructura del archivo GLB

El formato de archivo GLB se basa en little endian y su estructura muestra que contiene:

* Un preámbulo de 12 bytes, titulado encabezado.
* Uno o más fragmentos que contienen contenido JSON y datos binarios.

#### Encabezado GLB

El encabezado del formato de archivo GLB consta de tres entradas de 4 bytes:

* magia uint32 - magia es igual a 0x46546C67. Es una cadena ASCII glTF y se puede usar para identificar datos como binarios glTF
* Versión uint32: indica la versión del formato del contenedor binario glTF
* longitud uin32: la longitud total del glTF binario, incluido el encabezado y todos los fragmentos en bytes

#### Trozos

Cada fragmento en un archivo GLB tiene la siguiente estructura:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - longitud de chunkData en bytes
* `chunkType` - indica indica el tipo de fragmento
* `chunkData` - carga útil binaria de fragmento

donde los tipos de trozos son:

|# |Tipo de fragmento|ASCII|Descripción|Ocurrencias
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Contenido JSON estructurado|1
|2.|0x004E4942|BIN|Búfer binario|0 o 1

El inicio y el final de cada fragmento deben alinearse con un límite de 4 bytes y se debe usar el relleno para este propósito.

##### Contenido JSON estructurado

Esta debería ser la primera porción del activo glTF binario y permite que la implementación recupere progresivamente los recursos de las porciones posteriores. Esto también brinda la capacidad de leer solo un subconjunto seleccionado de recursos de un activo glTF binario, como el LOD más grueso de una malla. Para cumplir con los requisitos de alineación, este fragmento debe rellenarse con caracteres espaciales finales (0x20).

##### Búfer binario #####

Este fragmento contiene la carga útil binaria para geometría, fotogramas clave de animación, máscaras e imágenes. Debe ser el segundo fragmento del activo glTF binario y debe completarse con ceros finales (0x00) para satisfacer los requisitos de alineación.

## Referencias ##

* [Especificaciones del formato de archivo GLB - Khronos](/es/3D/GLTF/)

