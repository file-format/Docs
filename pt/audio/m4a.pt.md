{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "arquivo", "extensão", "formato", "o que é formato de arquivo m4a", "música", "formato de arquivo m4a", "M4A vs MP3", "especificação do formato de arquivo m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo M4A e APIs que podem criar, converter e abrir arquivos M4A.",
  "title" :"M4A - Arquivo de áudio MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## O que é um arquivo M4A?

O **formato de arquivo M4A** é um arquivo de áudio criado usando o AAC (Advanced Audio Coding), conhecido como compressão com perdas. A palavra M4A abreviada como MPEG 4 Audio. Esses arquivos de áudio geralmente têm extensão de arquivo .m4a. Isso é especialmente verdadeiro para conteúdo não protegido. Ele pode armazenar vários tipos de conteúdo de áudio, como audiolivros, músicas e podcasts. O M4A é geralmente percebido como um formato mais avançado que o MP3, que normalmente não foi projetado apenas para áudio. É apenas uma camada de áudio em arquivos de vídeo MPEG 1 ou 2.

O formato M4A é criptografado pelo FairPlay Digital Rights Management, pois foi vendido pela iTunes Store usando a extensão .m4p. Os iPhones da Apple usam áudio MPEG-4 para seus toques, mas esses arquivos de áudio usam a extensão .m4r.


## M4A vs MP3

Tanto M4A quanto [MP3](/audio/mp3/) são formatos de arquivo somente de áudio.

**M4A**: Melhor que MP3 em termos de qualidade e tamanho quando codificado na mesma taxa de bits. A extensão de arquivo .m4a é tão comum porque foi usada pela Apple para uso na iTunes Music Store. O M4A é um arquivo de áudio compactado usando a tecnologia MPEG-4; um algoritmo para compressão com perdas. É basicamente associado com “MPEG-4 Audio Layer”, arquivos com extensão .m4a são a camada de áudio de filmes MPEG-4. Destina-se a ultrapassar o MP3 e tornar-se o novo padrão em compressão de áudio. É muito próximo do MP3 em muitos aspectos, mas introduzido para ter uma qualidade melhor em um tamanho de arquivo igual ou até menor. O formato M4A foi introduzido pela primeira vez pela Apple. O tipo de formato também é realizado como o codificador sem perdas da Apple (ALE).

Portanto, atualmente o M4A não conseguiu o sucesso mainstream do MP3 porque o formato de áudio ainda não é jogável. De alguma forma, é limitado apenas ao MacOS, iPod e outros produtos da Apple.

**Mp3**: O formato de áudio digital mais famoso. Foi também um dos primeiros formatos de compressão em cena e tornou-se muito popular entre os amantes da música. Seu sucesso mainstream é tão rápido que o tipo de arquivo é capaz de ser reproduzido universalmente e com quase tudo, hardware ou software. De um modo geral, o M4A produzirá melhor qualidade de som, mas muitos argumentam que, seja verdade ou não, a diferença de som não é distinguível, e seria uma perda de tempo tentar converter arquivos MP3 em arquivos M4A. Eventualmente, a conversão apenas fará com que você perca a qualidade do som original.

## Especificação do formato de arquivo M4A

Os arquivos M4A consistem em pedaços consecutivos. Cada pedaço tem um cabeçalho de 8 bytes e é subdividido como:
- Tamanho do bloco de 4 bytes (big-endian, byte alto primeiro)
- tipo de bloco de 4 bytes - uma das assinaturas pré-definidas: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

O primeiro pedaço será do tipo "ftype" e possui um subtipo no deslocamento 8. O M4A definido pelo subtipo que deve ser "M4A_", para o subtipo M4B deve ser "M4B_" e para o subtipo M4P deve ser "M4P_".

Iterando pedaços, até que pedaço de tipo desconhecido seja detectado, ele irá compor o arquivo M4A (MPEG-4 Audio).

## Referências ##

* [MPEG-4 Parte 14 - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemplo de formato e recuperação de áudio MPEG-4 Parte 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

