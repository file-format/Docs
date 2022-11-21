---
date: 2019-10-11
keywords: prc, .prc, formato de arquivo prc, como abrir arquivos prc, extensão .prc, extensão prc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo RPC
linktitle: PRC
description: "Saiba mais sobre o formato de arquivo PRC e as APIs que podem criar e abrir arquivos PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Os formatos de arquivo PRC
As extensões ".prc" estão sendo usadas para o formato de arquivo Product Representation Compact 3D e um formato de arquivo de e-book pela MobiPocket.

## O que é um arquivo Product Representation Compact (PRC)?

PRC (Product Representation Compact) é um formato de arquivo 3D otimizado para armazenar, carregar e exibir dados 3D, especialmente provenientes de sistemas CAD (Computer-Aided Design). É um arquivo binário sequencial, escrito de forma portátil. O PRC pode ser usado para incorporar dados 3D em um arquivo PDF. O PRC suporta a maioria das principais construções de CAD, como montagens e peças, árvores de entidades 3D, representação de geometria exata, representação triangulada e marcação. O PRC usa a extensão .prc e o tipo de mídia de internet usado é *model/prc*.

PRC é um formato de arquivo multiuso que, com base em seu uso, pode ser armazenado usando compactação regular para representar diretamente dados CAD ou ser armazenado usando alta compactação para reduzir o tamanho do arquivo. Os dados 3D armazenados em um PDF usando o formato PRC são interoperáveis com aplicativos CAM e CAE.

### Especificação do formato de arquivo PRC (Product Representation Compact)

Um arquivo PRC tem uma seção de cabeçalho principal seguida por uma ou mais estruturas de arquivo seguidas por um arquivo de modelo no final. Uma estrutura de arquivo tem um cabeçalho seguido pelas seguintes seções de dados:

- **Globals**: Contém as estruturas de arquivos e cores referenciadas, estilos de linha e sistemas de coordenadas para cada entidade de árvore da estrutura de arquivos.
- **Árvore**: Contém uma descrição da árvore de itens como ocorrências de produtos, definições de peças, itens de representação e marcação.
- **Tessellation**: Contém todos os dados tesselados(triangulados) nas entidades folha da árvore (itens de representação e marcações).
- **Geometria**: Contém todos os dados exatos de geometria e topologia das entidades folha da árvore (itens de representação).
- **Geometria extra**: Contém os dados de resumo da geometria. Isso permite que o arquivo seja carregado parcialmente sem carregar toda a geometria.

A seguir está a estrutura de um arquivo PRC típico.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## O que é um arquivo de e-book MobiPocket com extensão PRC
Um formato de arquivo de e-book que é introduzido por uma empresa francesa chamada **Mobipocket** também está usando a extensão ".prc". Inicialmente, o Mobipocket lançou um aplicativo gratuito para vários dispositivos inteligentes como, tablets, PDAs e smartphones. A extensão ".prc" é na verdade idêntica a .mobi, mas é usada principalmente para PDAs que suportam apenas extensões **.prc** ou **.pdb**.

### Especificações de formato de arquivo Mobipocket PRC
O formato de arquivo MobiPocket PRC é baseado no padrão Open eBook usando XHTML e também pode incluir JavaScript e quadros. O suporte para consultas SQL nativas a serem usadas com bancos de dados incorporados também está disponível.

O Mobipocket Reader possui uma biblioteca de páginas iniciais. Os leitores podem inserir páginas em branco em qualquer parte de um livro e adicionar desenhos variáveis. Os objetos como anotações, marcadores, correções, notas e desenhos são gerenciáveis a partir de um único local. As imagens são convertidas para o formato GIF e têm um tamanho máximo de 64K, o que é suficiente para celulares com telas pequenas. O Mobipocket Reader possui marcadores eletrônicos e um dicionário integrado.

O leitor tem um modo de tela cheia para leitura e suporte para muitos PDAs, Comunicadores e Smartphones. Os produtos Mobipocket suportam a maioria dos sistemas operacionais Palm, Windows, Symbian, BlackBerry, mas não o Android. O leitor funciona em Linux ou Mac OS X usando WINE.

## Referências

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Especificação do formato PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparação de formatos de e-books - Por Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

