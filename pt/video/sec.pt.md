---
date: 2022-03-25
keywords: sec, .sec, formato de arquivo sec, formato de arquivo .sec, extensão .sec, extensão sec
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo SEC e APIs que podem criar e abrir arquivos SEC."
title: Formato de arquivo SEC - Arquivo de vídeo de segurança Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## O que é um arquivo SEC?

Um arquivo SEC é um arquivo de vídeo criado com o sistema de vigilância Samsung DVR. O vídeo é capturado de câmeras de vigilância e armazenado em disco no formato SEC. O vídeo SEC gravado pode ser reproduzido com o software de vídeo da Samsung que pode gerenciar o feed de vídeo de várias câmeras.

## Formato de arquivo SEC - Mais informações

Os arquivos SEC contêm fluxo h264/AVC dentro usando o formato de arquivo proprietário. O cabeçalho de um arquivo SEC começa com o número do modelo do SRD-1670D. As informações de data e hora são mantidas no final do arquivo.

### Converter arquivo SEC para AVI

O arquivo SEC pode ser convertido para o formato de arquivo padrão [AVI](/pt/video/avi/) usando FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referências ##

- [Arquivos Samsung e SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

