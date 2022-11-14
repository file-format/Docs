---
date: 2019-10-11
keywords: py, python, .py, formato de archivo py, cómo abrir un archivo py, cómo ejecutar archivos py, cómo ejecutar archivos python, cómo ejecutar python
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo PY
linktitle: PY
description: "Obtenga información sobre el formato de archivo PY y las API que pueden crear y abrir archivos PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## ¿Qué es un archivo PY? ##

Los archivos con la extensión .py contienen el código fuente de Python. El lenguaje Python se ha convertido en un lenguaje muy famoso hoy en día. Se puede utilizar para secuencias de comandos del sistema, desarrollo web y de software y matemáticas. Python admite la compatibilidad entre plataformas; significa que las aplicaciones desarrolladas en Python pueden funcionar en diferentes plataformas como Windows, MAC, Linux, Raspberry Pi, etc. Python proporciona una sintaxis simple y fácil de leer que es similar al idioma inglés. Los desarrolladores pueden escribir una aplicación de software razonable escribiendo unas pocas líneas de código Python. Dado que Python se ejecuta en un sistema de interpretación, el código se puede ejecutar tan pronto como se escribe, lo que lo hace muy bueno para la creación de prototipos.

## Breve historia ##

Python fue concebido a fines de la década de 1980 por Guido van Rossum como sucesor del lenguaje de programación ABC. Su implementación comenzó en diciembre de 1989 con Van Rossum como único desarrollador principal. Trabajó en Python hasta el 12 de julio de 2018. En enero de 2019, los desarrolladores principales activos de Python eligieron un "Consejo Directivo" de cinco miembros compuesto por Nick Coghlan, Brett Cannon, Carol Willing, Barry Varsovia y Van Rossum para dirigir el proyecto.

### Versiones ###

- Python 2.0 se lanzó el 16 de octubre de 2000.
- Python 3.0 se lanzó el 3 de diciembre de 2008.

## Cómo ejecutar el archivo py ##

Para verificar la versión de Python instalada, puede usar el siguiente comando:

```cmd
python --version
```

Esto generará la versión en la consola como

```cmd
Python 3.7.4
```

Si Python no está instalado en su máquina, puede ir a [python.org](https://www.python.org/) y descargar e instalar Python para su sistema operativo correspondiente.

Para ejecutar un script de Python, puede usar el siguiente comando:

```cmd
python helloworld.py
```

*helloworld.py* es un archivo de script que contiene el siguiente código

```py
print("Hello World from Python")
```

Esto imprimirá lo siguiente en la ventana de la consola.

```cmd
Hello World from Python
```

Nota: si usa IDE, proporcionan botones en la pantalla o diferentes métodos abreviados de teclado para ejecutar Python. Por ejemplo, se muestra un botón de reproducción en el canalón con el editor en PyCharm que le permite ejecutar el script de Python.

## Formato de archivo PY ##

Python fue diseñado para facilitar la lectura y tiene similitudes con el inglés y las matemáticas. Python usa líneas nuevas para indicar el comando completo en lugar de puntos y comas o paréntesis que se usan en otros idiomas. Para ámbitos, bucles y funciones, Python se basa en la sangría y los espacios en blanco en lugar de las llaves que se usan en otros idiomas.

### Sintaxis ###

El siguiente es un ejemplo de la sintaxis de Python.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Referencias ##

- [Python (lenguaje de programación) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

