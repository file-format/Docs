{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Archivo de código fuente de Matlab",
  "description":"Obtenga más información sobre el archivo de código fuente Matlab .m y las API que pueden crear y abrir archivos MF",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Archivos de código fuente de Matlab

## ¿Qué es un archivo M (Matlab)?

Un archivo con extensión .m es un archivo de código fuente utilizado por Matlab, una plataforma de programación y computación numérica utilizada para análisis, desarrollo de algoritmos y modelado de simulación. Al igual que otros formatos de archivo de programación, un archivo M contiene código fuente que ejecuta comandos de Matlab para trazar gráficos, ejecutar simulaciones y otras operaciones matemáticas. Una sola simulación de Matlab puede abarcar varios archivos .m que pueden clasificar la aplicación en scripts, clases, funciones o declaraciones. Los archivos Matlab M se pueden abrir con cualquier editor de texto.

## Formato de archivo Matlab M - Más información

Los archivos Matlab .m son archivos de texto que contienen código de programación en el lenguaje de programación Matlab. Estos pueden abrirse y editarse en cualquier editor de texto y guardarse para ejecutarse en el software Matlab. Matlab en sí contiene un Live Editor que se usa para crear scripts que es una combinación de código, salida y texto formateado.

### Archivos de funciones de Matlab

Al igual que otros lenguajes de programación, puede crear un archivo .m que solo contenga la definición de una función que realiza solo una tarea específica. Dichos archivos también se guardan con la extensión .m e implementan la funcionalidad relacionada solo con esa función.

### Ejemplo de archivo .M

El siguiente es un ejemplo de archivo de función de Matlab que calcula el tiempo que tarda un objeto en caer desde la altura h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Para llamar a esta función desde el editor de Matlab o desde otro archivo .m, se puede usar el siguiente código.
```C++
TimeToGround(100)
```

## Referencias

* [Matlab - Formatos de archivo admitidos](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Usando Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Archivo de implementación de Objective-C

## ¿Qué es un archivo M (Objetivo-C)?

Un archivo M también se conoce como archivo de implementación que contiene el código fuente de una clase escrita en lenguaje Objective-C, un lenguaje de programación utilizado para escribir aplicaciones de software para OS X e iOS. Objective-C es el principal lenguaje de programación que utilizan las principales API de Apple, Cocoa y Cocoa Touch, para estas plataformas. Una sola aplicación de software desarrollada en este lenguaje puede contener múltiples archivos .m, que contienen la implementación de las clases del programa. Estos se pueden abrir con Apple XCode, jEdit y otros editores de texto comunes.

## Formato de archivo Objective-CM - Más información

Los archivos M están escritos en formato de texto sin formato utilizando la sintaxis de programación de Objective-C. Cada método de una clase debe estar definido con todo su código necesario en estos archivos de implementación. Estos archivos M de implementación pueden importar uno o más archivos de encabezado .h según los requisitos. La declaración de importación le dice al compilador dónde encontrar el archivo de encabezado que pertenece a este archivo de implementación. La declaración de importación está escrita de la siguiente manera.

```C++
#import "network.h"
```

Cada implementación de archivo M comienza con la directiva `@implementation`, seguida por el nombre del archivo de clase de implementación. Esto es seguido por la implementación de todos los métodos que se declaran en el archivo de encabezado.

### Ejemplo de formato de archivo M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Referencias
* [Acerca del Objetivo C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Guía de Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

