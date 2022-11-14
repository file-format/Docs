---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato de archivo PYD - Módulo dinámico de Python
linktitle: PYD
description: "Obtenga información sobre el formato de archivo PYD y las API que pueden crear y abrir archivos PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## ¿Qué es un archivo PYD?

Un archivo PYD es una biblioteca de enlaces dinámicos escrita en Python que puede ser ejecutada por otro código de Python en tiempo de ejecución. Contiene uno o más módulos de Python que facilitan la reutilización del código y proporcionan una arquitectura de módulos para escribir aplicaciones. Los archivos PYD se pueden crear y guardar con la extensión .pyd, por ejemplo, helloworld.pyd. Los desarrolladores de aplicaciones pueden usar la declaración de importación para incluir los módulos PYD en sus aplicaciones. Los archivos PYD se pueden abrir con Python Software Foundation Python que está disponible para Windows, Mac y Linux OS.

## Formato de archivo PYD - Más información

Los archivos PYD están escritos en el lenguaje de programación Python y se generan al compilar el código de Python.

## Diferencia entre los formatos de archivo PY y PYD

Un archivo [PY](/es/programming/py/) contiene código fuente que se ejecuta tal cual y no se puede incluir como código reutilizable en otras aplicaciones de Python. Sin embargo, un archivo PYD es una biblioteca vinculada dinámicamente para ser utilizada en el sistema operativo Windows.

## ¿Cómo crear un archivo PYD?

Se puede crear un archivo PYD creando un módulo con un nombre, por ejemplo, exmaple.pyd. Este módulo contendrá toda la funcionalidad en forma de una o más funciones, por ejemplo, PyMod_example(). Cuando el programa incluye esta biblioteca y la llama, se puede hacer importando el módulo y se ejecutará la función PyMod_example().

## Referencias ##

* [Creación de extensiones de Python en C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (lenguaje de programación) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

