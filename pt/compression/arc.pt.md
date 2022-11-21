---
date: 2019-12-09
keywords: arc, .arc, formato de arquivo arc, como abrir arquivos arc, extensão .arc, extensão arc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo ARC
linktitle: ARC
description: "Saiba mais sobre o formato de arquivo ARC e as APIs que podem criar e abrir arquivos ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## O que é um arquivo ARC?

ARC é um formato de arquivamento e compactação de dados sem perdas desenvolvido pela System Enhancement Associates (SEA). O formato do arquivo e o aplicativo que o cria são chamados de ARC. O ARC era muito popular durante os primeiros dias do BBS dial-up, pois combinava os recursos de compactação e arquivamento de vários arquivos no mesmo arquivo. ARC foi posteriormente substituído por [ZIP](/pt/compression/zip/) que oferecia melhores taxas de compressão.

A extensão de arquivo .arc é usada por vários outros tipos de arquivos não relacionados, como o formato ARC usado pelo Internet Archive para armazenar vários recursos da Web, um formato ARC diferente usado pelo arquivador FreeArc, um formato diferente usado pela Nintendo para recursos, etc. .

## Breve História do Formato de Arquivo ARC

O programa ARC foi escrito por Thom Henderson da System Enhancement Associates em 1985. Este programa agrupava arquivos em um único arquivo e também os compactava. Os arquivos gerados pelo programa ARC utilizavam a extensão .arc. A SEA lançou o código fonte do ARC em 1986 e o ARC foi portado para Unix e Atari ST por Howard Chu em 1987.

Phil Katz desenvolveu o PKARC e o PKXARC para arquivar e extrair arquivos. Os arquivos funcionavam com o formato de arquivo ARC e eram significativamente mais rápidos. Ao contrário do ARC, Katz dividiu as funções de compactação e arquivamento entre dois arquivos diferentes, o que reduziu o requisito de memória para executá-los.

Após a ação judicial entre SEA e Katz, a SEA retirou-se do mercado de shareware e desenvolveu o ARC+Plus com uma interface de usuário em tela cheia. O formato ARC não é mais comum no PC.

## Formato de arquivo ARC

O arquivo ARC consiste em uma sequência de cabeçalho de arquivo e arquivo seguido pelo marcador de fim de arquivo, conforme mostrado abaixo.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Cabeçalho do arquivo ARC ###

|Deslocamento|Etiqueta|Tipo|Valor|Descrição|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Método|
|02|ARCFNT|DS|12|nome do arquivo|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Tamanho compactado|
|13|ARCDAT|DW|0000|Data do arquivo (MSDOS)|
|15|ARCTIM|DW|0000|Tempo do arquivo (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Tamanho não comprimido|
|1D|ARCFIL|DS|ARCNSZ| |

### Métodos de compressão ###

O byte do método de compactação indica o método de compactação usado. A seguir estão os métodos de compactação usados para o arquivo ARC.

|Método|Nome|Descrição|
|---|---|---|
|0|Armazenado|Sem compressão usada|
|1|Embalado|Codificação de comprimento de execução repetida (RLE)|
|2|Comprimido|Codificação Huffman|
|3|Crunched|LZW com buffer de 4K, códigos de 12 bits|
|4|Crunchado|Primeiro empacotamento, depois buffer LZW 4K com 12 bits|
|5|Crunchado|Embalagem, LZW, buffer de 4K, comprimento variável (9-12 bits)|
|6|Squashed|LZW, buffer de 8K, comprimento variável (9-13 bits)|
|7|Esmagado|Embalagem, então buffer LZW 8K, 2-13 bits (PAK 1.0)|
|8|Distill|Huffman dinâmico com buffer de 8K (PAK 2.0)|

## Referências

- [ARC (formato de arquivo) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

