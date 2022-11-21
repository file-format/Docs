---
date: 2022-01-06
keywords: vtt, .vtt, formato de arquivo vtt, formato de arquivo .vtt, extensão .vtt, extensão vtt
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Saiba mais sobre o arquivo .vtt e as APIs que podem criar e abrir arquivos VTT."
title: Formato de arquivo VTT - Arquivo de faixas de texto de vídeo da Web
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## O que é um arquivo VTT?

Um arquivo VTT é um arquivo de texto que contém informações para exibir faixas de texto com tempo (como legendas ou legendas) usando o formato Web Video Text Tracks (WebVTT). As faixas de texto temporizadas incluem informações como legendas ou legendas. O objetivo do arquivo VTT é adicionar sobreposições de texto a um<video> . O formato é um pouco semelhante aos arquivos SRT. Arquivos de texto baseados em WebVTT são codificados usando UTF-8. Um arquivo VTT contém informações como legendas, descrições, legendas, descrições, capítulos e metadados. Sendo arquivos de texto simples, os arquivos VTT podem ser abertos usando editores de texto como Microsoft Notepad, Apple TextEdit e Notepad++.

## Formato de arquivo VTT - Mais informações

Os arquivos VTT usam o formato de arquivo WebVTT para salvar informações de faixas de texto sequenciais. Cada faixa de texto temporizada consiste em uma única linha ou várias linhas, também conhecidas como `cue`, conforme mostrado no exemplo a seguir.

### Exemplo de arquivo VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Estrutura do arquivo VTT

A seguir estão os requisitos de estrutura de um arquivo VTT.

* Uma marca de ordem de byte opcional (BOM).
* A string "WEBVTT".
* Um cabeçalho de texto opcional à direita de WEBVTT.
* Uma linha em branco, que equivale a duas novas linhas consecutivas.
* Zero ou mais sugestões ou comentários.
* Zero ou mais linhas em branco.

## Referências

* [VTT - Escolas W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

