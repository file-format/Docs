---
date: 2022-01-31
keywords: stp, .stp, formato de archivo stp, cómo abrir archivos stp, extensión .stp, extensión stp
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato de archivo STP
linktitle: STP
description: "Obtenga información sobre el formato de archivo STP y las API que pueden crear y abrir archivos STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## ¿Qué es un archivo STP?

Un archivo STP es un archivo CAD 3D que se utiliza para el intercambio de datos de productos entre aplicaciones CAD y CAM. Contiene información sobre objetos 3D y se guarda de forma similar al formato de archivo **STEP**. Los archivos STP facilitan el intercambio de datos entre aplicaciones según los protocolos de aplicación [STEP](/es/3d/step/) ISO 10303-2xx. Esta ISO define el mecanismo de codificación para la representación de datos en el lenguaje de modelado de datos EXPRESS. Los archivos STP se pueden abrir en aplicaciones como **Autodesk Fusion 360**.

## Formato de archivo STP - Más información

Los archivos STP se guardan en el disco en formato de archivo ASCII simple. Estos contienen información de modelos 3D como texto sin formato que las aplicaciones CAD/CAM pueden leer para cargar estos modelos.

Los archivos STP también se guardan con la extensión .step y consisten en una secuencia de registros. Las características más destacadas de estos archivos incluyen:

* El conjunto de caracteres se define como puntos de código de ISO 10646.
* "ISO-10303-21;" son los primeros caracteres del primer registro.
* Los comentarios están rodeados por los caracteres "/*" y "*/".
* El último registro contiene "END-ISO-10303-21;" si el archivo STEP se ajusta a la versión 2002.
* En caso de que se ajuste a la versión 2016, puede haber una o más firmas digitales después de "END-ISO-10303-21"; terminador
* Los saltos de línea se indican con "\N\" y los saltos de página se indican con "\F\".

## Abrir archivos STP

Los archivos STP se pueden abrir en los visores STP y en los editores de texto.

### Abrir archivos STP con visores STP

Varias aplicaciones CAD pueden abrir archivos STP para verlos en Windows, MacOS y Linux. Éstos incluyen:

* Autodesk Fusion 360 (multiplataforma)
* FreeCAD (multiplataforma)
*IMSI TurboCAD (Windows, Mac)
* Sistemas Dassault CATIA (Windows, Linux)

### Abrir archivos STP con editores de texto

Los archivos STP se guardan como archivos de texto sin formato. Esto hace posible abrir archivos STP con editores de texto. Los editores de texto populares, como Notepad y Notepad ++ en el sistema operativo Windows, y Apple TextEdit en MacOS pueden abrir archivos STP. Una vez abierto en un editor de texto, el usuario puede editar las propiedades del archivo STP. Sin embargo, puede provocar la corrupción del archivo en caso de actualizar las propiedades incorrectamente.

## Cómo convertir archivos STP

Hay varias aplicaciones que pueden convertir archivos STP a otros formatos de archivo. Las aplicaciones CAD que pueden convertir archivos STP incluyen:

* Autodesk Fusión 360
*IMSI TurboCAD
* Borde sólido de Siemens

Además de estos, hay varias aplicaciones en línea que pueden convertir archivos STP a otros formatos de archivo. Estas aplicaciones en línea le permiten cargar su archivo STP en servidores en la nube donde se convierten al formato deseado y se devuelven para su descarga.

Autodesk Fusion 360 puede convertir archivos STP a los siguientes formatos de archivo 3D y CAD.

* [OBJ](/es/3d/obj/)
* [3MF](/es/3d/3mf/)
* [DWG](/es/cad/dwg/)
* [DXF](/es/cad/dxf/)
* [ASM](/es/cad/asm/)
* [IGES](/es/cad/iges/)
* [STL](/es/cad/stl/)
* [FBX](/es/3d/fbx/)
* F3D
* [USD](/es/3d/usd/)

## Referencias

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

