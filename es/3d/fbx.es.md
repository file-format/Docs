{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "archivo", "extensión", "formato", "Formato de archivo 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tu guía de formato de archivo para saber qué es un archivo FBX y las API que puedes crear y abrir",
  "title" :"FBX - Formato de archivo FilmBox 3D",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo FBX?

FBX, FilmBox, es un popular formato de archivo 3D desarrollado originalmente por Kaydara para MotionBuilder. Fue adquirido por Autodesk Inc en 2006 y ahora es uno de los principales formatos de intercambio 3D que utilizan muchas herramientas 3D. FBX está disponible en formato de archivo binario y ASCII. El formato se estableció para brindar interoperabilidad entre las aplicaciones de creación de contenido digital. Hay muchas herramientas disponibles para la conversión desde/hacia el formato de archivo FBX.

## Formato de archivo FBX: más información

FBX es un formato propietario y las especificaciones sobre su formato de archivo binario no están disponibles oficialmente. Autodesk proporciona un C++ FBX SDK para leer, escribir y convertir a/desde un archivo FBX. Un script de importación y exportación de Python para FBX también está disponible en el software Blender que no usa el SDK de FBX.

### Estructura de archivos basada en texto

La estructura de archivos basada en texto es una estructura de árbol documentada con identificadores claramente nombrados. Consiste en una lista anidada de nodos dispuestos en jerarquía donde cada nodo tiene:

* Un identificador de tipo de nodo (nombre de clase)
* Una tupla de propiedades asociadas con él, los elementos de la tupla son los tipos de datos primitivos habituales: ##float, integer, string## etc.
* Una lista que contiene nodos en el mismo formato (recursivamente).

Estos pueden representarse lógicamente de la siguiente manera:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Algunos de los nodos estándar se definen como una lista implícita en la que cada elemento consta de una lista anidada. Cualquier aplicación que tenga la intención de acceder a la geometría FBX tiene que analizar estos contenidos y darle un significado útil. Un ejemplo de archivo FBX basado en texto es el siguiente:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Estructura de archivos binarios de archivos FBX

Como se indicó anteriormente, las especificaciones de formato de archivo FBX no están disponibles públicamente para FBX. Dado que Blender Foundation implementa el formato de archivo FBX sin utilizar el SDK proporcionado por la empresa, algunos de los detalles sobre el formato de archivo binario están [disponibles] (https://code.blender.org/2013/08/fbx-binary-file-format -especificación/) como parte de su implementación.

La estructura de los archivos binarios sigue el siguiente orden:

* Encabezado
* Registro de objetos
* Pie de página

### Encabezado FBX

La información del encabezado del archivo se compone de 27 bytes.

* Bytes 0 - 20: Kaydara FBX Binary \x00 (archivo mágico, con 2 espacios al final, luego un terminador NULL).
* Bytes 21 - 22: [0x1A, 0x00]## (desconocido pero todos los archivos observados muestran estos bytes).
* Bytes 23 - 26: int sin firmar, el número de versión. 7300 para la versión 7.3 por ejemplo.

### Registro de objetos ###

El encabezado va seguido de un registro de objeto que es un registro de nodo completo con un nombre vacío y una lista de propiedades vacía. Contiene recursivamente toda la formación del archivo.

### Pie de página ###

La sección FBX Footer se encuentra al final del archivo cuyo contenido se desconoce.

## Formatos de registro ##

Los registros en un archivo FBX se clasifican como:

* Registros de nodos
* Registros de propiedad

### Formato de registro de nodo ###

Cada formato de registro de nodo tiene un nombre y tiene el siguiente diseño de memoria.


|Tamaño (Bytes)|Tipo de fecha|Nombre
--- | ---|---|
|4|UInt32|Desplazamiento final
|4|UInt32|NúmPropiedades
|4|UInt32|PropertyList
|1|UInt8|LongNombre
|NombreLongitud|carácter|Nombre
|?|?|Propiedad[n], donde n = 0:PropertyListLen
|Opcional| |
|?|?|Lista anidada
|13|uint8[]|Registro nulo

dónde:

* `EndOffset` es la distancia desde el comienzo del archivo hasta el final del registro del nodo (es decir, el primer byte de lo que viene después). Esto se puede usar para omitir fácilmente registros desconocidos o no requeridos.
* `NumProperties` es el número de propiedades en la tupla de valor asociada con el nodo. Una lista anidada como último elemento no se cuenta como propiedad.
* `PropertyListLen` es la longitud de la lista de propiedades. Este es el tamaño necesario para almacenar propiedades ##NumProperties##, que depende del tipo de datos de las propiedades.
* `NameLen` es la longitud del nombre del objeto, en caracteres. El único caso en el que esto es 0 parece ser el nivel superior de las listas.
* `Nombre` es el nombre del objeto. No hay terminación cero.
* `Property[n]` es la n-ésima propiedad. Para el formato, vea la sección propiedad Formato de registro. Las propiedades se escriben secuencialmente y sin relleno.
* `NestedList` es la lista anidada, cuya presencia se indica mediante un registro NULL al final.

La existencia de una entrada de lista anidada se puede determinar comprobando si quedan bytes hasta que se alcanza EndOffset. Si es así, el siguiente registro de objeto debe leerse directamente después de la última propiedad. El registro del objeto luego sigue 13 cero bytes, que luego se combinan con EndOffset. El propósito o requisito de la entrada NULL no se conoce y puede apuntar a alguna función de formato.

### Formato de registro de propiedad ###

Un registro de propiedad contiene detalles sobre las propiedades que forman parte de Node. Un registro de propiedad tiene el siguiente diseño de memoria:


|Tamaño (Bytes)|Tipo de datos|Nombre
--- | --- | ---
|1|char|TipoCódigo
|?|?|Datos

TypeCode representa códigos de caracteres que se ordenan en grupos que requieren un manejo similar. TypeCodes se puede clasificar en los siguientes tipos y TypeCode puede ser uno de los códigos de caracteres entre estos tipos.

#### Tipos primitivos ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Los datos en el registro de tipo escalar primitivo son exactamente la representación binaria del valor, en orden de bytes little-endian.

#### Tipos de matrices ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Los datos para el tipo de matriz son más complejos y tienen la siguiente estructura.


|Tamaño (Bytes)|Tipo de datos|Nombre
--- | --- | ---
|4|Uint32|Longitud de matriz
|4|Uint32|Codificación
|4|Uint32|LongitudComprimida
|?|?|Contenidos

### Tipos especiales ###

Los siguientes son los TypeCodes de tipos especiales.

```
S: String
R: raw binary data
```

Ambos códigos de tipo se representan de la siguiente manera:


|Tamaño (Bytes)|Tipo de datos|Nombre
--- | --- | ---
|4|Uin32|Longitud
|Longitud| |

La cadena no termina en cero y puede contener caracteres \0 (esto se usa en algunas propiedades de FBX).

## Referencias ##

* [FBX: el SDK de Autodesk] (http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [Especificaciones del formato de archivo binario FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

