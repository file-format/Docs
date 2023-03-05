---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "Formato de archivo PYM: archivo de preprocesador de macros PYM"
linktitle: PYM
description: "Obtenga información sobre el formato de archivo PYM y las API que pueden crear y abrir archivos PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## ¿Qué es un archivo PYM?

Un archivo PYM es un archivo de preprocesador de macros basado en el lenguaje de programación Python. Fue desarrollado por VRVis Research y almacena atajos de macros. Cuando el archivo PYM es interpretado por la etapa de preprocesamiento del intérprete de Python, estos accesos directos se expanden como reemplazos de su texto completo. Además, una tercera operación opcional que puede realizar un preprocesador de macros es la inclusión de archivos. Los archivos PYM se pueden abrir en editores de texto como Notepad, Notepad ++, Apple TextEdit y VI en Linux.

## Formato de archivo PYM

Los archivos PYM se guardan como archivos de texto sin formato en el disco. Un archivo PYM también puede incluir otros archivos usando la directiva `#include`.

### Sintaxis PYM

Las instrucciones PYM se incluyen entre los marcadores ""#begin python y "#end python", como se muestra a continuación.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Expansión de macros PYM

La macroexpansión PYM está representada por dos secuencias, es decir, <[ y ]>. Estas son etiquetas html especiales y pueden aparecer en cualquier lugar de una línea. Un pequeño ejemplo de PYM es el siguiente.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

El resultado de ejecutar esto a través de PYM es el siguiente:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referencias ##

* [PYM: un preprocesador de macros basado en Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Intérpretes de PYM](https://github.com/interpreters/pym)

