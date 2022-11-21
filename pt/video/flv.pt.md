---
date: 2019-10-11
keywords: flv, .flv, formato de arquivo flv, formato de arquivo .flv, extensão .flv, extensão flv, formato de vídeo flv
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo FLV e as APIs que podem criar e abrir arquivos FLV."
title: Formato de arquivo FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## O que é um arquivo FLV? ##

FLV (Flash Video) é um formato de arquivo contêiner com a extensão .flv. O FLV é usado para fornecer conteúdo de áudio/vídeo pela Internet usando o Adobe Flash Player ou o Adobe Air. Os dados nos arquivos FLV são codificados da mesma forma que os arquivos SWF. O suporte direto foi adicionado ao Flash Player 7 em 2003. Os sistemas Adobe criaram o F4V em 2007 devido às restrições do FLV.

### Codificação ###

Os arquivos FLV contêm fluxos de bits de vídeo do Sorenson Spark, que são uma variante proprietária do padrão de vídeo H.263. É o formato de compactação necessário para o Flash Player 6 e 7. A versão 8 do Flash Player suporta fluxos de bits de vídeo On2 TrueMotion VP6. É o formato de compactação recomendado para o Flash Player 8 e superior. O FLV suporta áudio em MP3, Nellymoser Asao Codec e o codec Speex de código aberto. Ele também suporta áudio não compactado ou áudio no formato ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile e AAC-LC) são suportados pelas versões recentes do Flash Player 9.

## Estrutura ##

Os arquivos FLV consistem em Cabeçalho e Pacotes. Um arquivo FLV começa com o cabeçalho. O cabeçalho tem os seguintes campos.

- **Assinatura**: Seu valor é FLV
- **Versão**: Seu valor padrão é 1. Somente 0x01 é válido.
- **Flags**: 0x04 é usado para áudio e 0x01 é usado para vídeo, então 0x05 é usado para áudio e vídeo.
- **Tamanho do cabeçalho**: O valor padrão é 9. É usado para pular um cabeçalho expandido mais recente.

Após o cabeçalho vem os pacotes. O arquivo FLV é dividido em vários pacotes chamados tags FLV que possuem cabeçalhos de 15 bytes. Os pacotes contêm os metadados de áudio, vídeo, scripts, informações de criptografia e carga útil. Os pacotes FLV possuem os seguintes campos.

- **Reservado**: É reservado para FMS e deve ser 0.
- **Filter**: Indica se os pacotes são filtrados ou não.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Tipo de pacote**: define o tipo de conteúdo do pacote.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Tamanho dos dados**: Indica o comprimento da mensagem.
- **Timestamp Lower**: armazena o timestamp em milissegundos em que os dados da tag se aplicam. Ele é definido como NULL para o primeiro pacote.
- **Timestamp Upper**: Extensão para criar um valor uint32_be.
- **ID do stream**: é definido como NULL para o primeiro stream.
- **Payload Data**: Estes são os dados baseados no tipo de pacote.

## Referências ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

