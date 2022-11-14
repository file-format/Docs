---
date: 2019-10-11
keywords: prc, .prc, formato de archivo prc, cómo abrir archivos prc, extensión .prc, extensión prc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo PRC
linktitle: PRC
description: "Obtenga información sobre el formato de archivo PRC y las API que pueden crear y abrir archivos PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Los formatos de archivo PRC
Las extensiones ".prc" se utilizan para el formato de archivo 3D compacto de representación de productos y un formato de archivo de libro electrónico de MobiPocket.

## ¿Qué es un archivo de Compacto de Representación de Producto (PRC)?

PRC (Product Representation Compact) es un formato de archivo 3D que está optimizado para almacenar, cargar y mostrar datos 3D, especialmente provenientes de sistemas CAD (diseño asistido por computadora). Es un archivo binario secuencial, escrito de forma portátil. PRC se puede utilizar para incrustar datos 3D en un archivo PDF. PRC es compatible con la mayoría de las construcciones principales de CAD, como ensamblajes y piezas, árboles de entidades 3D, representación de geometría exacta, representación triangulada y marcado. PRC usa la extensión .prc y el tipo de medio de Internet que se usa es *model/prc*.

PRC es un formato de archivo multipropósito que, según su uso, puede almacenarse con una compresión normal para representar directamente los datos CAD o almacenarse con una compresión alta para reducir el tamaño del archivo. Los datos 3D almacenados en un PDF con formato PRC son interoperables con las aplicaciones CAM y CAE.

### Especificación de formato de archivo de representación de producto compacto (PRC)

Un archivo PRC tiene una sección de encabezado principal seguida de una o más estructuras de archivo seguidas de un archivo de modelo al final. Una estructura de archivo tiene un encabezado seguido de las siguientes secciones de datos:

- **Globals**: contiene las estructuras y colores de archivos a los que se hace referencia, estilos de línea y sistemas de coordenadas para cada entidad de árbol de la estructura de archivos.
- **Árbol**: contiene una descripción del árbol de elementos como ocurrencias de productos, definiciones de piezas, elementos de representación y marcado.
- **Teselado**: Contiene todos los datos teselados (triangulados) en las entidades hoja del árbol (elementos de representación y marcas).
- **Geometría**: Contiene todos los datos exactos de geometría y topología de las entidades hoja del árbol (elementos de representación).
- **Geometría extra**: Contiene los datos resumen de la geometría. Esto permite que el archivo se cargue parcialmente sin cargar toda la geometría.

La siguiente es la estructura de un archivo PRC típico.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## ¿Qué es un archivo de libro electrónico MobiPocket con extensión PRC?
Un formato de archivo de libro electrónico introducido por una empresa francesa llamada **Mobipocket** también utiliza la extensión ".prc". Inicialmente, Mobipocket lanzó una aplicación gratuita para múltiples dispositivos inteligentes como tabletas, PDA y teléfonos inteligentes. La extensión ".prc" es en realidad idéntica a .mobi pero se usa particularmente para PDA que solo admiten extensiones **.prc** o **.pdb**.

### Especificaciones de formato de archivo Mobipocket PRC
El formato de archivo MobiPocket PRC se basa en el estándar Open eBook usando XHTML y también puede incluir JavaScript y marcos. También está disponible el soporte para consultas SQL nativas que se utilizarán con bases de datos integradas.

Mobipocket Reader tiene una biblioteca de página de inicio. Los lectores pueden insertar páginas en blanco en cualquier parte de un libro y agregar dibujos variables. Los objetos como anotaciones, marcadores, correcciones, notas y dibujos se pueden administrar desde una sola ubicación. Las imágenes se convierten a formato GIF y tienen un tamaño máximo de 64K que es suficiente para teléfonos móviles con pantallas pequeñas. Mobipocket Reader tiene marcadores electrónicos y un diccionario incorporado.

El lector tiene un modo de pantalla completa para lectura y soporte para muchos PDA, comunicadores y teléfonos inteligentes. Los productos Mobipocket son compatibles con la mayoría de los sistemas operativos Palm, Windows, Symbian, BlackBerry, pero no con Android. El lector funciona bajo Linux o Mac OS X usando WINE.

## Referencias

- [RPC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Especificación de formato PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparación de formatos de libros electrónicos - Por Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

