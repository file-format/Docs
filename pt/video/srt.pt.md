---
date: 2019-10-11
keywords: srt, .srt, formato de arquivo srt, formato de arquivo .srt, extensão .srt, extensão srt
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo SRT e as APIs que podem criar e abrir arquivos SRT."
title: Formato de arquivo SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## O que é um arquivo SRT? ##

SRT (formato de arquivo SubRip) é um arquivo de legenda simples salvo no formato de arquivo SubRip com a extensão .srt. Ele contém um número sequencial de legendas, carimbos de data e hora de início e fim e texto de legenda. Os arquivos SRT possibilitam adicionar legendas ao conteúdo de vídeo após sua produção.

## Estrutura do arquivo SRT ##

Cada legenda tem quatro partes no arquivo SRT.

1. Um contador numérico que indica o número ou a posição da legenda.
1. Hora de início e término da legenda separada por --> caracteres
1. Texto da legenda em uma ou mais linhas.
1. Uma linha em branco indicando o final da legenda.

### Exemplo de SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Para especificar o formato de hora *horas:minutos:segundos,milissegundos (00:00:00.000)* é usado.

## Formatação de arquivos SRT ##

A formatação de arquivos SRT é derivada de tags HTML. As tags de formatação do arquivo SRT estão listadas abaixo.

| Efeito | Etiquetas |
| --- | --- |
|Negrito|**\ <b>...\</b> ** ou {b}...{/b}|
|Itálico|**\ <i>...\</i> ** ou **{i}...{/i}**|
|Sublinhado|**\ <u>...\</u> ** ou **{u}...{/u}**|
|Cor da fonte|**\ <font color="white">...\</font> **|
|Line Position|**{\a3}** (indica que o texto deve começar a aparecer na linha 3)

## Software SubRip ##

SubRip é um programa de software gratuito que roda no Windows. Extrai legendas e seus tempos de diferentes formatos de vídeo e salva as legendas no formato SRT. SubRip usa reconhecimento óptico de caracteres para extrair legendas de vídeo ao vivo, outros arquivos de vídeo e DVDs.

## Referências ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
