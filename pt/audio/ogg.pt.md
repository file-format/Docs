---
date: 2019-12-13
keywords: ogg, formato de arquivo ogg, extensão .ogg, formato de áudio ogg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo OGG e as APIs que podem criar e abrir arquivos OGG."
title: Arquivo OGG - Arquivo de áudio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## O que é um arquivo OGG?

OGG é um arquivo de áudio compactado Ogg Vorbis que é salvo com a extensão .ogg. Os arquivos OGG são usados para armazenar dados de áudio e também podem incluir informações e metadados de artistas e faixas. OGG é um formato de contêiner aberto e gratuito mantido pela Xiph.Org Foundation.

## Breve História do Formato de Arquivo OGG

O projeto Ogg começou como parte de um projeto maior em 1993 e foi nomeado Squish, mas por causa de uma marca existente, foi renomeado para OggSquish. Foi descrito como uma tentativa de criar um formato de áudio compactado flexível para aplicativos de áudio modernos. A referência OGG foi separada de Vorbis em 2 de setembro de 2000.

OGM foi criado em 2002 devido à falta de suporte formal de vídeo no OGG. Isso permitiu a incorporação de vídeo da estrutura Microsoft DirectShow em um wrapper baseado em OGG. Em 2006, o OGG era suportado por muitos mecanismos de videogame e era comumente usado para codificar conteúdo gratuito. A Free Software Foundation iniciou uma campanha em 15 de maio de 2007 para aumentar o uso do Vorbis como uma alternativa superior ao MP3. Em 30 de junho de 2009, OGG era o único formato de contêiner suportado pela implementação HTML5 do Firefox 3.5.

## Formato de arquivo OGG

O formato OGG consiste em blocos de dados. Cada pedaço é chamado de página Ogg. Cada página começa com "OggS" para identificar o formato Ogg. O cabeçalho contém o número de série e o número da página que identifica cada página como parte de uma série. A página consiste nos seguintes componentes.

- **Cabeçalho da página**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Valor | Descrição |
| --- | --- | --- |
| 0 | 0x01 | Indica que o primeiro pacote da página é a continuação do pacote anterior no fluxo de bits lógico. |
| 1 | 0x02 | Indica que esta página é a primeira no fluxo de bits lógico. |
| 2 | 0x04 | Indica que esta página é a última no fluxo de bits lógico. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadados**: VorbisComment é o mecanismo mais amplamente suportado para armazenar metadados. Outros mecanismos incluem o seguinte:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referências ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

