{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo mng", "formato de arquivo mng", "o que é um arquivo mng", "arquivo", "exemplo mng", "extensão de arquivo mng", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo MNG - Formato de arquivo gráfico de rede de várias imagens",
  "description":"Saiba mais sobre o formato de arquivo MNG e APIs que podem criar e abrir arquivos MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo MNG?

Um arquivo com extensão .mng é um formato de arquivo gráfico de rede com várias imagens semelhante ao formato de imagem [PNG](/pt/image/png/), mas suporta imagens animadas. Foi desenvolvido para evitar sobrecarregar o formato PNG com recurso adicional de animações. O MNG também é semelhante aos arquivos [GIF](/pt/image/gif/), mas usa mais compactação e oferece suporte ao recurso alfa completo. O tipo de mídia MIME não oficial para arquivos MNG é video/x-mng. Os arquivos MNG podem ser abertos em aplicativos como ImageMagik e IrfanView.

## Formato de arquivo MNG

O formato de arquivo MNG é semelhante ao do PNG e usa a mesma estrutura de blocos conforme definido nas especificações do PNG. Um decodificador MNG deve ser capaz de decodificar os fluxos de dados PNG sem especificar nenhum sinalizador especial para instruções de decodificação. O MNG agrupa várias imagens em um "quadro", com algumas imagens usadas como sprite para mover de um local para outro. O mecanismo permite reutilizar dados de imagem sem retransmiti-los. As [especificações MNG](http://www.libpng.org/pub/mng/spec/) podem ser consultadas para referência do desenvolvedor.

### Assinatura MNG

O fluxo de dados MNG começa com uma assinatura de 8 bytes contendo:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Isso é semelhante ao da assinatura PNG, mas contém MNG em vez de PNG.

### Quadro MNG

Um quadro MNG consiste em uma imagem bidimensional de imagens menores. Cada pequena imagem pode ser acessada usando a combinação de índice de linha e coluna. O formato é capaz de armazenar dados tridimensionais "voxel" que são dispostos em uma série de planos bidimensionais. Cada plano é representado por um fluxo de dados PNG ou Delta-PNG. Cada fluxo de dados Delta-PNG define uma imagem como as diferenças da imagem PNG pai. Isso fornece uma maneira muito mais compacta de representar imagens subsequentes do que usar um fluxo de dados PNG completo para cada uma.

## Referências ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Formato MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

