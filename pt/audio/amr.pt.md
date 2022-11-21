{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "arquivo", "extensão", "formato", "o que é um arquivo amr", "música", "formato de arquivo amr", "arquivo amr","converter arquivo amr para mp3", "reproduzir arquivo amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo AMR e APIs que podem criar, converter e abrir arquivos AMR.",
  "title" :"AMR - Arquivo de codec multi-taxa adaptável",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## O que é um arquivo AMR?
O arquivo com extensão .amr é um formato de dados de áudio relevante para o codec de áudio **Adaptive Multi-Rate**; consiste num codec de voz de banda estreita multi-taxa que codifica sinais de banda estreita a uma taxa de bits de 4,75-12,2 kbit/s com voz de qualidade de tarifação a partir de 7,4 kbit/s; usa adaptação de link para selecionar uma das oito taxas de bits diferentes com base.

## Formato de arquivo AMR
O formato de arquivo AMR usa muitas técnicas de codificação, o algoritmo ACELP (Algebraic Code Excited Linear Prediction) é uma das melhores técnicas; projetado para compactar o áudio falado por humanos de maneira mais eficiente. O AMR foi definido como o codec de voz ou fala padrão pela 3GPP em 1999. O formato de arquivo AMR também é usado para armazenar o áudio falado usando o codec de áudio **Adaptive Multi-Rate** que é usado por muitos smartphones para armazenar gravações discursos.

### Estrutura de formato de arquivo
O AMR(Adaptive Multi-Rate) é um formato de áudio; amplamente utilizado em várias aplicações e dispositivos móveis, normalmente em reprodutores/gravadores de áudio ou em aplicações do tipo VoIP. A AMR pode ainda ser classificada como:

1. AMR-NB (Banda Estreita)
2. AMR-WB (banda larga)

Normalmente, AMR refere-se a AMR-NB. O formato de arquivo AMR tem a seguinte estrutura:

Cada arquivo AMR contém um cabeçalho de 6 bytes que reconhece o arquivo como um áudio AMR. Este cabeçalho é sempre definido como:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Isso geralmente é semelhante em todos os arquivos AMR-NB. Se o cabeçalho seguir um padrão, é provável que o arquivo esteja corrompido e não deva ser utilizado. o arquivo AMR consiste em um número inteiro de quadros de áudio compactados. Esses quadros compõem cada um 20ms de áudio. Cada quadro pode ser codificado usando qualquer um dos modos AMR-NB válidos (0-7, 8 SID no modo DTX). Como os quadros podem ser codificados em diferentes taxas de bits, esse método típico é chamado Adaptive Multi-Rate (AMR).
#### Modos AMR
A seguir estão os diferentes modos AMR e suas taxas de bits correspondentes:

|MODO| TAXAS DE BIT|
---|---|
|0| AMR 4.75 - Codifica a 4.75kbit/s|
|1 | AMR 5.15 - Codifica a 5,15kbit/s|
|2 | AMR 5.9 - Codifica a 5,9kbit/s|
|3 | AMR 6.7 - Codifica a 6,7kbit/s|
|4 | AMR 7.4 - Codifica a 7,4kbit/s|
|5 | AMR 7.95 - Codifica a 7.95kbit/s|
|6 | AMR 10.2 - Codifica a 10,2kbit/s|
|7 | AMR 12.2 - Codifica a 12,2kbit/s|

O tamanho do quadro dos modos AMR em bytes (incluindo o byte de cabeçalho) é dado abaixo:

|CMR |MODE |FRAME SIZE( em bytes)|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Referências ##

* [Codec de áudio multitaxa adaptável - pela Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Formato de carga útil RTP e formato de armazenamento de arquivos para codecs de áudio AMR e AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

