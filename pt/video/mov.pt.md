{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo mov", "formato de arquivo mov", "o que é um arquivo mov", "arquivo", "exemplo mov", "extensão de arquivo mov", "extensão", "formato", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo MOV - Formato de arquivo de filme Apple QuickTime",
  "description":"Saiba mais sobre o formato de arquivo MOV e APIs que podem criar e abrir arquivos MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## O que é um arquivo MOV?

Um arquivo MOV é um tipo de arquivo de vídeo, desenvolvido pela Apple Inc., que contém uma ou mais faixas. Cada faixa armazena um filme, áudio, clipes de filme e legendas. É um contêiner multimídia que pode armazenar diferentes tipos de elementos de mídia. O formato de vídeo MOV é compatível com os sistemas Windows e Macintosh. Ele usa MPEG-4 codificado para compactação e as faixas são mantidas em objetos chamados átomos que são colocados em uma estrutura de dados hierárquica.

## Breve História do Formato de Arquivo MOV

O formato de arquivo MPEG-4 evoluiu da especificação QuickTime File Format (**QTFF**) em 2001. A Organização Internacional de Padronização aprovou o formato e as especificações de sistemas MPEG-4 Parte 1 foram publicadas em 1999. Em 2001, um arquivo de revisão formato [MP4](/pt/video/mp4/) foi publicado.

A primeira versão do MP4 foi revisada em 2003 como MPEG-4 Parte 14 (ISO/IEC 14496-14:2003). Em 2004, o MP4 foi generalizado para definir uma estrutura geral para todos os arquivos de mídia baseados em tempo. Portanto, agora é usado como base para vários outros formatos de arquivos multimídia.

## Formato de arquivo QuickTime (QTFF) - Mais informações

Para trabalhar com multimídia digital, o QTFF pode conter vários tipos de dados. É um formato de ideia para troca de mídia digital, pois o formato define os padrões para descrever qualquer tipo de estrutura de mídia. O formato do arquivo consiste em uma coleção flexível de objetos orientados a objetos. Para o armazenamento de filmes em discos, o QuickTime usa duas estruturas, ou seja, `átomos` e `átomos QT`.

### Átomos

Atom é a unidade básica do arquivo QuickTime. Existem dois campos principais em qualquer átomo antes de qualquer outro campo: os campos Tamanho e Tipo. O campo de tamanho mostra o tamanho do átomo enquanto o campo de tipo indica o tipo de dados armazenados no átomo. Por natureza, os átomos são hierárquicos, o que significa que um átomo pode conter outros átomos que ainda podem conter outros. O layout de um átomo de amostra é mostrado na imagem a seguir.

Cada átomo tem duas partes, `header` e `data`. O cabeçalho contém os campos de tamanho e tipo e a parte de dados contém os dados reais. Além disso, cada campo é explicado abaixo:

### Tamanho do átomo

O cabeçalho e o conteúdo do átomo são indicados por um inteiro de 32 bits conhecido como tamanho do átomo. O campo size contém o tamanho do átomo em bytes, expresso em um inteiro sem sinal de 32 bits.

### Tipo de átomo

O tipo do átomo também é mostrado por um inteiro de 32 bits, que é tratado principalmente como um campo de quatro caracteres com valor knemônico, como 'moov' (0x6D6F6F76) para um átomo de filme ou 'trak' (0x7472616B) para um átomo de pista. Uma vez conhecido o tipo de átomo, ele permite interpretar seus dados.

### Átomos QT e Recipientes Atom

Os átomos QT fornecem um formato de armazenamento de uso geral e têm um cabeçalho estendido que consiste nos campos Tamanho, Tipo, ID do átomo e Contagem de átomos filhos. Os átomos QT são encapsulados em um contêiner de átomos, uma estrutura de dados exclusiva com um cabeçalho com uma contagem de bloqueio. Existe um átomo raiz em cada recipiente de átomos que é o átomo QT. O layout do átomo QT é mostrado na figura abaixo.

O cabeçalho do contêiner do átomo QT tem os seguintes dados:

Reservado: Um elemento de 10 bytes com valor 0.

Contagem de bloqueio: inteiro de 16 bits com valor 0.

Os cabeçalhos do átomo QT têm os seguintes dados:

**Tamanho -** O cabeçalho e o conteúdo do átomo QT são indicados em bytes por um inteiro de 32 bits. No caso de um átomo de folha, este campo contém o tamanho de um único átomo.

**Tipo -** O tipo do átomo é indicado por um inteiro de 32 bits. Caso seja o átomo raiz, então o valor é definido como 'sean'.

**ID do átomo -** É um número inteiro de 32 bits que mostra o ID do átomo e deve ser exclusivo para todos os irmãos. Átomo raiz sempre o valor do ID do átomo como 1.

**Reservado -** Um inteiro de 16 bits que deve ser definido como 0.

**Contagem de filhos -** Um inteiro de 16 bits que indica o número de átomos filhos de um átomo.

**Reservado -** Um inteiro de 32 bits que deve ser definido como 0.

## Estrutura de arquivos de arquivos MOV

Os arquivos MOV consistem em pedaços consecutivos. Cada bloco tem um cabeçalho de 8 bytes: tamanho de bloco de 4 bytes (big-endian, byte alto primeiro) e tipo de bloco de 4 bytes - uma das assinaturas pré-definidas: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". O primeiro pedaço é do tipo "ftype" e possui um subtipo no deslocamento 8. MOV definido pelo subtipo que deve ser "qt". Para compor o arquivo MOV, é necessário iterar pedaços até que o tipo desconhecido seja detectado.

Aqui está um `exemplo de amostra`: Inspecionando os dados binários de um arquivo MOV de amostra, é evidente que ele começa com uma assinatura **ftyp** (hex: 66 74 79 70) no deslocamento 4, que define o tipo de arquivo do contêiner QuickTime. O subtipo de arquivo é **qt~_~_** (hex: 71 74 20 20) que aponta para o tipo de arquivo MOV. O tamanho do primeiro bloco é 32 (hex: 00 00 00 20, big-endian, high byte first), tamanho localizado no deslocamento 0. No deslocamento 32 (hex: 20) está localizado o segundo bloco, que tem tamanho 8 e digite **mdat** (hex: 6D 64 61 74).

O próximo bloco está localizado no deslocamento 32+8#40 (hex: 28) e tem um tamanho 3.263.028 (hex: 00 31 CA 34) e digite **mdat** (hex: 6D 64 61 74) no deslocamento 44 (hex : 2C). O próximo pedaço está localizado no deslocamento 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) e tem um tamanho 21.189 (hex: 00 00 52 C5) e digite **moov** (hex: 6D 6F 6F 76) no deslocamento 1.836.019.574 (hex: 00 31 CA 60). Este é o último pedaço, então o tamanho total do arquivo é 3.263.068+21.189#3.284.257 bytes.

## Como converter arquivo MOV?

Existem muitos players de mídia e editores de vídeo de software disponíveis para converter arquivos MOV em outros formatos de arquivo de vídeo populares. Alguns dos players de mídia que podem converter arquivos MOV para outros formatos incluem:

* Reprodutor de mídia VideoLAN VLC
* Eltima Elmedia Player

Vários players de mídia e editores de vídeo, incluindo o player de mídia VideoLAN VLC e o Eltima Elmedia Player, podem converter arquivos MOV para outros formatos. Esses softwares podem converter arquivos MOV para os seguintes formatos de vídeo.

* Vídeo MPEG-4 - [MP4](/pt/video/mp4/)
* Vídeo WebM - [WEBM](/pt/video/webm/)
* Fluxo de transporte de vídeo - [TS](/pt/video/ts/)
* Formato de sistemas avançados - [ASF](/pt/video/ts/)
* Áudio Ogg Vorbis - [OGG](/pt/audio/ogg/)
* Áudio MP3 - [MP3](/pt/audio/mp3/)
* Codec de áudio sem perdas grátis - [FLAC](/pt/audio/flac/)
* Áudio WAVE - [WAV](/pt/audio/wav/)

## API de código aberto para arquivos MOV

* [React Native API para converter MOV para MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API Python para reparar arquivos MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby para converter MOV para GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referências

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

