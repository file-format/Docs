---
date: 2019-10-11
keywords: rm, .rm, formato de arquivo rm, formato de arquivo .rm, extensão .rm, formato de arquivo RealMedia
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo RM e as APIs que podem criar e abrir arquivos RM."
title: Formato de arquivo RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## O que é um arquivo RM? ##

RealMedia é um formato de contêiner multimídia proprietário desenvolvido pela RealNetworks que usa a extensão .rm. Ele é usado com a combinação de [RealAudio (RA)](/pt/audio/ra/) e [RealVideo(RV)](/pt/video/rv/) para streaming pela Internet. Esses fluxos são de taxa de bits constante. Para taxa de bits variável, a RealNetworks desenvolveu o formato RealMedia Variable Bitrate (RMVB). RealMedia é adequado para streaming de conteúdo pela Internet e pode ser usado para streaming de televisão ao vivo, por exemplo.

## Estrutura do arquivo RealMedia ##

Um arquivo RealMedia consiste em uma série de blocos, cada um com a seguinte estrutura:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

A seguir estão os tipos de pedaços presentes no arquivo RealMedia:

- **Cabeçalho do arquivo RealMedia (.RMF)**: Este deve ser o primeiro pedaço do arquivo RealMedia. Apenas um fragmento RMF está presente em um arquivo. Ele contém informações sobre o número de cabeçalhos.
- **Cabeçalho de propriedades do arquivo (PROP)**: Contém informações sobre as propriedades gerais do arquivo RealMedia. Há apenas um pedaço desse tipo em cada arquivo RealMedia.
- **Cabeçalho de propriedades de mídia (MDPR)**: Este bloco contém informações sobre as propriedades do fluxo. Ele contém informações sobre o tipo de fluxo e o codec usado. Há um pedaço MDPR para cada fluxo no arquivo.
- **Cabeçalho de descrição do conteúdo (CONT)**: Este bloco contém informações de texto como o título ou autor do conteúdo no arquivo RealMedia. Este pedaço é apenas para fins informativos.
- **Cabeçalho de dados (DATA)**: Este bloco contém um grupo de pacotes de dados.
- **Cabeçalho de índice (INDX)**: Este fragmento vem depois de todos os fragmentos de DADOS e contém entradas de índice. Um arquivo pode ter mais de um fragmento INDX.

## Formatos de áudio e vídeo suportados ##

### Formatos de áudio ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipro: Sipro
- cozinhar: cozinhar
- atrc: ATRAC3
- ralf: Formato sem perdas RealAudio
- raac: LC-AAC
- rap: HE-AAC

### Formatos de vídeo ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: precursor H.264
- RV40: precursor H.264, RV40
- RVTR: H.263+ (RV20)

## Referências ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

