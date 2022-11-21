---
date: 2022-03-20
keywords: mxl, formato de arquivo Musepack, extensão .mxl
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo MXL e APIs que podem criar e abrir arquivos MXL."
title: Formato de arquivo MXL - arquivo MusicXML compactado
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## O que é um arquivo MXL?

Um arquivo MXL é a forma compactada do formato de arquivo MusicXML que é um formato padrão aberto para troca de partituras digitais. Os arquivos MusicXML de texto simples são grandes em tamanho e o uso de tais arquivos como um formato de distribuição de folha foi afetado pelo tamanho do arquivo grande. Esses problemas foram tratados com o [MusicXML](https://www.musicxml.com/) 2.0, introduzindo o formato de arquivo MXL que compacta os arquivos o suficiente para reduzir o tamanho do arquivo semelhante ao dos arquivos MIDI originais. O tipo de mídia recomendado para arquivos MXL é application/vnd.recordare.musicxml.

## Formato de arquivo MXL

Os arquivos MXL são armazenados como [ZIP](/pt/compression/zip/) arquivos compactados [XML](/pt/web/xml/) com extensão de arquivo .mxl. Os arquivos MXL são compactados com o algoritmo DEFLATE conforme especificado na [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Estrutura do arquivo MXL

Cada arquivo MXL tem um formato XML baseado em ZIP que deve ter um arquivo META-INF/container.xml que descreve o ponto de partida da versão MusicXML do arquivo. Não há arquivo .xsd correspondente definido para o formato de arquivo MXL.

Um arquivo container.xml simples tem o conteúdo a seguir. Este exemplo foi retirado do arquivo Dichterliebe01.mxl disponível no site MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Neste exemplo, o<container> elemento é o elemento do documento. o<rootfiles> elemento pode conter um ou mais<rootfile> elementos, com o primeiro<rootfile> elemento que descreve a raiz MusicXML. Um arquivo MusicXML usado como<rootfile> pode ter<score-partwise> ,<score-timewise> , ou<opus> como seu elemento de documento.

## Referências

* [Arquivos MXL compactados](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

