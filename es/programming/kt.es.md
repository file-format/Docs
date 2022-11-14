---
date: 2019-10-11
keywords: kt, .kt, formato de archivo kotlin, cómo abrir archivos kotlin, cómo ejecutar archivos kotlin, formato de archivo .kt, archivo kt, extensión de archivo kotlin, extensión .kt, kotlin vs java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo KT
linktitle: KT
description: "Obtenga información sobre el formato de archivo KT y las API que pueden crear y abrir archivos KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## ¿Qué es un archivo KT? ##

Un código fuente escrito en Kotlin se guarda con la extensión .kt, comúnmente conocida como **extensión de archivo Kotlin**. Kotlin es un lenguaje de programación multiplataforma de propósito general desarrollado por JetBrains para ser totalmente interoperable con [Java](/es/programming/java/). La marca Kotlin está protegida por la Fundación Kotlin.

Kotlin fue anunciado como el lenguaje de programación preferido para el desarrollo de aplicaciones de Android por Google el 7 de mayo de 2019. Android Studio 3.0 comenzó a admitir Kotlin como una alternativa para el desarrollo de aplicaciones de Android en octubre de 2017.

## Breve historia del formato de archivo Kotlin KT##

Kotlin fue presentado por JetBrains en julio de 2011 como un nuevo lenguaje de programación para JVM. El líder de JetBrains, Dmitry Jemerov, dijo que a la mayoría de los lenguajes les faltaban las características que estaban buscando, excepto Scala, pero la lenta compilación de Scala era un inconveniente. Uno de los principales objetivos de Kotlin era compilar tan rápido como Java. El proyecto Kotlin fue de código abierto bajo la licencia Apache 2 en febrero de 2012.

La versión 1.0 de Kotlin se lanzó el 15 de febrero de 2015. Android anunció compatibilidad de primera clase para Kotlin en Android en Google I/O 2017. Kotlin 1.2 se lanzó el 28 de noviembre de 2017 con la capacidad de compartir código entre plataformas JVM y JavaScript. Kotlin 1.3 se lanzó el 29 de octubre de 2018 con soporte para programación asíncrona. Google anunció que Kotlin sería el lenguaje de programación preferido para el desarrollo de aplicaciones de Android el 7 de mayo de 2019. Kotlin 1.4 se lanzó en agosto de 2020 con algunos cambios leves para admitir la interoperabilidad con Swift/Objective-C.

## Sintaxis de Kotlin ##

Kotlin fue diseñado para ser mejor que Java pero aun así ser interoperable con el código Java para permitir la migración gradual de Java a Kotlin.

* Los puntos y comas son opcionales en Kotlin. Una nueva línea es suficiente para indicar el final de la declaración.
* Kotlin admite dos tipos de variables, de solo lectura, definidas por la palabra clave *val*, y mutables, definidas por la palabra clave *var*.
* Las clases son privadas y definitivas por defecto. Para derivar de una clase, la clase base debe declararse con la palabra clave *open*.
* Kotlin también es compatible con la programación de procedimientos.
* El punto de entrada al programa Kotlin es la función "principal" similar a Java, C#, etc.

### Ejemplo de sintaxis ###

El siguiente es un ejemplo de la sintaxis de Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

En el código anterior, la palabra clave **fun** define la función denominada main. Dentro de la función, se declara una variable de solo lectura 'audiencia' con la palabra clave **val**. Al usar el método **println**, "Hello World from Kotlin" se imprime en la consola. El valor de la variable audiencia se inyecta en la cadena con el signo **$**.

## Kotlin frente a Java
Kotlin es un lenguaje oficial para escribir aplicaciones de Android que ofrece muchas funciones avanzadas, pero muchos desarrolladores expertos de Java aún no muestran interés en cambiar a Kotlin. Piensan que pueden hacer todo solo con Java. La siguiente es la comparación entre dos tecnologías que pueden convencer a los desarrolladores de Java para que cambien:

| Parámetro | Java | Kotlin |
|--------------------------|---------------------------|---------------- -|
| Objetos Singleton | √ | √ |
| Tipos de comodines | √ | Χ |
| Compilación | Códigos de bytes | Máquina virtual |
| Expresión lambda | Χ | √ |
| Matriz invariante | Χ | √ |
| Campos no privados | √ | Χ |
| moldes inteligentes | Χ | √ |
| Seguridad nula | Χ | √ |
| Miembros estáticos | √ | Χ |

## Referencias ##

- [Kotlin (lenguaje de programación) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(lenguaje_de_programación))

