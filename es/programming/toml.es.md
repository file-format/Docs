---
date: 2019-10-11
keywords: toml, .toml, formato de archivo toml, cómo abrir archivos toml, extensión .toml, extensión toml
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo TOML
linktitle: TOML
description: "Obtenga información sobre el formato de archivo TOML y las API que pueden crear y abrir archivos TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## ¿Qué es un archivo TOML? ##

TOML (Tom's Obvious Minimal Language) es un formato de archivo de configuración mínimo que utiliza la extensión .toml. TOML tiene como objetivo ser fácil de leer, mapear sin ambigüedades a los diccionarios y ser fácil de analizar en diferentes estructuras de datos. TOML tiene una especificación de código abierto que recibió contribuciones de la comunidad. TOML es compatible con muchos lenguajes de programación como C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. El tipo MIME para archivos TOML es *application/toml*.


## Formato de archivo TOML ##

Los archivos TOML consisten principalmente en pares clave/valor, secciones/tablas, comentarios y deben ser un documento Unicode codificado en UTF-8 válido. TOML admite los tipos de datos String, Integer, Float, Boolean, Datetime, Array y Table (hash table/dictionary). TOML es un lenguaje que distingue entre mayúsculas y minúsculas.

### Sintaxis ###

- **Pares clave-valor**: los pares clave-valor están separados por el signo igual (=). Cada par debe estar en una nueva línea.

```toml
primero = "Tom"
último = "Preston-Werner"
```

- **Comentarios**: los comentarios comienzan con el símbolo de almohadilla (#).

```toml
# Este es un documento TOML.
```

- **Cadenas**: las cadenas están entre comillas (").

```toml
cadena = "Cadena de ejemplo"
```

- **Cadenas de varias líneas**: las cadenas de varias líneas están rodeadas por tres comillas (""").

```toml
[direccion de casa]
calle = """123 Callejón Tornado
Conjunto 16"""
ciudad = "Este de Centerville"
estado = "KS"
```

- **Enteros/Flotantes**

```toml
entero = 20
flotar = 20.5
```

- **Booleanos**: Los booleanos siempre están en minúsculas.

```toml
bool1 = verdadero
bool2 = falso
```

- **Date-Time**: para DateTime, puede usar una fecha y hora con formato RFC 3339 como se muestra en el siguiente ejemplo.

```toml
offset_date_time = 1979-05-27 07:32:00Z
hora_fecha_local = 1979-05-27T07:32:00
fecha_local = 1979-05-27
hora_local = 07:32:00
```

- **Arreglos**: Los arreglos están rodeados por corchetes con elementos separados por comas (,).

```toml
colores = [ "rojo", "amarillo", "verde" ]
```

- **Tablas**: las tablas son colecciones de pares clave/valor que se definen mediante encabezados en una nueva línea rodeada de corchetes ([]). La tabla finaliza cuando se proporciona un nuevo encabezado o cuando finaliza el archivo.

```toml
[direccion de casa]
calle = """123 Callejón Tornado
Conjunto 16"""
ciudad = "Este de Centerville"
estado = "KS"

[Dirección de la oficina]
calle = """123 Callejón Tornado
Conjunto 16"""
ciudad = "Este de Centerville"
estado = "KS"
```

Las tablas en línea están rodeadas por llaves ({}) con cada par clave/valor separado por una coma (,).

```toml
nombre = { primero = "Tom", último = "Pitt" }
```

## Referencias ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

