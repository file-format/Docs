{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","qué es un archivo ac","cómo abrir un archivo c", "extensión", "archivo", "archivo c","formato de archivo c", "extensión de archivo c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - Archivo de programación de lenguaje C",
  "description":"Obtenga información sobre el formato de archivo C y las API que pueden crear y abrir archivos C",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## ¿Qué es un archivo C?

Un archivo guardado con la extensión de archivo c es un archivo de código fuente escrito en lenguaje de programación C. El archivo **C** incluye toda la implementación de la funcionalidad de la aplicación en forma de código fuente. La declaración del código fuente se escribe en los archivos de encabezado que se guardan con la extensión [.h](/es/programación/h/). C++ es la forma moderna del lenguaje C y se utiliza para desarrollar la mayor parte del software en la actualidad.

## Breve historia

El lenguaje C surgió como resultado de la creación de diferentes utilidades para el sistema operativo UNIX. Denis Ritchie, el hombre detrás de la creación de este lenguaje de programación, el trabajo comenzó originalmente en la década de 1960 y principios de la de 1970.

## Formato de archivo C

Los archivos C se escriben en formato de archivo de texto sin formato siguiendo la sintaxis del lenguaje de programación. Un archivo C típico tendrá:

* declaración de importación en la parte superior del archivo para importar cualquier archivo de encabezado
* uno o más métodos para implementar la funcionalidad deseada

### Importación de encabezados

Los archivos de encabezado, con la extensión .h, contienen las declaraciones de inclusión necesarias para incluir otros archivos de funcionalidad en el proyecto. Además, estos contienen las declaraciones de métodos definidos en el archivo de implementación. Los archivos de encabezado se incluyen mediante la declaración de inclusión como se muestra a continuación.

```
#include <filename.h>
```

### Implementación del código fuente

La implementación real de los requisitos funcionales se codifica como métodos en el archivo C. Cada método en un archivo C tiene un tipo de devolución, un nombre de método y puede tener algunos parámetros de entrada. Si el tipo de devolución no es nulo, es posible que el método devuelva algún valor.

### Ejemplo de código C
Aquí está el programa de ejemplo ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referencias** ##

* [Implementación de clase: por Wikipedia] (https://en.wikipedia.org/wiki/Class_implementation_file)

