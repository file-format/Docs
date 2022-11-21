---
date: 2020-08-12
keywords: flif, .flif, formato de arquivo flif, como abrir arquivos flif, extensão .flif, extensão flif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo FLIF
linktitle: FLIF
description: "Saiba mais sobre o formato de arquivo FLIF e as APIs que podem criar e abrir arquivos FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## O que é um arquivo FLIF? ##

FLIF (Free Lossless Image Format) é um formato de imagem sem perdas que usa a extensão .flif para seus arquivos. A FLIF alega ter um desempenho superior ao [PNG](/pt/image/png/), [WebP](/pt/image/webp/) sem perdas, BPG sem perdas e JPEG 2000 sem perdas em termos de taxa de compactação. O FLIF usa entrelaçamento progressivo, pelo qual qualquer download parcial da imagem pode ser usado como uma codificação com perdas para a imagem inteira.

## Breve história ##

O FLIF foi anunciado em setembro de 2015 e a versão alfa foi lançada em outubro de 2015. Em setembro de 2016, a primeira versão estável do FLIF foi lançada.

## Projeto FLIF ##

O FLIF usa uma variante do CABAC (codificação aritmética binária adaptável ao contexto), MANIAC (Codificação aritmética de inteiro próximo a zero meta-adaptativo) para compactação. MANIAC é um algoritmo de codificação de entropia desenvolvido por Jon Sneyers e Pieter Wuille. No MANIAC, os contextos são nós de árvores de decisão que são aprendidas no momento da codificação dinamicamente. Isso torna o modelo de contexto mais específico da imagem e resulta em uma melhor compactação. O FLIF possui os seguintes recursos:

- Suporta compressão sem perdas
- Suporta compressão com perdas com pré-processamento do codificador
- Suporta escala de cinza, RGB e RGBA
- Suporta profundidade de cor de 1 a 16 bits por canal
- Suporta arquivos entrelaçados e não entrelaçados
- Suporta decodificação progressiva de arquivos parcialmente baixados
- Suporta animações
- Suporta perfis de cores ICC incorporados, metadados Exif e XMP
- Tem suporte limitado para compactar arquivos camera raw (RGGB)

## Formato de arquivo FLIF ##

Um arquivo FLIF tem as quatro partes a seguir:

## Cabeçalho principal ##

O cabeçalho principal contém os principais metadados, incluindo largura, altura, profundidade de cor, número de quadros.

|Tipo|Valor|Descrição|
|---|---|---|
|4 bytes|"FLIF"|Magia|
|4 bits|3 = ni ainda; 4 = eu ainda; 5 = ni anim; 6 = i anim|Entrelaçamento, animação|
|4 bits|1 = Escala de cinza; 3 = RGB; 4 = RGBA|Número de canais (nb_channels)|
|1 byte|'0','1','2' ('0'=custom)|Bytes por canal (Bpc)|
|variante|largura-1|Largura|
|variante|altura-1|Altura|
|varint|nb_frames-2 (somente se animação)|Número de quadros (nb_frames)|

## Partes de metadados ##

Esta parte contém metadados não-pixel como Exif/XMP, perfil de cores ICC, etc. que são codificados usando a compactação DEFLATE. Esses pedaços são definidos de forma semelhante aos pedaços PNG, com a diferença de que o tamanho do mandril é codificado com um número variável de bytes. Os nomes dos pedaços podem ter 4 letras (4 bytes) ou um valor abaixo de 32 indicando um pedaço não opcional.

O seguinte é um exemplo de mandris opcionais:

|Nome do bloco|Descrição|Conteúdo (após a descompressão DEFLATE)|
|---|---|---|
|iCCP|Perfil de cores ICC|dados brutos de perfil de cores ICC|
|eXif|Metadados Exif|cabeçalho "Exif\0\0" seguido por um cabeçalho TIFF e os dados EXIF|
|eXmp|Metadados XMP|XMP contido em um xpacket somente leitura sem preenchimento|

### Convenção de nomes ###

- **Primeira letra**: Maiúsculas são usadas para críticas e minúsculas são usadas para partes não críticas.
- **Segunda Letra**: Maiúsculas são usadas para públicos e minúsculas são usadas para blocos privados
- **Terceira Letra**: Maiúsculas são usadas para mandris que são necessários para exibir a imagem corretamente e minúsculas não são importantes para exibir a imagem.
- **Quarta Letra**: Maiúsculas são usadas para mandris que podem ser copiados cegamente com segurança. As letras minúsculas dependem dos dados da imagem.

## Segundo cabeçalho ##

Este contém as informações sobre a codificação real dos pixels.

|Tipo|Descrição|Condição|Valor Padrão|
|---|---|---|---|
|1 byte|NUL byte (0x00), nome do bloco de um fluxo de bits FLIF16||
|uni_int(1,16)|Bits por pixel dos canais|Bpc == '0': repeat(nb_channels)|8 se Bpc == '1', 16 se Bpc == '2'|
|uni_int(0,1)|Flag: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Número de loops|nb_frames > 1||
|uni_int(0,60_000)|Frame delay em ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Sinalizador: has_custom_cutoff_and_alpha|||
|uni_int(1.128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2.128)|alpha divisor|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Sinalizador: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|variável|Transformações (veja abaixo)|||
|uni_int(1) = 0|Bit indicador: feito com transformações|||
|uni_int(0,2)|Previsor de pixel invisível|alpha_zero && entrelaçado && intervalo alfa inclui zero||

**Canais**

|Número do canal|Descrição|
|---|----|
|0|Vermelho ou Cinza|
|1|Verde|
|2|Azul|
|3|Alfa|

**Transformações**

|Tipo|Descrição|
|---|---|
|uni_int(1) = 1|Bit indicador: ainda não concluído|
|uni_int(0,13)|Identificador de transformação|
|variável|Dados de transformação (depende da transformação)|

A transformação é usada para modificar dados de pixel para melhor compactação e para acompanhar os valores de pixel que realmente ocorrem.

## Dados de pixel ##

Esta parte contém os dados de pixel reais codificados usando a codificação de entropia MANIAC. Os pixels podem ser codificados usando codificação entrelaçada ou não entrelaçada.

### Método entrelaçado ###

Neste método, os níveis de zoom são definidos. Zoomlevel 0 é usado para a imagem completa, zoomlevel 1 é usado para todas as linhas de número par, zoomlevel 2 é usado para todas as colunas de número par do zoomlevel 1. Em outras palavras, cada zoomlevel de número par 2k é uma versão reduzida do imagem, na escala 1:2^k. Os níveis de zoom são codificados do mais alto para o mais baixo.

### Método não entrelaçado ###

Neste método, a codificação das árvores MANIAC começa imediatamente seguida pela codificação dos pixels.

## Referências ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

