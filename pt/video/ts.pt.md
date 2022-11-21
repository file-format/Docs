{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo TS - Arquivo de fluxo de transporte de vídeo",
  "keywords" :[ "ts", "flie", "extensão", "extensão", ".ts", "formato" ],
  "description":"Saiba mais sobre o que é um arquivo TS e APIs que podem criar e abrir arquivos TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## O que é um arquivo TS?

Um arquivo com extensão .ts é um fluxo de vídeo que armazena os dados em DVDs. Ele usa o algoritmo de compactação MPEG-2 ([.mpeg](/pt/video/mpg/)) para obter a máxima eficiência e compatibilidade em diferentes tipos de mídia, como streaming e transmissão pela Internet. O formato de arquivo TS foi criado para que possa ser reproduzido em dispositivos com conexões de internet ruins, como smart TV.

## Formato de arquivo TS - Mais informações

Os dados em um arquivo TS são semelhantes ao arquivo [MP4](/pt/video/mp4/), mas são divididos em pequenos pedaços. Cada pedaço consiste em um pequeno pedaço de vídeo, seguido por um pouco de áudio e uma legenda opcional. Um único arquivo TS consiste em muitos desses pedaços. Além de vídeo, áudio e legenda, cada bloco também inclui alguns dados adicionais para detectar erros no bloco. Devido a isso, os arquivos TS são um pouco maiores em tamanho.

### Por que usar o formato de arquivo TS?

Então, se os arquivos TS são um pouco grandes em tamanho, que vantagem oferece usá-los em vez de outros formatos de arquivo? Bem, na transmissão, os pequenos pedaços de vídeo e áudio podem ser enviados pelos meios de comunicação (com fio ou rádio) em tempo real. Os dados extras nos pedaços são usados pelo receptor para pular os pedaços propensos a erros.

Além disso, os arquivos TS são usados porque o sistema de transmissão não precisa de todo o fluxo para reproduzi-lo. A transmissão pode ser captada e utilizada em tempo real através da montagem de áudio e vídeo.

## Como reproduzir arquivos TS?

Bem, os arquivos TS podem ser abertos e reproduzidos no popular [VideoLAN VLC media player] (https://www.videolan.org/vlc/features.html) que está disponível gratuitamente para download.

## Referências ##

* [MPEG Transport Stream - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

