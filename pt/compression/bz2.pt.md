{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo bz2", "formato de arquivo bz2", "o que é um arquivo bz2", "arquivo", "exemplo bz2", "extensão de arquivo bz2", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Formato de arquivo compactado",
  "description":"Saiba saber o que é um arquivo BZ2 e APIs que podem criar e abrir arquivos BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## O que é um arquivo BZ2?

BZ2 são arquivos compactados gerados usando o método de compactação de código aberto [BZIP2](http://www.bzip.org/), principalmente no sistema UNIX ou Linux. Ele é usado para compactação de um único arquivo e não se destina ao arquivamento de vários arquivos. Isso contrasta com o formato de arquivo TAR nas mesmas plataformas que arquiva vários arquivos em um único arquivo, mas sem compactação. Arquivos compactados como BZ2 podem ser descompactados com aplicativos como [WinZip](https://www.winzip.com/win/en/). O BZIP2 usa o algoritmo de compactação Run-Length Encoding (RLE) ou [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) para atingir altos níveis de compactação.

## Formato de arquivo BZ2

Não há especificações formais disponíveis para este formato de arquivo. No entanto, [especificações de engenharia reversa] não oficiais (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) mostram que um fluxo .bz2 consiste em um cabeçalho de 4 bytes que é seguido por zero ou mais blocos compactados. Ele é imediatamente seguido por um marcador de fim de fluxo contendo um CRC de 32 bits para todo o fluxo de texto simples processado. Não há preenchimento entre os blocos compactados e todos os blocos são alinhados por bits.

## Descompactar/extrair arquivo BZ2

Você pode descompactar um arquivo BZ2 no Windows e Mac OS usando software como o WinZip. No linux, o seguinte comando no terminal.

```
bzip2 -d filename.bz2
```

## Referências

* [Especificações do formato BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

