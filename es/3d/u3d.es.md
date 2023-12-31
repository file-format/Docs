{
  "date" : "2019-10-11",
  "keywords" :[ "archivo u3d", "formato de archivo u3d", "qué es un archivo u3d", "archivo", "ejemplo u3d", "extensión de archivo u3d","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Formato de archivo 3D universal",
  "description":"Obtenga información sobre el formato de archivo U3D y las API que pueden abrir y crear archivos U3D",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo U3D?

**U3D** (Universal 3D) es un formato de archivo comprimido y una estructura de datos para gráficos 3D por computadora. Contiene información del modelo 3D, como mallas triangulares, iluminación, sombreado, datos de movimiento, líneas y puntos con color y estructura. El formato fue aceptado como estándar [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) en agosto de 2005. Los documentos 3D [PDF](/es/pdf/) son compatibles con U3D incrustación de objetos y se puede ver en Adobe Reader (versión 7 y posteriores).

El formato U3D se desarrolló teniendo en cuenta el objetivo de establecer un estándar universal para el almacenamiento e intercambio de datos tridimensionales. Sin embargo, el formato encuentra su uso principal en la codificación de PDF 3D en lugar de ser utilizado como un formato de intercambio. Acrobat 3D convierte un tipo de archivo 3D compatible a U3D o PRC al convertirlo a PDF.

## Formato de archivo U3D

Los archivos U3D están en formato de archivo binario que se sometió a cuatro ediciones como se describe en el documento de referencia ECMA-363, lo que resultó en una actualización de las especificaciones con cada edición. El estándar de archivo PDF ISO-32000 acepta U3D como tipo de anotación y multimedia permitido.

La primera edición de U3D se centró en las representaciones clave de las propiedades de los gráficos 3D, como la geometría, el color, las texturas, la iluminación, los huesos y la animación basada en la transformación. Las ediciones segunda y tercera corrigieron algunas erratas en la primera edición, siendo la tercera versión el tipo más utilizado en el software de la industria. La cuarta edición proporciona definiciones para primitivas de orden superior (superficies curvas). Especificaciones U3D están disponibles en línea para referencia del usuario en el sitio web de ECMA.

### Tipos de datos en archivos U3D

El archivo binario contendrá los siguientes tipos: U8, U16, U32, U64, I16, I32, F32, F64 y String.

* U8 : Un entero de 8 bits sin signo
* U16 : Un entero de 16 bits sin signo
* U32 : Un entero de 32 bits sin signo
* U64 : Un entero de 64 bits sin signo
* I16 : Un entero de 16 bits con signo
* F32: Un flotador de precisión simple IEEE.
* F64: Un flotador de doble precisión IEEE.
* Cadena: las cadenas en un archivo U3D comienzan con un número entero de 16 bits sin signo que define la longitud total de los caracteres en la cadena. Las cadenas siempre se procesan con distinción entre mayúsculas y minúsculas.

## Estructura de archivo U3D

Un archivo U3D contiene una secuencia de bloques. Hay 3 tipos diferentes de bloque en cada archivo U3D.

* Bloque de encabezado de archivo
* Bloque de declaración
* Bloque de continuación

El cargador determina el final de un bloque si los datos de ese bloque no son necesarios o si no hay disponible un decodificador para ese tipo de bloque.

{{< figure src="../u3d.png" alt="Formato de archivo U3D" >}}

### Bloque de encabezado de archivo
Un bloque de encabezado de archivo contiene información de archivo que utiliza el cargado para determinar cómo leer el archivo.

### Bloque de declaración

Los bloques de declaración contienen información sobre los objetos del archivo. Los objetos en un bloque de declaración deben definirse.

### Bloque de continuación

La información adicional para los objetos declarados en un bloque de declaración se proporciona en el bloque de continuación. Cada bloque de continuación debe estar asociado con un bloque de declaración.


## Referencias ##

* [Formato de archivo U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Especificaciones de formato de archivo ECMA U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)