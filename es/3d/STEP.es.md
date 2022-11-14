---
date: 2019-10-11
keywords: paso, .paso, formato de archivo paso, cómo abrir archivos paso, extensión .paso, extensión paso
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo PASO
linktitle: STEP
description: "Obtenga información sobre el formato de archivo STEP y las API que pueden crear y abrir archivos STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## ¿Qué es un archivo STEP?

El archivo STEP es un formato de intercambio de datos ampliamente utilizado para el diseño asistido por computadora (CAD). Fue estandarizado en 1994 por el comité ISO bajo el nombre de "ISO 10303-21". ISO 10303-21 define el mecanismo de codificación para representar datos en el lenguaje de modelado de datos EXPRESS. Un archivo STEP también se conoce como archivo p21 y archivo físico STEP. Las extensiones de archivo utilizadas para el archivo STEP son .stp y .step.

## Historia básica

En 1994, se emitió la especificación original de la Parte 21. Tiene algunos errores que fueron corregidos por el corrigendum técnico emitido en 1996. La segunda edición se publicó en 2002 que incluía el corrigendum y extensiones para varias secciones de datos. La tercera edición se publicó en 2016 y agregó secciones de anclaje y referencia que permitieron almacenar entidades y valores en archivos externos. Se agregó soporte UTF-8 de cadenas. Se agregaron firmas digitales para verificar el contenido del archivo y validar las credenciales. También se agregó el soporte para comprimir y almacenar la estructura de intercambio usando ZIP.

## Formato de archivo PASO

El formato de texto sin formato para un archivo STEP consta de una secuencia de registros. El conjunto de caracteres se define como puntos de código de ISO 10646. "ISO-10303-21;" son los primeros caracteres del primer registro. Los comentarios están rodeados por los caracteres "/*" y "*/". El último registro contiene "END-ISO-10303-21;" si el archivo STEP se ajusta a la versión 2002. En caso de que se ajuste a la versión 2016, puede haber una o más firmas digitales después de "END-ISO-10303-21"; terminador Los saltos de línea se indican con "\N\" y los saltos de página se indican con "\F\".

El archivo STEP está dividido en secciones y sus nombres son términos reservados. Todas las secciones terminan con el registro "ENDSEC" y deben estar en el orden que se muestra a continuación.

- **HEADER**: Esta es una sección obligatoria y no repetible. Está formado por las siguientes entidades:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Es una sección opcional no repetitiva que se introdujo en la versión 2016. Define los nombres externos de las instancias para que puedan ser referenciados.
- **REFERENCIA**: Es una sección opcional no repetitiva que también se introdujo en la versión 2016. Cada entrada en esta sección asocia un nombre de instancia de entrada/valor a una instancia/valor en un archivo externo.
- **DATOS**: es una sección repetible opcional que contiene el contenido principal de la instancia del modelo.
- **FIRMA**: Es una sección repetible opcional que se introdujo en la versión 2016. Posee la firma digital para verificar el contenido del archivo o para validar las credenciales.

## Referencias

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

