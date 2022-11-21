{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo j2k", "formato de arquivo j2k", "o que é um arquivo j2k", "arquivo", "exemplo j2k", "extensão de arquivo j2k", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Saiba mais sobre o formato de arquivo J2K e APIs que podem criar e abrir arquivos J2K.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## O que é um arquivo J2K?

Um arquivo **J2K** é uma imagem compactada usando a compactação wavelet em vez da compactação DCT. Este formato de arquivo é usado pelos arquivos do Joint Photographic Experts Group (JPEG) 2000. Os arquivos J2K armazenam informações de metadados sobre o arquivo de imagem em XML, diferentemente de .jpeg ou .jpg que usam o formato EXIF para essa finalidade. Os arquivos J2K suportam cores de 15 bits, transparência alfa e compactação sem perdas. Existem várias APIs comerciais para decodificar imagens JPEG 2000, como J2K-Codec. Um arquivo J2K pode ser aberto no sistema operacional Windows usando os visualizadores de imagem padrão.

## Formato de arquivo J2K ##

O formato de arquivo J2K é o mesmo do JPEG 2000, que geralmente é salvo como .jp2 e .jpc. Isso faz com que os arquivos J2K sigam a mesma abordagem de codificação de metadados no formato XML, onde o Padrão 12234-1 é usado como referência entre as tags Exif e os componentes XML. Ele é aprimorado ainda mais pela extensão JPEG 2000 part-2 que combina o mecanismo de animação e as configurações de fluxo de código em uma única imagem. Esses arquivos de formato de arquivo estendido são salvos como .jpx.

### Layout de um arquivo JPEG2000 ###

O JPEG2000 suporta uma variedade de aplicativos baseados na conformidade para formatos de arquivo extensíveis. Embora o tipo mais simples possa conter uma única imagem, os tipos mais complexos podem incluir uma série de imagens, empilhadas umas sobre as outras ou sequenciadas com base no tempo.

#### Caixa JP2 ####
É o bloco de construção de nível superior do formato de arquivo JP2 e contém campos de tipo e comprimento no cabeçalho e uma seção de dados. O tipo mais notável de caixa é a caixa de fluxo de código contígua. Esta caixa armazena em sua seção de dados o codestream JPEG2000.

#### Fluxo de código JPEG2000 ####

O JPEG2000 CodeStream é uma sequência de bytes necessária para decodificar a imagem compactada JPEG2000. Caso o arquivo não tenha nada além desse fluxo de código, ele é chamado de arquivo de fluxo de código bruto. Normalmente, um codestream JPEG é a aplicação do algoritmo de compactação JPEG2000 em uma imagem, embora não seja a única maneira.

#### Peças de Azulejo ####

Uma imagem codificada em JPEG2000 é uma coleção de unidades de dados chamadas pacotes. Esses pacotes são mantidos no codestream dentro de grupos de pacotes chamados tile-parts. Antes de codificar uma imagem, o codificador divide a imagem em uma grade retangular de blocos, chamada de blocos, onde cada bloco é codificado separadamente, independentemente de outros blocos.

{{< figure src="../JPEG2000_Codestream.png" alt="Formato de arquivo JPEG2000" >}}

## Compressão J2K ##
O JPEG 2000 usa a tecnologia de compressão wavelet tornando-o rápido com base no fato de que relativamente poucos pixels são mostrados em qualquer porta de visualização ou janela em que o visualizador exibe a imagem. Isso pode ser enfatizado pelo fato de que apenas alguns megabytes de pixels aparecerão na tela para imagens de tamanho muito grande (em gigabytes). Isso ajuda a buscar e renderizar rapidamente apenas a parte dos dados da imagem necessária para preencher os pixels de exibição. Isso também requer tecnologia de descompressão de alta velocidade para acelerar o mecanismo de busca de imagens para criar as imagens necessárias em tempo real.

O J2K aproveita a descompressão rápida e busca apenas as informações necessárias para que os dados de pixel renderizem parte das imagens visíveis rapidamente nas telas. O J2K foi projetado principalmente para visualização de dados e não para edição.

## Identificação J2K ##
Os arquivos JPEG 2000 possuem bytes de assinatura 6A 50 20 20.

### Tipos de mímica ###
Tipos de Mime registrados para arquivos JPEG 2000 incluem:
* imagem/jp2
* imagem/jpx
* imagem/jpm
* vídeo/mj2

## Melhorias em relação ao padrão JPEG ##
As melhorias em relação ao padrão JPEG incluem:
* Desempenho de compressão superior
* Representação de resolução múltipla
* Transmissão progressiva por pixel e precisão de resolução
* Escolha de compressão sem perdas ou com perdas
* Resiliência a erros, formato de arquivo flexível
* Suporte de alta faixa dinâmica
* Informações espaciais do canal lateral

## Referências ##
* [Taubman, David; Marcelino, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

