---
date: 2019-12-13
keywords: m3u, formato de arquivo m3u, extensão .m3u, lista de reprodução multimídia m3u, formato de lista de reprodução m3u
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo M3U e as APIs que podem criar e abrir arquivos M3U."
title: Formato de arquivo M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## O que é um arquivo M3U? ##

M3U (MP3 URL) é um arquivo de lista de reprodução de áudio armazenado com a extensão .m3u. M3U não é um arquivo de áudio real, apenas aponta para arquivos de áudio e às vezes de vídeo. O M3U foi desenvolvido para ser usado com o software Winplay3 da Fraunhofer. Também é suportado por vários players de mídia e software.

## Formato de arquivo M3U

Não há especificação oficial para o formato de arquivo M3U, é um padrão de fato. M3U é um arquivo de texto simples que usa a extensão .m3u se o texto estiver codificado na codificação não Unicode padrão do sistema local ou com a extensão .m3u8 se o texto for codificado em UTF-8. Cada entrada no arquivo M3U pode ser uma das seguintes:

- Caminho absoluto para o arquivo
- Caminho do arquivo relativo ao arquivo M3U.
- URL

### M3U Estendido ###

No M3U estendido, são introduzidas diretivas adicionais que começam com "#" e terminam com dois pontos (:) se tiverem parâmetros. Abaixo está uma lista de diretivas para M3U estendida.

- **#EXTM3U** - É o cabeçalho do arquivo indicando M3U Estendido e deve ser a primeira linha do arquivo.
- **#EXTENC:** - Codificação de texto. Deve ser a 2ª linha do arquivo.
- **#EXTINF:** - Usado para informações de faixas e outras propriedades adicionais.
- **#PLAYLIST:** - O título da playlist
- **#EXTGRP:** - Iniciar o agrupamento de nomes
- **#EXTALB:** - Informações do álbum
- **#EXTART:** - Artista do álbum
- **#EXTGENRE** - Gênero do álbum
- **#EXTM3A** - Lista de reprodução de arquivo único para faixas ou capítulos de álbuns.
- **#EXTBYT:** - Tamanho do arquivo em bytes.
- **#EXTBIN:** - Seguem os dados binários.
- **#EXTIMG:** - Logo, Capa ou outras imagens.

### HLS M3U ###

HLS (HTTP Live Streaming) foi criado pela Apple para transmitir áudio e rádio para dispositivos iOS. É baseado no M3U estendido codificado em UTF-8. Foi padronizado como RFC 8216 em 2017 pela IETF. As tags para a lista de reprodução HLS começam com "#EXT-X-". Dada a seguir é uma lista de tags para HLS

- **EXT-X-VERSION** - Indica a versão de compatibilidade do arquivo com base na mídia e seu servidor.
- **#EXT-X-START:** - Indica o ponto de partida preferido para a lista de reprodução.
- **#EXT-X-PLAYLIST-TYPE:** - Fornece o tipo de playlist (EVENTO ou VOD).
- **#EXT-X-TARGETDURATION:** - Especifica a duração máxima do Segmento.
- **#EXT-X-MEDIA-SEQUENCE:** - Indica o Número de Sequência da Mídia.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Indica que todas as amostras de mídia são independentes e podem ser decodificadas sem outros segmentos.
- **#EXT-X-MEDIA:** - É usado para relacionar listas de reprodução de mídia que contêm versões alternativas do mesmo conteúdo.
- **#EXT-X-STREAM-INF:** - Especifica um Variant Stream que faz parte das Renditions.
- **#EXT-X-BYTERANGE:** - Indica que o segmento de mídia é um subintervalo do recurso identificado por seu URI.
- **#EXT-X-DISCONTINUITY** - Indica descontinuidade entre os segmentos de mídia anterior e seguinte.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Permite a sincronização entre diferentes versões do mesmo Variant Stream ou diferentes Variant Streams.
- **#EXT-X-KEY:** - Especifica como descriptografar segmentos de mídia.
- **#EXT-X-MAP:** - Especifica como obter a seção de inicialização de mídia. É necessário analisar os segmentos de mídia aplicáveis.
- **#EXT-X-PROGRAM-DATE-TIME:** - Associa a primeira amostra do Segmento de Mídia a uma data e/ou hora absoluta.
- **#EXT-X-DATERANGE:** - Associa um Data Range.
- **#EXT-XI-FRAMES-ONLY** - Indica que cada segmento de mídia na lista de reprodução descreve um único quadro I.
- **EXT-XI-FRAME-STREAM-INF** - Indica que o arquivo de playlist contém I-frames de apresentação multimídia.
- **#EXT-X-SESSION-DATA:** - Permite que dados de sessão arbitrários sejam
carregado em uma lista de reprodução principal.
- **#EXT-X-SESSION-KEY:** - Permite chaves de criptografia. O cliente pode pré-carregar essas chaves sem ler a lista de reprodução primeiro.
- **#EXT-X-ENDLIST** - Indica que não serão adicionados mais segmentos de mídia ao arquivo.

A seguir está a lista de tipos de mídia da Internet usados pelo M3U:

- **application/vnd.apple.mpegurl**: É o único tipo de mídia registrado (registrado em 2009) para M3U que é usado para fazer referência às listas de reprodução em aplicativos HLS.
- Os seguintes tipos de mídia da Internet são usados por aplicativos não HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Exemplo M3U ##

Este é um exemplo do arquivo M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referências ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Transmissão ao vivo HTTP](https://tools.ietf.org/html/rfc8216)

