---
date: 2020-08-12
keywords: bpg, .bpg, formato de archivo bpg, cómo abrir archivos bpg, extensión .bpg, extensión bpg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo BPG
linktitle: BPG
description: "Obtenga información sobre el formato de archivo BPG y las API que pueden crear y abrir archivos BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## ¿Qué es un archivo BPG? ##

BPG (Better Portable Graphics) es un formato de archivo creado por Fabrice Bellard en 2014 para imágenes digitales. Propuso BPG como reemplazo de JPEG, ya que BPG era más eficiente en compresión o tamaño. BPG utiliza la codificación intra-frame del estándar de compresión de video HEVC (High-Efficiency Video Coding).

BPG está diseñado como un formato portátil de memoria eficiente para trabajar en dispositivos portátiles y de IoT. Actualmente, los navegadores web no admiten el formato BPG, pero los sitios web aún pueden entregar imágenes BPG mediante el uso de una biblioteca JavaScript escrita por Bellard. BPG utiliza el perfil de imagen fija principal 4:4:4 16 de HEVC hasta 14 bits por muestra.

## Especificaciones ##

El formato de contenedor BPG es un formato de imagen genérico en lugar del flujo de bits sin procesar que se usa en HEVC. BPG admite formatos de color 4:4:4, 4:2:2 y 4:2:0. El canal alfa también es compatible con un canal adicional codificado por separado o el cuarto canal de imagen CMYK. BPG proporciona soporte de metadatos para Exif, perfiles ICC y XMP. BPG admite YCbCr (ITU-R BT.601, BT.709 y BT.2020 (luminancia no constante)), YCgCo, RGB, CMYK y espacio de color en escala de grises. BGP también admite animación y compresión de datos HEVC con pérdida y sin pérdida.

## Referencias ##

- [Mejores gráficos portátiles - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

