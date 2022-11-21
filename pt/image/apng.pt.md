{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo apng", "formato de arquivo apng", "o que é um arquivo apng", "arquivo", "exemplo apng", "extensão de arquivo apng", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo APNG - Arquivo gráfico de rede portátil animado",
  "description":"Saiba mais sobre o formato de arquivo APNG e APIs que podem criar e abrir arquivos APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo APNG?

Um arquivo com extensão .apng (Animated Portable Network Graphics) é um formato gráfico raster e é uma extensão não oficial do Portable Network Graphic ([PNG](/pt/image/png/) ). É composto por vários quadros (cada um de imagem PNG) que representa uma sequência de animação. Isso fornece uma visualização semelhante a um arquivo [GIF](/pt/image/gif/). Os arquivos APNG suportam imagens de 24 bits e transparência de 8 bits. APNG é compatível com arquivos GIF não animados. Os arquivos APNG usam a mesma extensão .png e podem ser abertos por aplicativos como Mozilla Firefox, Chrome com suporte a APNG, aplicativos iMessage para iOS 10.

## Breve história

* As especificações APNG foram criadas em 2004 para fornecer suporte para imagens PNG animadas
* Os decodificadores APNG foram desenvolvidos com tamanho bem menor e usando a parte de trás do decodificador PNG
* Após deliberações contínuas, uma nova imagem/apng do tipo MIME foi formulada, mantendo a extensão igual a .png em vez de .apng
* APNG foi oficialmente rejeitado pelo grupo PNG em 20 de abril de 2007 devido à sua uniformidade para imagens PNG e ao mesmo tempo ter especificações diferentes

## Formato de arquivo APNG

Os arquivos APNG são armazenados como arquivos binários no disco e usam as especificações estendidas do PNG para imagens animadas. O primeiro quadro de um arquivo APNG é um fluxo PNG normal que pode ser lido pelos decodificadores PNG para exibição. O formato de arquivo APNG segue as especificações do PNG e os dados são armazenados em segmentos chamados pedaços. No entanto, o APNG introduziu os seguintes novos pedaços:

`Animation Control Chunk (acTL)` - Indica que este arquivo é um arquivo PNG animado em vez de um arquivo PNG normal. Ele atua como um marcador e vem antes do bloco IDAT. Ele também contém o número de quadros e informações sobre os tempos para fazer o loop das animações

`Frame Control Chunk` - Ocorre no início de cada e informações de metadados, como dimensões, posição, aplicação de transparência e informações de substituição pelo quadro anterior ou seguinte, uma vez terminado.

`Frame Data Chunk` - Armazena o conteúdo do quadro e inicia com um número de seqüência. Esse número de sequência tem a mesma estrutura que o bloco IDAT da imagem padrão.

{{< figure src="../APNG.png" alt="PNG animado - formato de arquivo APNG" >}}

O APNG é compatível com o PNG, pois as especificações da lateral foram projetadas de tal forma que um aplicativo que lê um arquivo PNG deve simplesmente ignorar os pedaços que não entende. As especificações relativas à profundidade de bits, tipo de cor, compactação, filtros, métodos de entrelaçamento e informações de paleta são usadas da mesma forma que o formato PNG padrão.

## APNG vs GIF

Com o GIF já instalado e sendo usado por um longo período de tempo, você pode se perguntar como o APNG é diferente do GIF. A seguir está um conjunto de comparação entre APNG e GIF que dá uma breve ideia de ambos os formatos de arquivo.

||APNG|GIF|
---|---|---|
|Publicado|2004|1987|
|Profundidade de cor|24 bits|8 bits|
|Taxa de quadros|Ilimitado|10 quadros por segundo|
|Transparência|Completo e parcial|Completo|
|Compressão|Muito Bom|Bom|

## Referências

* [Formato de arquivo APNG](https://en.wikipedia.org/wiki/APNG)
* [Especificações oficiais do formato PNG](https://www.w3.org/TR/PNG/)

