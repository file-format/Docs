{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "archivo", "extensión", "formato de archivo", "C++", "Lenguaje de programación" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - Archivo de código fuente de C++",
  "description":"Obtenga información sobre el formato de archivo CPP y las API que pueden crear y abrir archivos CPP",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo C++?

Los archivos con la extensión de archivo CPP son archivos de código fuente para aplicaciones escritas en el lenguaje de programación C++. Un solo proyecto de C++ puede contener más de un archivo CPP como código fuente de la aplicación. Dicho proyecto consta de diferentes tipos de archivos, de los cuales los archivos CPP se conocen como archivos de implementación, ya que contienen todas las definiciones de los métodos declarados en el archivo de encabezado (.h). El proyecto C++ como un todo da como resultado una aplicación ejecutable cuando se compila como un todo.

## Estructura del archivo CPP

La estructura de un archivo CPP es simple en comparación con los archivos de encabezado. El objetivo principal de dicho archivo de implementación es separar la interfaz de la implementación. Esto da como resultado declaraciones de todas las funciones miembro en un archivo de encabezado y sus detalles dentro del archivo CPP. Un archivo de implementación de CPP se puede usar como un archivo simple para escribir una aplicación o como una implementación de clase.

### Implementación independiente

Un archivo CPP, cuando se usa como una aplicación independiente, puede contener todas las implementaciones dentro de él sin el requisito de declaración de métodos en el archivo de encabezado. Dicha implementación consta de todos los métodos definidos en el archivo de implementación donde la entrada de la aplicación se rige por un método principal que toma la entrada opcional del usuario como argumentos. También puede incluir cualquier biblioteca de la biblioteca estándar de C++ para ser utilizada por cualquier método declarado en el archivo.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Implementación de clases

En la programación orientada a objetos (POO), se utiliza un archivo CPP como definición de clase. En tal caso, todos los miembros de datos de clase y funciones miembro se declaran dentro del archivo de encabezado. Cada archivo de encabezado, a su vez, también puede hacer referencia a métodos de biblioteca estándar. El archivo CPP de definición de clase se refiere al archivo de encabezado en una declaración de inclusión al comienzo del archivo. En su mayoría, los desarrolladores de software incluyen comentarios al comienzo de un archivo de implementación de clase que proporciona información sobre el contenido real del archivo, los detalles del autor y la fecha de implementación. En tales casos, los archivos de implementación de encabezado deben tener los mismos nombres. Un ejemplo de un archivo de encabezado e implementación de este tipo es el siguiente.

### Archivo de cabecera

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### Archivo de implementación de CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referencias

* [Implementación de clase: por Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

