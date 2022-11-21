---
date: 2019-12-09
keywords: arj, .arj, formato de arquivo arj, como abrir arquivos arj, extensão .arj, extensão arj
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo ARJ
linktitle: ARJ
description: "Saiba mais sobre o formato de arquivo ARJ e as APIs que podem criar e abrir arquivos ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## O que é um arquivo ARJ? ##

ARJ (Arquivado por Robert Jung) é um arquivo compactado de alta eficiência desenvolvido por Robert K. Jung. O ARJ foi desenvolvido para DOS e versões anteriores do Windows no início dos anos 90. Os arquivos ARJ são úteis para fazer backup ou compartilhar um grande número de arquivos, pois você não precisa acompanhar todos esses arquivos e há apenas um único arquivo para manipular. A extensão .arj é usada para os arquivos ARJ.

## Formato de arquivo ARJ ##

Um arquivo ARJ contém dois tipos de cabeçalhos:

- Cabeçalho principal: Existe um cabeçalho principal no início do arquivo.
- Cabeçalhos locais: Os cabeçalhos locais estão presentes antes de cada arquivo.

|Deslocamento|Tipo|Contagem|Descrição|
|---|---|---|---|
|0000h|palavra|1|ID=0EA60h|
|0002h|palavra|1|tamanho básico do cabeçalho|
|0004h|byte|1|Tamanho do cabeçalho|
|0005h|byte|1|Número da versão do arquivador|
|0006h|byte|1|Número mínimo da versão necessária|
|0007h|byte|1|SO do host:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - Unix</br> 3 - AMIGO</br> 4 - MAC-OS (Sistema xx)</br> 5 - OS/2</br> 6 - MAÇÃ GS</br> 7 - ATARI ST</br> 8 - NeXT</br> 9 - VAX VMS|
|0008h|byte|1|Sinalizadores internos, bitmap:</br> 0 - sem senha / senha</br> 1 - reservado</br> 2 - o arquivo continua no próximo disco</br> 3 - o campo de posição inicial do arquivo está disponível</br> 4 - tradução de caminho ( "\" para "/" )|
|0009h|byte|1|Método de compactação:</br> 0 - armazenado</br> 1 - mais comprimido</br> 2 - comprimido</br> 3 - compactado mais rápido</br> 4 - compactado mais rápido|
|000Ah|byte|1|Tipo de arquivo:</br> 0 - binário</br> 1 - texto de 7 bits</br> 2 - cabeçalho do comentário</br> 3 - diretório</br> 4 - etiqueta do volume|
|000Bh|byte|1|reservado|
|000Ch|dword|1|Data/Hora do arquivo original no formato MS-DOS|
|0010h|dword|1|Tamanho do arquivo compactado|
|0014h|dword|1|Tamanho do arquivo original"|
|0018h|dword|1|CRC-32 do arquivo original|
|001Ah|word|1|Filespec position in filename|
|001Ch|word|1|Atributos do arquivo|
|001Eh|palavra|1|Dados do host|
|?|dword|1|Posição inicial do arquivo estendido|
|????h|dword|1|CRC-32 do cabeçalho básico|
|????h|palavra|1|Tamanho do primeiro cabeçalho estendido|
|????h+"SIZ"+2|dword|1|CRC-32 do cabeçalho estendido|
|????h+"SIZ"+6|byte|?|Arquivo compactado|

## Referências ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

