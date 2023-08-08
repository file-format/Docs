---
date: 2019-10-11
keywords: java, .java, formato de archivo java, cómo abrir archivos java, cómo ejecutar archivos java, archivo java, código de muestra java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo Java
linktitle: Java
description: "Obtenga información sobre el formato de archivo Java y las API que pueden crear y abrir archivos Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## ¿Qué es un archivo Java? ##
Un archivo que contiene el código fuente de Java y se guarda con la extensión de archivo .java se conoce como archivo Java. Java es una de las tecnologías más utilizadas para el desarrollo de juegos, aplicaciones móviles, web y de escritorio. Dado que Java es independiente de la plataforma, funciona perfectamente en Windows, Mac, Linux, Raspberry Pi, etc. Java es muy similar a C# y C++, por lo que es más fácil cambiar entre estos lenguajes.

## Breve historia ##

El proyecto Java fue iniciado en junio de 1991 por James Gosling, Mike Sheridan y Patrick Naughton. Java se llamó inicialmente Oak. Más tarde pasó a llamarse Green y finalmente a Java. James Gosling diseñó Java con una sintaxis similar a C/C++. La primera versión pública de Java fue lanzada en 1996 por Sun Microsystems. Podría ejecutarse en todos los sistemas populares que hicieron que Java se hiciera popular rápidamente. Con el lanzamiento de Java 2 en diciembre de 1998, se crearon múltiples configuraciones para diferentes tipos de plataformas. Las versiones fueron las siguientes

- J2EE (Java EE): Para soluciones empresariales
- J2ME (Java ME): Para aplicaciones móviles
- J2SE (Java SE): Para aplicaciones de escritorio

El 19 de noviembre de 2006, Sun lanzó Java Virtual Machine (JVM) como software gratuito y de código abierto. Después de que Oracle Corporation adquiriera Sun Microsystems en 2009-2010, James Gosling renunció a Oracle el 2 de abril de 2010.

## Cómo ejecutar/ejecutar código Java ##

Para ejecutar el código Java, primero debe compilarse. Para eso, se requiere el SDK de Java. El SDK de Java compila el código Java en un archivo de clase de código de bytes. Hay IDE como Eclipse e IntelliJ Idea que facilitan el trabajo con archivos Java al proporcionar finalización de código y una interfaz fácil de usar para compilar y ejecutar el código Java.

## Formato de archivo Java ##

La sintaxis de Java estuvo muy influenciada por C y C++ pero, a diferencia de C++, Java se creó casi exclusivamente como un lenguaje orientado a objetos. En Java, todo el código está escrito dentro de clases y cada elemento de datos es un objeto. A diferencia de C++, Java no admite la sobrecarga de operadores ni la herencia múltiple.

### Código de muestra de Java ###

El siguiente es un ejemplo de sintaxis de Java.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
En el código anterior, la palabra clave **public** denota el modificador de acceso. Establece que esta clase puede ser accedida por las clases fuera de la jerarquía de clases. El modificador de acceso también puede ser **protegido** (se puede acceder en el mismo paquete) o **privado** (solo la misma clase puede acceder a los métodos). El **estático** delante del método indica que el método se puede invocar sin una instancia específica de la clase. El **vacío** indica que el método no devolvería nada. Para imprimir la cadena en la consola. Se utiliza el comando System.out.println. En este comando, la clase *System* tiene un campo estático *out* que es una instancia de la clase *PrintStream* que contiene el método *println*.

El nombre de archivo de los archivos Java debe ser el mismo que el nombre de la clase. Entonces, el archivo Java para el código de ejemplo se llamaría *ExampleApp.java*.

## Referencias ##

- [Java (lenguaje de programación) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

