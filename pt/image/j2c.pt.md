{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo j2c", "formato de arquivo j2c", "o que é um arquivo j2c", "arquivo", "exemplo j2c", "extensão de arquivo j2c", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Saiba mais sobre o formato de arquivo J2C e APIs que podem criar e abrir arquivos J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## O que é um arquivo J2C?

Um arquivo com extensão .j2c é uma variante do formato de arquivo JPEG e é compactado com a compactação wavelet. Possui sistema de marcadores e segmentos quase idêntico ao formato de arquivo JPEG 2000. O formato de arquivo J2C é definido na Parte 1 do suporte JPEG 2000 que suporta compactação com e sem perdas. O codestream JPEG 2000 foi projetado para ser incorporado em [JP2](/pt/image/jp2/) ou outro formato de arquivo, embora possa aparecer em um arquivo por si só. Um arquivo J2C pode ser aberto usando Adobe Photoshop 2020, Adobe Illustrator 2020 e Corel Paintshop Pro.

## Formato de arquivo J2C

O formato de arquivo J2C é o mesmo do JPEG 2000, que geralmente é salvo como .jp2 e .jpc. Isso faz com que os arquivos J2C sigam a mesma abordagem de codificação de metadados no formato XML, onde o Padrão 12234-1 é usado como referência entre as tags Exif e os componentes XML. Ele é aprimorado ainda mais pela extensão JPEG 2000 part-2 que combina o mecanismo de animação e as configurações de fluxo de código em uma única imagem. Esses arquivos de formato de arquivo estendido são salvos como [.jpx](/pt/image/jpx/).

### Layout de um arquivo JPEG2000

O JPEG2000 suporta uma variedade de aplicativos baseados na conformidade para formatos de arquivo extensíveis. Embora o tipo mais simples possa conter uma única imagem, os tipos mais complexos podem incluir uma série de imagens, empilhadas umas sobre as outras ou sequenciadas com base no tempo.

#### Caixa JP2
É o bloco de construção de nível superior do formato de arquivo JP2 e contém campos de tipo e comprimento no cabeçalho e uma seção de dados. O tipo mais notável de caixa é a caixa de fluxo de código contígua. Esta caixa armazena em sua seção de dados o codestream JPEG2000.

#### JPEG2000 CodeStream

O JPEG2000 CodeStream é uma sequência de bytes necessária para decodificar a imagem compactada JPEG2000. Caso o arquivo não tenha nada além desse fluxo de código, ele é chamado de arquivo de fluxo de código bruto. Normalmente, um codestream JPEG é a aplicação do algoritmo de compactação JPEG2000 em uma imagem, embora não seja a única maneira.

#### Peças de Azulejo ####

Uma imagem codificada em JPEG2000 é uma coleção de unidades de dados chamadas pacotes. Esses pacotes são mantidos no codestream dentro de grupos de pacotes chamados tile-parts. Antes de codificar uma imagem, o codificador divide a imagem em uma grade retangular de blocos, chamada de blocos, onde cada bloco é codificado separadamente, independentemente de outros blocos.

{{< figure src="../JPEG2000_Codestream.png" alt="Formato de arquivo JPEG2000" >}}

## Compressão J2C
O JPEG 2000 usa a tecnologia de compressão wavelet tornando-o rápido com base no fato de que relativamente poucos pixels são mostrados em qualquer porta de visualização ou janela em que o visualizador exibe a imagem. Isso pode ser enfatizado pelo fato de que apenas alguns megabytes de pixels aparecerão na tela para imagens de tamanho muito grande (em gigabytes). Isso ajuda a buscar e renderizar rapidamente apenas a parte dos dados da imagem necessária para preencher os pixels de exibição. Isso também requer tecnologia de descompressão de alta velocidade para acelerar o mecanismo de busca de imagens para criar as imagens necessárias em tempo real.

O J2C aproveita a descompressão rápida e busca apenas as informações necessárias para que os dados de pixel renderizem parte das imagens visíveis rapidamente nas telas. J2C é projetado principalmente para a visualização de dados e não para edição.

## Identificação J2C
Os arquivos JPEG 2000 têm bytes de assinatura `FF 4F FF 51`.

### Tipos de mímica
Tipos de Mime registrados para arquivos JPEG 2000 incluem:
* imagem/j2c
* imagem/jpx
* imagem/jpm
* vídeo/mj2

## Melhorias em relação ao padrão JPEG
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

