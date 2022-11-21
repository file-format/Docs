{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "arquivo", "extensão", "formato", "MPEG-4", "Gerenciamento de direitos digitais", "DRM", "Apple", "vídeo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Saiba mais sobre o formato de arquivo M4V e as APIs que podem criar e abrir arquivos M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## O que é um arquivo M4V?

O formato de arquivo **M4V**, desenvolvido pela Apple, é um contêiner de vídeo opcionalmente protegido com proteção de cópia Digital Rights Management (DRM) para proteger a privacidade ou a cópia. Vídeos e faixas de áudio são agrupados por arquivos de contêiner para indexar e organizar fluxos de reprodução. Além disso, os contêineres também oferecem o recurso de capítulos semelhantes aos dos DVDs. A Apple usa M4V para codificar vídeos em sua iTunes Store. Ele protege a reprodução não autorizada por meio da proteção contra cópia FairPlay da Apple, permitindo que arquivos M4V sejam reproduzidos apenas em computadores autorizados com as contas usadas para comprar o vídeo. No entanto, se a proteção DRM for removida dos arquivos M4V, esses arquivos poderão ser reproduzidos em outros players de vídeo alterando a extensão de .m4v para .mp4, razão pela qual os arquivos M4V estão associados ao MPEG-4. O M4V usa H.264 para vídeo e **[AAC](/pt/audio/aac/)** e Dolby Digital para codificação e decodificação de áudio.

## Estrutura do arquivo M4V ##

Os arquivos M4V têm blocos contínuos com cabeçalho de 8 bytes, tamanho de bloco de 4 bytes e tipo de bloco de 4 bytes em cada bloco. O primeiro pedaço é “ftype” e tem um subtipo no deslocamento 8. M4V definido pelo subtipo que deve ser "M4V_". Outros tipos de blocos são assinaturas predefinidas: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PIC”. Iterando pedaços, até que um tipo desconhecido seja detectado, compomos o arquivo M4V.

Aqui está um exame de uma amostra: Os dados binários de um arquivo m4v de amostra são inspecionados através do Hex Viewer e pode-se observar que ele começa com uma assinatura **ftyp** (hex: 66 74 79 70) no deslocamento 4, que define o QuickTime Tipo de arquivo de contêiner. O subtipo de arquivo é **M4V_** (hex: 4D 34 56 20) que aponta para o tipo de arquivo M4V (MPEG-4). O tamanho do primeiro bloco é 32 (hex: 00 00 00 20, big-endian, high byte first), tamanho localizado no deslocamento 0. No deslocamento 32 (hex: 20) está localizado o segundo bloco, que tem um tamanho de 30.322 (hex : 00 00 76 72, big-endian, primeiro byte inferior) e digite **moov** (hex: 6D 6F 6F 76). O próximo pedaço está localizado no deslocamento 32+30.322#30.354 (hex: 00 00 76 92) e tem tamanho 8 (hex: 00 00 00 08) e tipo **free** (hex: 66 72 65 65).
### Codecs usados em M4V ###

#### Codec de vídeo H.264 ####

H.264 é um padrão de compressão de vídeo que converte vídeo digital em um formato que requer menos espaço quando necessário para transmissão ou armazenamento. M4V usa H.264 para compressão de vídeo. Sua aplicação abrange desde DVD, TV, Videoconferência e streaming de vídeo pela internet. O H.264 consiste em duas partes principais: Codificador – que compacta o vídeo, Decodificador – que descompacta o vídeo compactado de volta. Na figura abaixo, os processos de codificação e decodificação são destacados e outros processos são abordados no padrão H.264.

##### Processo de codificação e decodificação de vídeo em H.264 #####

Para o fluxo de bits H.264 compactado, o codificador de vídeo conduz o processo de previsão, transformação e codificação. Ao mesmo tempo, o decodificador realiza o processo inverso de decodificação, transformação inversa e reconstrução para produzir de volta o arquivo de vídeo. O H.264 ocupa metade do tamanho do MPEG.

#### Codec de áudio ####

Advanced Audio Coding (AAC) é um codec de áudio para compressão de áudio digital com perdas e é usado em um contêiner M4V. AAC é o sucessor do formato [MP3](/pt/audio/mp3/) e alcança melhor qualidade que o MP3 com a mesma taxa de bits. O formato AAC joga fora algumas informações durante o processo de compactação, o que é menos importante. AAC é um codec baseado em bloco de taxa de bits variável (VBR) em que cada bloco decodifica para 1024 amostras de domínio de tempo.

### Referências ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

