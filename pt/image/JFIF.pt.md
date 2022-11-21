---
date: 2020-08-12
keywords: jfif, .jfif, formato de arquivo jfif, como abrir arquivos jfif, extensão .jfif, extensão jfif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Arquivo JFIF - O que é um arquivo .jfif?
linktitle: JFIF
description: "Saiba mais sobre o formato de arquivo JFIF e APIs que podem criar e abrir arquivos JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## O que é um arquivo JFIF?

JFIF (JPEG File Interchange Format (JFIF)) é um arquivo de formato de imagem que usa a extensão .jfif. JFIF é construído sobre JIF (JPEG Interchange Format) reduzindo a complexidade e resolvendo suas limitações.

## Breve História do JFIF

O desenvolvimento do documento JFIF foi liderado por Eric Hamilton e um acordo sobre a primeira versão foi estabelecido no final de 1991. A versão 1.02 foi publicada em 7 de setembro de 1992. A RFC 2046 especificou que o formato JFIF é usado para transmitir imagens JPEG pela Internet. JFIF foi publicado pela ECMA em 2009 e foi padronizado pela ITU-T em 2011 como sua Recomendação T.871 e pela ISO/IEC em 2013 como ISO/IEC 10918-5

## Formato de arquivo JFIF ##

Um arquivo JFIF consiste em uma sequência de marcadores conforme definido na parte 1 do JPEG Standard. Cada marcador consiste em dois bytes (FF seguido por um byte que especifica o tipo de marcador). Os marcadores podem ser autônomos ou indicar o início de um segmento de marcador.

O JFIF permite que vários componentes como Y, Cb, Cr tenham resoluções diferentes, mas seu alinhamento não é definido. Ao contrário do JPEG, o JFIF pode fornecer informações de resolução e proporção. JFIF também define o modelo de cores a ser utilizado.

### Estrutura do arquivo ##

|Segmento|Código|Descrição|
|---|---|---|
|SOI|FF D8|Início da Imagem|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|segmentos de marcadores adicionais|
|SOS|FF DA|Início da varredura|
||dados da imagem compactada||
|EOI|FF D9|Fim da imagem|

O Padrão JFIF define os seguintes segmentos:

### Segmento do marcador JFIF APP0 ###

É um segmento obrigatório que contém parâmetros de imagem. Ele também pode conter uma miniatura não compactada incorporada.

|Campo|Tamanho (bytes)|Descrição|
|---|---|---|
|Marcador APP0|2|FF E0|
|Comprimento|2|Comprimento do segmento excluindo o marcador APP0|
|Identificador|5|JFIF (4A 46 49 46 00) em ASCII terminado por um byte nulo|
|Versão JFIF|2|Versão do JFIF|
|Unidades de densidade|1|Unidade para os seguintes campos de densidade de pixels</br> 00 : Sem unidades; largura: a proporção de pixel de altura é igual a Ydensidade:Xdensidade</br> 01 : Pixels por polegada</br> 02 : Pixels por centímetro|
|Xdensity|2|Densidade horizontal de pixels maior que zero|
|Ydensidade|2|Densidade vertical de pixels maior que zero|
|Xthumbnail|1|Contagem horizontal de pixels da miniatura RGB incorporada. Pode ser zero|
|Ythumbnail|1|Contagem vertical de pixels da miniatura RGB incorporada. Pode ser zero|
|Dados de miniatura|3 × n|Dados de miniatura de raster RGB de 24 bits não compactados|

### Extensão JFIF segmento de marcador APP0 ###

Esta é uma seção opcional que, se definida, deve seguir imediatamente o segmento do marcador JFIF APP0. Esta seção é suportada pelo JFIF versão 1.02 e superior e permite a incorporação de miniaturas em três formatos diferentes.

|Campo|Tamanho (bytes)|Descrição|
|---|---|---|
|Marcador APP0|2|FF E0|
|Comprimento|2|Comprimento do segmento excluindo o marcador APP0|
|Identificador|5|JFXX (4A 46 58 58 00) em ASCII terminado por um byte nulo|
|Formato da miniatura|1|Especifica qual formato de dados é usado para a seguinte miniatura incorporada:</br> 10: formato JPEG</br> 11 : 1 byte por pixel formato paletizado</br> 13 : 3 bytes por pixel Formato RGB|
|Dados de miniatura|variável||

## Conversão de JFIF para outros formatos de arquivo de imagem

JFIF pode ser convertido em formatos de arquivo de imagem populares, como [PNG](/pt/image/png/), [JPG](/pt/image/jpg/) e [PDF](/pt/pdf/).

## Referências ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

