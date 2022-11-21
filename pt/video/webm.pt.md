---
date: 2019-10-11
keywords: WEBM, O que é um arquivo WEBM, Formato de arquivo WEBM
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Saiba mais sobre o formato de arquivo WEBM e APIs que podem criar e abrir arquivos WEBM."
title: WEBM - Formato de arquivo de vídeo WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## O que é um arquivo WEBM?

Um arquivo com extensão .webm é um arquivo de vídeo baseado no formato de arquivo WebM aberto e isento de royalties. Ele foi projetado para compartilhar vídeo na web e define a estrutura do contêiner de arquivos, incluindo formatos de vídeo e áudio. O WebM é 100% gratuito, implementando alta qualidade com base em tecnologias abertas, como HTML, HTTP e TCP/IP, que podem ser implementadas por qualquer pessoa. O WebM foi projetado especificamente para veicular vídeo na web, o que o torna otimizado para streaming com baixo consumo computacional. Isso o torna adequado para reprodução de vídeos em qualquer dispositivo, especialmente netbooks, handhelds e tablets de baixo consumo.

## Formato de arquivo WEBM

A estrutura do arquivo WebM é baseada em um subconjunto do formato de arquivo contêiner Matroska [MKV](/pt/video/mkv/). Os fluxos de vídeo disponíveis em um arquivo WebM são compactados usando as tecnologias de compactação VP8 ou VP9 que são altamente eficientes na compactação. Da mesma forma, os fluxos de áudio em um arquivo WebM são compactados usando os codecs Vorbis ou Opus que foram desenvolvidos pela [Xiph Foundation](https://www.xiph.org/). Todos esses vídeos e codecs de áudio são isentos de royalties e podem ser usados sem nenhum custo.

A seguir estão as especificações resumidas para o formato de arquivo WebM.

|Campo|Descrição|
---|---|
|tipo MIME |vídeo/webm|
|Somente áudio do tipo MIME |áudio/webm|
|Identificador de tipo uniforme| org.webmproject.webm|
|Nome do codec de vídeo| VP8 ou VP9|
|Nome do codec de áudio| Vorbis ou Opus|

### Elementos WebM

WebM, sendo um subconjunto das especificações do Matroska, fornece suporte para algumas das funcionalidades do Matroska. A seguir está uma descrição dos elementos suportados.

#### EBML

|Nome |Descrição|
---|---|
|EBML|Defina as características EBML dos dados a seguir. Cada documento EBML deve começar com isso.|
|EBMLVersion |A versão do analisador EBML usada para criar o arquivo.|
|EBMLReadVersion|A versão mínima de EBML que um analisador deve suportar para ler este arquivo.|
|EBMLMaxIDLength |O comprimento máximo dos IDs que você encontrará neste arquivo (4 ou menos em Matroska).|
|EBMLMaxSizeLength|O comprimento máximo dos tamanhos que você encontrará neste arquivo (8 ou menos em Matroska). Isso não substitui o tamanho do elemento indicado no início de um elemento. Elementos que têm um tamanho indicado que é maior do que o permitido por EBMLMaxSizeLength devem ser considerados inválidos.|
|DocType|Uma string que descreve o tipo de documento que segue este cabeçalho EBML ("webm" em nosso caso).|
|DocTypeVersion|A versão do interpretador DocType usada para criar o arquivo.|
|DocTypeReadVersion|A versão mínima de DocType que um interpretador deve suportar para ler este arquivo.|

#### Elementos Globais

No momento, apenas o elemento `Void` é suportado, usado para anular dados danificados, para evitar comportamentos inesperados ao usar dados danificados. O conteúdo é descartado. Também usado para reservar espaço em um subelemento para uso posterior.

#### Segmento
Este elemento contém todos os outros elementos de nível superior (nível 1). Normalmente, um arquivo Matroska é composto por 1 segmento.

#### Informações de meta-busca

As seguintes informações de busca são suportadas.

|Nome do elemento |Descrição|
---|---|
|SeekHead |Contém a posição de outro elemento de nível 1.|
|Procurar |Contém uma única entrada de busca para um elemento EBML.|
|SeekID |O ID binário correspondente ao nome do elemento.|
|SeekPosition |A posição do elemento no segmento em octetos (0 = primeiro nível 1 elemento).|

## Referências

* [WebM](https://www.webmproject.org/)
* [Repositórios de código WebM](https://www.webmproject.org/code/#webp-repositories)

