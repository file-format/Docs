---
date: 2020-08-12
keywords: jxr, .jxr, formato de arquivo jxr, como abrir arquivos jxr, extensão .jxr, extensão jxr
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo JXR
linktitle: JXR
description: "Saiba mais sobre o formato de arquivo JXR e as APIs que podem criar e abrir arquivos JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## O que é um arquivo JXR? ##

JPEG XR (alcance estendido JPEG) é um formato de arquivo para imagens fotográficas de tom contínuo. É um padrão de compactação de imagens estáticas baseado no HD Photo desenvolvido pela Microsoft. Ele suporta compressão com e sem perdas.

## Breve história ##

O Windows Media Photo foi anunciado pela primeira vez pela Microsoft no WinHEC 2006. Foi renomeado para HD Photo em novembro de 2006. O JPEG XR foi aprovado como Padrão Internacional ISO/IEC 29199-2 em 19 de junho de 2009. O ITU-T e o ISO/IEC publicaram uma moção especificação de formato (ITU-T T.833 | ISO/IEC 29199-3), um conjunto de teste de conformidade (ITU-T T.834 | ISO/IEC 29199-4) e software de referência (ITU-T T.835 | ISO /IEC 29199-5) para JPEG XR após a conclusão da especificação de codificação de imagem em 2010. Um relatório técnico descrevendo a arquitetura de fluxo de trabalho para JPEG XR foi publicado em 2011.

## Projeto JPEG XR ##

Em comparação com o JPEG, o JPEG XR oferece várias melhorias, incluindo:

- **Melhor compactação**: JPEG XR oferece taxas de compactação mais altas.
- **Compressão sem perdas**: JPEG XR suporta compressão sem perdas.
- **Estrutura de mosaico**: a imagem JPEG XR pode ser segmentada em regiões de mosaico onde cada região pode ser decodificada separadamente.
- **Mais precisão de cores**: JPEG XR inclui conversão interna para o espaço de cores YCoCg para suportar imagens usando espaço de cores RGB. O JPEG XR também oferece suporte a um modelo de cores CMYK inteiro de 16 bits por componente (64 bits por pixel). O JPEG XR suporta o formato de cor de ponto flutuante de expoente compartilhado RGBE para imagens HDR. O JPEG XR também suporta codificações de cores em tons de cinza e multicanal.
- **Mapa de transparência**: JPEG XR suporta o canal alfa para transparência.
- **Modificação de imagem de domínio compactado**: as imagens JPEG XR podem ser convertidas em codificação com perdas, reduzidas em resolução, cortadas, invertidas, giradas e a estrutura do bloco pode ser alterada sem decodificação completa do arquivo.
- **Suporte a metadados**: o arquivo de imagem JPEG XR pode conter perfil de cores ICC para uma representação de cores consistente em vários dispositivos. O formato também suporta os formatos de metadados Exif e XMP.

## Formato do Contêiner ##

Os dados de imagem JPEG XR podem ser armazenados no formato de contêiner do tipo TIFF usando uma tabela de tags do Diretório de Arquivos de Imagem (IFT). Um arquivo JXR contém o seguinte em tags IFD:

- Dados de imagem: São dados de imagem contíguos e autocontidos.
- Dados do canal alfa opcional: Se estiverem presentes, os dados da imagem podem ser compactados separadamente permitindo o suporte de aplicativos que não suportam transparência.
- Metadados
- Metadados XMP opcionais
- Metadados Exif opcionais

Como é baseado no formato TIFF, ele herda todas as limitações do formato TIFF, como o limite de tamanho de arquivo de 4 GB.

## Referências ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

