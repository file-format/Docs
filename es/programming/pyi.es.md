---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato de archivo PYI - Definición de interfaz de Python
linktitle: PYI
description: "Obtenga información sobre el formato de archivo PYI y las API que pueden crear y abrir archivos PYI."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## ¿Qué es un archivo PYI?

Un archivo PYI es un archivo de definición de interfaz de Python que contiene una referencia de código auxiliar para la implementación de la interfaz. Cada módulo de Python se representa como un código auxiliar .pyi, que es un archivo de Python normal pero con métodos vacíos. La sintaxis de los archivos PYI es la misma que la de un módulo normal de Python. La implementación de los métodos vacíos se deja para que el usuario final logre el objetivo específico para el cual se escribió el módulo. Ahí es donde los archivos PYI son diferentes a los archivos [PY](/es/programming/py/) que contienen la implementación completa del programa. Los archivos PYI se pueden abrir con editores de texto como Notepad, Notepad++, Microsoft Visual Studio Code y JetBrains PyCharm.

## Formato de archivo PYI

Los archivos PYI se guardan como archivos de texto sin formato que se pueden abrir con cualquier editor de texto. Python es un lenguaje de interpretación que realiza la verificación de tipos cuando se ejecuta el código. En tal caso, los archivos PYI son beneficiosos en la forma en que los desarrolladores pueden definir y verificar manualmente los tipos de un módulo mientras escriben la aplicación.

## Referencias ##

* [Interfaces - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [Intérpretes de PYM](https://github.com/interpreters/pym)

