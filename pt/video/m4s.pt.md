{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo M4S - O que é um arquivo M4S?",
  "description":"Saiba mais sobre o formato de arquivo M4S e APIs que podem criar e abrir arquivos M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## O que é um arquivo M4S?

Um arquivo M4S é um pequeno segmento de um vídeo que é transmitido pela Internet usando a técnica de streaming **MPEG-DASH**. Ele contém um segmento de vídeo na forma de dados binários. O aplicativo receptor (geralmente um navegador da Web ou reprodutores de mídia) reproduz esses segmentos na ordem em que são recebidos. O primeiro segmento M4S é identificado pelos dados de inicialização que ele contém. Em **resumo**, os arquivos M4S são pequenos segmentos de mídia individuais de um arquivo completo.

## Formato de arquivo M4S

Os arquivos M4S são baseados no formato [ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Esses pequenos segmentos de um arquivo grande podem ser baixados independentemente via HTTP. Assim, se você tiver um grande arquivo de filme [MP4](/pt/video/mp4/), ele pode ser transmitido usando a técnica MPEG-DASH (Streaming Adaptativo Dinâmico sobre HTTP) segmentando-o como arquivos de segmento M4S. Se esse arquivo de filme grande for baixado para o disco como M4S, vários arquivos M4S serão baixados. Se todos esses segmentos .m4s forem concatenados, um arquivo reproduzível completo será produzido. Os media players não podem reproduzir o arquivo a menos que o primeiro segmento de inicialização também esteja disponível com o arquivo.

## Sobre o streaming MPEG-DASH

O MPEG-DASH usa a técnica de transmissão de taxa de bits adaptável que possibilita transmitir conteúdo de mídia de alta qualidade pela Internet. Isso é feito dividindo o conteúdo em uma sequência de pequenos segmentos que são transmitidos por HTTP. Grandes arquivos de mídia, como filmes, podcasts ou transmissão ao vivo de um evento esportivo, podem ser transmitidos dessa maneira. Esses segmentos são codificados em diferentes taxas de bits. Os players de mídia habilitados para MPEG-DASH selecionam automaticamente o segmento com a taxa de bits mais alta usando um algoritmo de adaptação de taxa de bits. Isso evita a paralisação ou re-buffering de eventos na reprodução.

### API de código aberto para arquivos M4S

Existem APIs de código aberto disponíveis que podem ser usadas para ler e converter arquivos M4S.

* [libdash](https://github.com/bitmovin/libdash) - API .NET para arquivos M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - cliente Javascript para arquivo M4S
* [Biblioteca Go para criar arquivos Dash](https://github.com/zencoder/go-dash)

### API de código aberto para converter M4S para MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referências ###

* [formato ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Streaming dinâmico adaptativo sobre HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

