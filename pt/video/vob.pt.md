---
date: 2019-10-11
keywords: vob, .vob, formato de arquivo vob, formato de arquivo .vob, extensão .vob, extensão vob, formato de vídeo vob, arquivos vob dvd
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo VOB e as APIs que podem criar e abrir arquivos VOB."
title: Formato de arquivo VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## O que é um arquivo VOB? ##

Os arquivos VOB são armazenados normalmente no diretório VIDEO_TS em um DVD com extensão .vob. Os arquivos VOB contêm dados de vídeo e áudio, bem como outros dados, como menus e legendas. O VOB é baseado no formato de fluxo de programa MPEG-2, mas possui limitações e especificações adicionais em fluxos privados. Os arquivos VOB são um subconjunto estrito de fluxos de programas MPEG, portanto, todos os arquivos VOB são fluxos de programas MPEG, mas todos os fluxos de programas MPEG não são compatíveis com VOB.

## Estrutura do Vídeo DVD ##

Quando um DVD é aberto em um computador, VIDEO_TS é o diretório de nível superior com AUDIO_TS. AUDIO_TS está vazio e não é usado. Dentro do diretório VIDEO_TS, existem arquivos VOB, BUP e IFO. Os arquivos VOB contêm o conteúdo MPEG. Eles são divididos em pedaços de 1 GB ou menos para que sejam compatíveis com todos os sistemas operacionais. Os arquivos IFO contêm informações sobre os menus e a estrutura do título. Os arquivos BUK são arquivos de backup dos arquivos IFO com o mesmo nome. Esses arquivos devem ser mantidos em uma área separada fisicamente para que, caso o arquivo IFO seja danificado devido a danos físicos ao DVD, o arquivo BUK possa fornecer as mesmas informações.

### Formato físico ###

- Todos os arquivos no disco devem ser contíguos.
- Os arquivos relacionados devem estar próximos uns dos outros (VOB, IFO, BUP).
- Os arquivos numerados devem estar em ordem crescente.

## Proteção contra cópia ##

Muitos DVDs de vídeo são criptografados e impedem a cópia de dados do DVD. As chaves de autenticação e descriptografia são necessárias para reproduzir os arquivos localizados na área inacessível de entrada do DVD. Essas chaves são usadas pelo software de descriptografia CSS presente no DVD player ou no software player. Sem as chaves, os arquivos de vídeo não podem ser reproduzidos, pois as chaves serão solicitadas quando os arquivos forem abertos.

## Referências ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

