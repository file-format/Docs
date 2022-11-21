---
date: 2020-08-12
keywords: bpg, .bpg, formato de arquivo bpg, como abrir arquivos bpg, extensão .bpg, extensão bpg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo BPG
linktitle: BPG
description: "Saiba mais sobre o formato de arquivo BPG e as APIs que podem criar e abrir arquivos BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## O que é um arquivo BPG? ##

BPG (Better Portable Graphics) é um formato de arquivo criado por Fabrice Bellard em 2014 para imagens digitais. Ele propôs o BPG como substituto do JPEG, pois o BPG era mais eficiente em termos de compactação ou tamanho. O BPG usa a codificação intraquadro do padrão de compressão de vídeo HEVC (High-Efficiency Video Coding).

O BPG foi projetado como um formato portátil com eficiência de memória para funcionar em dispositivos portáteis e IoT. Atualmente, os navegadores da web não suportam o formato BPG, mas os sites ainda podem fornecer imagens BPG usando uma biblioteca JavaScript escrita por Bellard. O BPG usa o perfil Main 4:4:4 16 Still Picture do HEVC até 14 bits por amostra.

## Especificações ##

O formato de contêiner BPG é um formato de imagem genérico em vez do fluxo de bits bruto usado no HEVC. O BPG suporta os formatos de cor 4:4:4, 4:2:2 e 4:2:0. O canal alfa também é suportado com um canal extra codificado separadamente ou o quarto canal da imagem CMYK. O BPG fornece suporte a metadados para perfis Exif, ICC e XMP. O BPG suporta YCbCr (ITU-R BT.601, BT.709 e BT.2020 (luminância não constante)), YCgCo, RGB, CMYK e espaço de cores em tons de cinza. O BGP também suporta animação e compressão de dados HEVC com e sem perdas.

## Referências ##

- [Melhores gráficos portáteis - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

