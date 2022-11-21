{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo lzma", "formato de arquivo lzma", "o que é um arquivo lzma", "arquivo", "exemplo lzma", "extensão de arquivo lzma", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Formato de arquivo compactado LZMA",
  "description":"O que é um arquivo LZMA e APIs que podem criar e abrir arquivos LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## O que é um arquivo LZMA?

Um arquivo com extensão .lzma é um arquivo compactado criado usando o método de compactação LZMA (Lempel-Ziv-Markov chain Algorithm). Eles são encontrados/usados principalmente no sistema operacional Unix e são semelhantes a outros algoritmos de compactação, como [ZIP](/pt/compression/zip/) para minimizar o tamanho do arquivo. LZMA é um formato de arquivo legado, que está sendo ou foi substituído pelo formato .xz. O tipo MIME do formato .lzma é \`application/x-lzma'. Este formato de arquivo foi projetado por Igor Pavlov para uso no LZMA SDK.

## Formato de arquivo LZMA

O arquivo LZMA consiste em duas partes principais:

1. Cabeçalho
1. Dados compactados


### Cabeçalho LZMA

Os arquivos LZMA têm um cabeçalho de 13 bytes seguido pelos dados compactados LZMA. O cabeçalho LZMA consiste em:

* Propriedades
* Tamanho do Dicionário
* Tamanho não compactado

#### Propriedades do cabeçalho LZMA

O campo Propriedades contém três propriedades. Uma abreviação é fornecida entre parênteses, seguida do intervalo de valores da propriedade. O campo consiste em

1) o número de bits de contexto literais (lc, [0, 8]);
2) o número de bits de posição literal (lp, [0, 4]); e
3) o número de bits de posição (pb, [0, 4]).

#### Tamanho do Dicionário LZMA

Isso é armazenado como um pequeno inteiro endian de 32 bits sem sinal com valores que variam de 2^n e 2^n + 2^(n-1). LZMA Utils pode descompactar arquivos com qualquer tamanho de dicionário.

#### Tamanho não compactado
O tamanho não compactado é armazenado como um pequeno inteiro endian não assinado de 64 bits. Um valor especial de 0xFFFF_FFFF_FFFF_FFFF indica que o tamanho descompactado é desconhecido. O valor é representado pelo Marcador de Fim de Carga Útil (\*) se e somente se o Tamanho Descompactado for desconhecido.

## Referências

* [Formato de arquivo LZMA](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Algoritmo de cadeia de Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

