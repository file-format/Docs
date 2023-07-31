{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","qué es un archivo ah","cómo abrir un archivo h", "extensión", "archivo", "archivo h","formato de archivo h", "extensión de archivo h", "Ejemplo de archivo H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Formato de archivo de encabezado C/C++",
  "description":"Obtenga información sobre el formato de archivo H y las API que pueden crear y abrir un archivo H",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## ¿Qué es un archivo H?

Un archivo guardado con **extensión de archivo h** es un archivo de encabezado que se usa en archivos C/C++ para incluir la declaración de variables, constantes y funciones. Estos son referidos por los archivos de implementación [C++](/es/programming/cpp/) que contienen la implementación real de estas funciones. Un archivo de encabezado .h también puede incluir información adicional, como definiciones de macro. Se hace referencia a estos archivos de encabezado en los archivos C/C++ mediante la directiva `#include`.

Un nuevo proyecto de C++ generalmente contiene un archivo de encabezado especial con el nombre de archivo **stdafx.h** que es el punto de partida para todas las cadenas de compilación y todos los archivos de encabezado se pueden incluir en este único archivo. Un archivo .h se puede abrir con cualquier editor de texto, Eclipse IDE, Microsoft Visual Studio IDE, el compilador Borland C++ y muchas otras aplicaciones.

## Formato de archivo .H

Un archivo .h es un archivo de texto sin formato que tiene sus propias reglas para definir la sintaxis. Los archivos de encabezado pueden contener la siguiente información.

**`Variables`**: en el caso de la programación orientada a objetos (OOP), un archivo de encabezado de clase contiene definiciones de todas las variables de nivel de clase a las que se puede acceder a través de los archivos de código fuente de implementación.
**`Declaración de métodos`**: todas las declaraciones de métodos se incluyen en los archivos de encabezado .h para que sean accesibles a través de múltiples archivos de implementación.
**`Definiciones de funciones no en línea`**: los archivos de encabezado también pueden contener definiciones de métodos no en línea.
**`Mapas de mensajes`**: un archivo de encabezado también puede contener mapas de mensajes en el caso de una implementación de código fuente de MFC. En tal caso, los mapas de mensajes están vinculados a la implementación de la funcionalidad, que está vinculada a elementos de la interfaz de usuario, como botones, casillas de verificación, botones de opción, etc.


### Protectores de cabecera

Los archivos de encabezado pueden generar errores complejos cuando se incluyen varias declaraciones en el mismo archivo como resultado de agregar otros archivos de encabezado. Estas definiciones duplicadas generan errores del compilador. Esta situación problemática se puede evitar a través de un mecanismo llamado protección de encabezado que son directivas de compilación condicional como se muestra a continuación.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Con este encabezado, el preprocesador verifica si `ANY_UNIQUE_NAME_HERE` ya ha sido definido. Si el encabezado se incluye repetidamente en el mismo archivo, se ignorará el contenido del encabezado.

## Ejemplo de archivo H

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## Referencias

* [Archivadores de encabezado: Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

