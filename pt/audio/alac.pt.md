---
date: 2021-03-21
keywords: alac, formato de arquivo alac, extensão .alac
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo ALAC e as APIs que podem criar e abrir arquivos ALAC."
title: ALAC - Formato de arquivo de codec de áudio sem perdas da Apple
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## O que é um arquivo ALAC?

O formato de arquivo ALAC é o Apple Lossless Audio Codec (ALAC) que usa o contêiner QuickTime compatível com MPEG-4. Foi introduzido em 2004 como formato de arquivo proprietário, até 2011, quando a Apple o disponibilizou de código aberto e livre de royalties. O formato é semelhante ao [FLAC](/pt/audio/flac/) (Free Lossless Audio Codec), mas oferece mais compressão comparativamente. Oferece melhor som alternativo para [AAC](/pt/audio/aac/) ou [MP3](/pt/audio/mp3/). Arquivos de áudio codificados com codec ALAC podem ser abertos usando Apple QuickTime, Apple iTunes e Microsoft Windows Media Player com codec K-Lite.

## Formato de arquivo ALAC

Arquivos baseados no codec ALAC são arquivos binários que estão disponíveis como [código aberto no GitHub](https://github.com/macosforge/alac) para referência do desenvolvedor. Ele contém as fontes para o codificador e decodificador ALAC. A Apple também forneceu um utilitário de linha de comando, chamado `alacconvert`, para ler e gravar os dados de áudio de/para arquivos Core Audio Format (CAF) e [WAVE](/pt/audio/wav/). A seguir estão alguns pontos-chave sobre o formato de arquivo ALAC.

1. 'Profundidade de bits' - 16, 20, 24 e 32 bits.
1. `Taxa de amostragem` - Qualquer taxa de amostragem inteira arbitrária de 1 a 384.000 Hz. Taxas teóricas de até 4.294.967.295 (2^32 - 1) Hz podem ser suportadas.
1. `Packet Size` - O tamanho padrão do pacote é de 4096 quadros de amostra de áudio por pacote. Outros tamanhos de pacotes são certamente possíveis. No entanto, não há garantia de que tamanhos de pacote não padrão funcionem corretamente em todos os dispositivos de hardware compatíveis com Apple Lossless. Pacotes acima de 16.384 quadros de amostra não são suportados.
1. `Canais Suportados` - Suporta de um a oito canais. Cada canal tem a seguinte ordem de informações.

|Num Chan| Encomenda|
|---|---|
|1 |mono|
|2 |estéreo (esquerda, direita)|
|3 |MPEG 3.0 B (Centro, Esquerda, Direita)|
|4 |MPEG 4.0 B (Centro, Esquerda, Direita, Surround Central)|
|5 |MPEG 5.0 D (Centro, Esquerda, Direita, Surround Esquerdo, Surround Direito)|
|6 |MPEG 5.1 D (Centro, Esquerda, Direita, Surround Esquerdo, Surround Direito, Efeitos de Baixa Frequência)|
|7 |Apple AAC 6.1 (Centro, Esquerda, Direita, Surround Esquerdo, Surround Direito, Surround Central, Efeitos de Baixa Frequência)|
|8 |MPEG 7.1 B (Centro, Centro Esquerdo, Centro Direito, Esquerdo, Direito, Surround Esquerdo, Surround Direito, Efeitos de Baixa Frequência)|

## Referências

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Codec de áudio sem perdas da Apple](https://macosforge.github.io/alac/)
* [macosforge - alac no GitHub](https://github.com/macosforge/alac)

