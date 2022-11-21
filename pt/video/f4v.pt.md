---
date: 2019-10-11
keywords: f4v, .f4v, formato de arquivo f4v, formato de arquivo .f4v, extensão .f4v, extensão f4v, formato de vídeo f4v, como abrir arquivos f4v, o que são arquivos f4v
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo F4V e as APIs que podem criar e abrir arquivos F4V"
title: Formato de arquivo F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## O que é um arquivo F4V? ##

F4V (Flash MP4 Video File) é um arquivo de vídeo salvo com a extensão .f4v. Ele é baseado no formato de arquivo de mídia de base ISO (MPEG-4 Parte 12). É muito semelhante ao [MP4](/pt/video/mp4/) e é por isso que também é chamado informalmente de Flash MP4. [FLV](/pt/video/flv/) tinha limitações ao transmitir conteúdo H.264/ACC, o que resultou na criação do novo formato F4V pela Adobe Systems. O Flash Player pode reproduzir arquivos F4V desde o lançamento do Flash Player 9 Update 3.

## Estrutura de arquivos F4V ##

O formato de arquivo F4V é baseado no formato de arquivo de mídia de base ISO (MPEG-4 Parte 12) e é muito semelhante ao formato MP4. Para obter detalhes sobre a estrutura, consulte a página [MP4](/pt/video/mp4/). A principal diferença entre o F4V e o MP4 são os formatos de metadados que o F4V pode armazenar. Abaixo está a lista dos formatos de metadados suportados pelo formato F4V.

- **Caixa de tags**: quatro caixas de tags opcionais adicionais (auth, title, dscp, cprt) dentro da caixa Movie (moov).
- **Caixa de metadados XMP**: Esta caixa vem logo após a caixa Filme (moov). Com isso, o arquivo pode comunicar metadados XMP a um filme SWF por meio do ActionScript.
- **ilst box**: Esta caixa ocorre dentro da caixa Meta (meta) e pode conter várias tags de metadados. Os tipos de dados suportados são fornecidos abaixo.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Caixa de Metadados de Faixa de Texto**: As amostras de texto (texto ou tx3g) dentro da Caixa de Dados de Mídia (mdat). Ele pode conter as seguintes caixas de metadados.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referências ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

