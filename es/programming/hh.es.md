{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","qué es un archivo .hh","cómo abrir un archivo .hh", "extensión", "archivo", "archivo .hh","formato de archivo .hh", " extensión de archivo .hh",".Ejemplo de archivo HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Formato de archivo de encabezado C++",
  "description":"Obtenga información sobre el formato de archivo HH y las API que pueden crear y abrir un archivo HH",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## ¿Qué es un archivo HH?

Un archivo con extensión .hh es un archivo de encabezado de C++ que incluye la declaración de variables, constantes y funciones. Estas declaraciones son utilizadas por los archivos de implementación de C++ correspondientes, generalmente guardados como archivos [.cpp](/es/programming/cpp/) que contienen la implementación real de la lógica del usuario. Se hace referencia a los archivos de encabezado .hh en los archivos CPP de implementación mediante la directiva `#include`. Puede agregar tantos archivos de encabezado como sea posible a su proyecto de C++ para incluir declaraciones de nivel de proyecto.

## Formato de archivo .HH

Un archivo .hh es un archivo de texto sin formato que se crea teniendo en cuenta las reglas de definición del archivo de encabezado. La información más común declarada en un archivo .hh incluye lo siguiente.

**`Variables`**: en el caso de la programación orientada a objetos (OOP), un archivo de encabezado de clase contiene definiciones de todas las variables de nivel de clase a las que se puede acceder a través de los archivos de código fuente de implementación.
**`Declaración de métodos`**: todas las declaraciones de métodos se incluyen en los archivos de encabezado .h para que sean accesibles a través de múltiples archivos de implementación.
**`Definiciones de funciones no en línea`**: los archivos de encabezado también pueden contener definiciones de métodos no en línea.
**`Mapas de mensajes`**: un archivo de encabezado también puede contener mapas de mensajes en el caso de una implementación de código fuente de MFC. En tal caso, los mapas de mensajes están vinculados a la implementación de la funcionalidad, que está vinculada a elementos de la interfaz de usuario, como botones, casillas de verificación, botones de opción, etc.

## Diferencia entre archivos .H y .HH

Aparentemente, no existe tal diferencia entre los archivos de encabezado .h y .hh aparte de la forma recomendada de usarlos para los respectivos idiomas, es decir, [C](/es/programación/c/) o C++. Nombrar sus archivos de encabezado de acuerdo con estos lenguajes lo ayuda a distinguirlos en un proyecto grande que puede ser una combinación de implementaciones de C y C++.

Además, si los encabezados están separados por extensión, su editor puede aplicar el formato adecuado automáticamente para cada uno.

En general, la diferenciación de estos dos formatos de archivo no hará ningún daño, pero será ventajoso, y se recomienda seguir para la distinción entre C y C++.

### Protectores de cabecera

Los archivos de encabezado pueden generar errores complejos cuando se incluyen varias declaraciones en el mismo archivo como resultado de agregar otros archivos de encabezado. Estas definiciones duplicadas generan errores del compilador. Esta situación problemática se puede evitar a través de un mecanismo llamado protección de encabezado que son directivas de compilación condicional como se muestra a continuación.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Con este encabezado, el preprocesador verifica si `ANY_UNIQUE_NAME_HERE_HPP` ya ha sido definido. Si el encabezado se incluye repetidamente en el mismo archivo, se ignorará el contenido del encabezado.

## Referencias

* [Archivadores de encabezado: Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Diferencia entre los formatos de archivo .h y .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

