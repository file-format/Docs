---
date: 2019-10-11
keywords: dart, .dart, formato de archivo dart, archivo dart, cómo ejecutar archivos dart, extensión .dart
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo de dardo
linktitle: Dart
description: "Obtenga información sobre el formato de archivo Dart y las API que pueden crear y abrir archivos Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## ¿Qué es un archivo Dart? ##

Un archivo Dart contiene el código fuente del lenguaje de programación Dart, que es un lenguaje de programación optimizado para el cliente desarrollado por Google que se utiliza para crear aplicaciones para dispositivos móviles, de escritorio, web, IoT (Internet de las cosas), etc. Dart es un lenguaje orientado a objetos con una sintaxis similar a C. Dart se puede compilar en JavaScript o en código nativo. Puede ejecutar los archivos Dart en el famoso navegador web al igual que puede ejecutar un archivo javascript. Una herramienta de línea de comandos conocida como máquina virtual Dart que viene con Dart SDK también se usa para compilar y ejecutar los archivos Dart.

## Breve historia ##

El proyecto Dart fue fundado por Lars Bak y Kasper Lund y la primera versión se lanzó el 14 de noviembre de 2013. Al principio, Dart fue criticado por la fragmentación de la web debido a los planes para incluir una máquina virtual Dart en Google Chrome. Esos planes se abandonaron y Dart se centró en compilar en JavaScript con el lanzamiento de la versión 1.9 en 2015.

Dart 2.0 se lanzó en agosto de 2018 en el que se introdujo la extensión dart2native que compiló el código de Dart para plataformas nativas de Linux, Windows y macOS. Esta extensión habilitó ejecutables autónomos debido a que no se requería el SDK de Dart para ejecutar las aplicaciones de Dart en esas plataformas. Esta extensión también se integró con Flutter, lo que permite crear aplicaciones multiplataforma.

ECMA estandarizó Dart con la primera edición en julio de 2014 y la segunda edición en diciembre de 2014.


## Cómo ejecutar/ejecutar el código Dart ##

El código Dart puede ejecutarse de las siguientes maneras:

- **Compilado como JavaScript**:</br> El código Dart se compila en JavaScript mediante el compilador dart2js. El código JavaScript compilado es compatible con todos los principales navegadores web.
- **Ser único**:</br> El kit de desarrollo de software (SDK) de Dart se envía con una VM de Dart independiente que permite que el código de Dart se ejecute en la interfaz de línea de comandos. Dart se envía con una biblioteca estándar completa que permite a los usuarios escribir aplicaciones totalmente funcionales.
- **Recopilado antes de tiempo (AOT)**:</br> El código Dart se puede compilar AOT en un código de máquina que permite crear aplicaciones móviles con Flutter.
- **Nativo**:</br> Con el compilador dart2native, el código de Dart se puede compilar en ejecutables autónomos que se pueden ejecutar en Windows, Linux y macOS.

## Formato de archivo dardo ##

Dart es un lenguaje orientado a objetos de estilo C que admite interfaces, mixins, clases abstractas, genéricos cosificados e interfaz de tipos.

### Sintaxis ###

Los siguientes son algunos ejemplos de la sintaxis de Dart.

#### Imprimir en la consola ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Bucles y arreglos ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### Funciones ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Clases ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### Mezclas ####

Los mixins son clases normales de las que podemos tomar prestados métodos/variables sin heredarlas. Esto se hace usando la palabra clave *"with"*.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## Referencias ##

- [Dart (lenguaje de programación) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dardo](https://dart.dev/)

