{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo QT - Arquivo de filme rápido",
  "keywords" :[ "QT", "QuickTime video", "qt format", "como reproduzir arquivos qt", "Quick Movie File", "QTFF", "video", "Apple" ],
  "description":"Saiba mais sobre o formato de arquivo QT e APIs que podem criar e abrir arquivos QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## O que é um arquivo QT?

Um arquivo com extensão .qt é um arquivo contêiner multimídia usado pela estrutura do QuickTime para armazenar o conteúdo do arquivo multimídia. Desenvolvido pela Apple Inc., o QuickTime File Format (QTFF) é um arquivo de contêiner multimídia que contém áudio, vídeo ou texto para reprodução posterior. É o formato de escolha para a troca de mídia digital entre dispositivos, aplicativos e sistemas operacionais. Os arquivos QT também são salvos no formato [MOV](/pt/video/mov/) que também foi desenvolvido pela Apple Inc. Alguns dos aplicativos que podem abrir arquivos QT incluem o Apple QuickTime player, o VLC media player e o Media Player Classic com K- Pacote de Codec Lite.

## Formato de arquivo QT

O QTFF é orientado a objetos que expõe uma coleção flexível de objetos para facilitar a análise e a expansão. Cada faixa em um arquivo QT contém um fluxo de mídia codificado digitalmente ou uma referência de dados ao fluxo de mídia localizado em outro arquivo. A estrutura de dados hierárquica que consiste em objetos chamados átomos atua como contêineres de trilhas. As especificações de formato de arquivo para [formato de arquivo QT](https://developer.apple.com/documentation/quicktime-file-format) estão oficialmente disponíveis pela Apple Inc para referência do desenvolvedor.

### Descrição da mídia

A descrição de mídia de um arquivo QuickTime é armazenada separadamente dos dados de mídia. Informações como o número de faixas, formato de compactação de vídeo e informações de tempo são armazenadas na descrição da mídia (também conhecida como recurso de filme, átomo de filme ou simplesmente o filme). Os dados de mídia são referenciados por um índice nessa estrutura de mídia. Os dados de mídia são os dados de amostra reais, como quadros de vídeo e amostras de áudio, usados no filme.

### Átomos

Atom é a unidade básica do arquivo QuickTime. Existem dois campos principais em qualquer átomo antes de qualquer outro campo: os campos Tamanho e Tipo. O campo de tamanho mostra o tamanho do átomo enquanto o campo de tipo indica o tipo de dados armazenados no átomo. Por natureza, os átomos são hierárquicos, o que significa que um átomo pode conter outros átomos que ainda podem conter outros. O layout de um átomo de amostra é mostrado na imagem a seguir.

Cada átomo tem duas partes, cabeçalho e dados. O cabeçalho contém os campos de tamanho e tipo e a parte de dados contém os dados reais. Além disso, cada campo é explicado abaixo:

#### Tamanho do átomo

O cabeçalho e o conteúdo do átomo são indicados por um inteiro de 32 bits conhecido como tamanho do átomo. O campo size contém o tamanho do átomo em bytes, expresso em um inteiro sem sinal de 32 bits.

#### Tipo de átomo

O tipo do átomo também é mostrado por um inteiro de 32 bits, que é tratado principalmente como um campo de quatro caracteres com valor knemônico, como 'moov' (0x6D6F6F76) para um átomo de filme ou 'trak' (0x7472616B) para um átomo de pista. Uma vez conhecido o tipo de átomo, ele permite interpretar seus dados.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Estrutura do arquivo ##

Os arquivos QT/MOV consistem em pedaços consecutivos. Cada bloco tem um cabeçalho de 8 bytes: tamanho de bloco de 4 bytes (big-endian, byte alto primeiro) e tipo de bloco de 4 bytes - uma das assinaturas pré-definidas: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". O primeiro pedaço é do tipo "ftype" e possui um subtipo no deslocamento 8. MOV definido pelo subtipo que deve ser "qt". Para compor o arquivo MOV, é necessário iterar pedaços até que o tipo desconhecido seja detectado.

Aqui está um exemplo de exemplo: Inspecionando os dados binários de um arquivo MOV de amostra, é evidente que ele começa com uma assinatura **ftyp** (hex: 66 74 79 70) no deslocamento 4, que define o tipo de arquivo do contêiner QuickTime. O subtipo de arquivo é **qt~_~_** (hex: 71 74 20 20) que aponta para o tipo de arquivo MOV. O tamanho do primeiro bloco é 32 (hex: 00 00 00 20, big-endian, high byte first), tamanho localizado no deslocamento 0. No deslocamento 32 (hex: 20) está localizado o segundo bloco, que tem tamanho 8 e digite **mdat** (hex: 6D 64 61 74).

O próximo bloco está localizado no deslocamento 32+8#40 (hex: 28) e tem um tamanho 3.263.028 (hex: 00 31 CA 34) e digite **mdat** (hex: 6D 64 61 74) no deslocamento 44 (hex : 2C). O próximo pedaço está localizado no deslocamento 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) e tem um tamanho 21.189 (hex: 00 00 52 C5) e digite **moov** (hex: 6D 6F 6F 76) no deslocamento 1.836.019.574 (hex: 00 31 CA 60). Este é o último pedaço, então o tamanho total do arquivo é 3.263.068+21.189#3.284.257 bytes.

## Referências ##

* [Formato de arquivo QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [QuickTime File Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)
