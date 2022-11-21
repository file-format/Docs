---
date: 2019-10-11
keywords: MP4, arquivo, extensão, formato, formato de vídeo, MPEG-4
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo MP4 e as APIs que podem criar e abrir arquivos MP4."
title: Formato de arquivo MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## O que é um arquivo MP4? ##

MP4 (abreviação de MPEG-4 Parte 14) é um formato de arquivo baseado em ISO/IEC 14496-12:2004 que é baseado no formato de arquivo QuickTime, mas especifica formalmente suporte para Descritores de Objeto Inicial (IOD) e outros recursos MPEG. É usado principalmente para armazenar vídeo e áudio, mas também pode ser usado para armazenar legendas e imagens estáticas. Os arquivos MP4 são armazenados com a extensão .mp4. MP4 é um padrão internacional de codificação audiovisual. Semelhante aos formatos de contêiner mais modernos, o MP4 suporta streaming pela Internet. Devido à alta compactação usada no MP4, os arquivos resultantes são menores em tamanho, com quase toda a qualidade original mantida.

## Breve história ##

A especificação MP4 foi desenvolvida pelo Moving Picture Experts Group (MPEG) e foi baseada no formato QuickTime [MOV](/pt/video/mov/) que foi publicado em 2001. A primeira versão (ISO/IEC 14496-1:2001) do MP4 foi uma revisão da MPEG-4 Part 1: Systems Specification publicada em 1999. O formato de arquivo MP4 foi generalizado para ISO Base Media File Format ISO/IEC 14496-12:2004 que definiu a estrutura geral para arquivos de mídia baseados em tempo. Como resultado, ele é usado como base para outros formatos de arquivo.

## Estrutura de arquivos MP4 ##

O MP4 é um arquivo de contêiner extensível, o que significa que não define uma estrutura estrita e permite estrutura e hierarquia personalizadas para cada tipo de mídia. Os dados no arquivo MP4 são divididos em duas seções, a primeira contendo os dados relacionados à mídia e a segunda contendo metadados. Os dados de mídia contêm áudio ou vídeo e metadados indicam sinalizadores para acesso aleatório, carimbos de data/hora, etc.
As estruturas em MP4 são normalmente referidas como átomos ou caixas. O tamanho mínimo de um átomo é de 8 bytes (os primeiros 4 bytes especificam o tamanho e os próximos 4 bytes especificam o tipo). Aqui está uma lista dos átomos de nível raiz contidos nos arquivos MP:

- **ftyp**: contém o tipo de arquivo, a descrição e as estruturas de dados comuns usadas.
- **pdin**: contém informações de carregamento/download progressivo de vídeo.
- **moov**: Container para todos os metadados do filme.
- **moof**: contêiner com fragmentos de vídeo.
- **mfra**: o contêiner com acesso aleatório ao fragmento de vídeo
- **mdat**: contêiner de dados para mídia.
- **stts**: tabela amostra-tempo.
- **stsc**: tabela de amostra para bloco.
- **stsz**: tamanhos de amostra (enquadramento)
- **meta**: O contêiner com as informações de metadados.

Aqui está uma lista de átomos de segundo nível usados no MP4:

- **mvhd**: Contém as informações do cabeçalho do vídeo com todos os detalhes do vídeo.
- **trak**: Container com pista individual.
- **udta**: O container com o usuário e informações de rastreamento.
- **iods**: descritor de arquivo MP4

## Referências ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

