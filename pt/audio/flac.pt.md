---
date: 2019-12-13
keywords: flac, formato de arquivo flac, extensão .flac, arquivo flac, flac vs mp3
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo FLAC e as APIs que podem criar e abrir arquivos FLAC."
title: Formato de arquivo FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## O que é um arquivo FLAC?

FLAC (Free Lossless Audio Codec) é um formato de codificação de áudio de compressão sem perdas desenvolvido pela Xiph.Org Foundation. FLAC é um formato aberto isento de royalties que é salvo com a extensão .flac. O áudio digital compactado usando o algoritmo FLAC é normalmente reduzido para 50 a 70 por cento do tamanho. Os arquivos FLAC podem ser descompactados em uma cópia idêntica dos arquivos de áudio originais.

## Formato de arquivo FLAC

Esta é uma visão geral do fluxo de bits FLAC.

- **marcador fLaC**: Este marcador é adicionado ao início do fluxo. Ele é seguido por um ou mais blocos de metadados.
- **Blocos de metadados**: 128 tipos de blocos de metadados são suportados pelo FLAC; atualmente os seguintes são definidos.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Os dados de áudio são compostos por um ou mais quadros de áudio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Breve História do Formato de Arquivo FLAC

Josh Coalson começou o desenvolvimento do FLAC em 2000. A primeira versão do FLAC foi lançada em 20 de julho de 2001. O FLAC foi incorporado sob a bandeira Xiph.Org em 20 de janeiro de 2003. O desenvolvimento do FLAC foi movido para o repositório git Xiph.Org com o lançamento da versão 1.3.0 em 26 de março de 2013.

## Composição do Projeto FLAC

O projeto FLAC consiste no seguinte:

- Formatos de fluxo.
- Formato de contêiner simples para o fluxo (FLAC).
- libFLAC: Uma biblioteca de codificadores de referência, decodificadores e interface de metadados.
- libFLAC++: Um wrapper orientado a objetos para libFLAC.
- flac: Um programa de linha de comando para codificar e decodificar fluxos FLAC.
- metaflac: Um editor de metadados de linha de comando para FLAC.
- Plugins de entrada para players de música como Winamp, XMMX, etc.
- Formato de contêiner Ogg (Ogg FLAC).

## Projeto FLAC

Dependendo da densidade e amplitude da música, o tamanho do arquivo compactado pode ser 80% menor que o arquivo original.

### Codificador de Fonte ###

- Ele suporta apenas amostras inteiras e não de ponto flutuante. Ele pode lidar com resolução de bits PCM de 4 a 32 bits por amostra e taxa de amostragem de 1 Hz a 65.535 Hz. A codificação FLAC é limitada a 24 bits por amostra.
- Os canais podem ser agrupados para aproveitar as correlações entre canais para aumentar a compactação.
- As somas de verificação CRC são usadas para identificar quadros corrompidos.
- Para conversão de amostras de áudio, o FLAC usa previsão linear.

### Metadados ###

- FLAC suporta ReplayGain (usado para perceber e normalizar o volume no áudio).
- FLAC usa o mesmo sistema usado nos comentários Vorbis para marcação.
- libFLAC é usado pela maioria dos aplicativos FLAC para codificação/decodificação.
- A API libFLAC é organizada em fluxos, fluxos pesquisáveis e arquivos para aumentar a abstração do fluxo de bits FLAC básico.

### Compressão ###

libFLAC usa níveis de compressão de 0 a 8 onde 0 é o mais rápido e 8 é o mais lento. Os arquivos compactados são sempre sem perdas, embora a compensação seja entre velocidade e tamanho.

## FLAC vs MP3
O MP3 é um formato de compactação com perdas, o que significa que pode cortar alguma parte do áudio para reduzir seu tamanho após a aplicação da compactação. Considerando que, FLAC é um formato de arquivo sem perdas, o que significa que você pode ouvir o áudio em sua forma mais pura. Anteriormente, os formatos de arquivo sem perdas eram CDA ou WAV, que não eram muito eficientes em termos de espaço como FLAC. A tabela a seguir mostrará a comparação entre esses dois formatos para alguns termos importantes:

|Prazo|FLAC|MP3|
---|---|---|
|**Qualidade de dados**|Sem perda de dados de áudio| Alguns dados podem ser perdidos ao compactar dados de áudio|
|**Tamanho**|Tamanho de arquivo maior em comparação com formatos com perdas. Então precisa de maior capacidade de armazenamento| Tamanho de arquivo menor, adequado para reprodução em dispositivos de áudio compactos com pouco espaço de armazenamento |
|**Requisitos de hardware**| Precisa de equipamento de áudio de alta qualidade e grande capacidade de armazenamento | Grandes bibliotecas de áudio podem ser salvas em um espaço de armazenamento menor. Adequado para dispositivos portáteis, como players de áudio ou telefones celulares|
|**Distribuição pela Internet**|Não pode ser distribuído facilmente pela Internet devido ao tamanho do arquivo enorme |O tamanho do arquivo compacto facilita a distribuição pela Internet|
|**Compatibilidade**|O codec de audição de música e áudio mais popular que praticamente é compatível com todos os dispositivos do planetaCompatível com PCs de nova geração, telefones, receptores AV, players de blu-ray, dispositivos de streaming como Roku ou Fire TV|

## Referências ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

