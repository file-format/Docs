{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo lz4", "formato de arquivo lz4", "o que é um arquivo lz4", "arquivo", "exemplo lz4", "extensão de arquivo lz4","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - Formato de arquivo compactado LZ4",
  "description":"Saiba mais sobre o formato de arquivo LBR e APIs que podem criar e abrir arquivos LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## O que é um arquivo LZ4?

Um arquivo com extensão .lz4 é um arquivo compactado criado com aplicativos/utilitários que suportam compactação [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). O algoritmo LZ4 se concentra no equilíbrio entre velocidade e taxa de compressão. Os arquivos compactados LZ4 podem ser criados usando o utilitário de linha de comando LZ4 e podem ser descompactados usando o mesmo.

## Formato de arquivo LZ4

O formato de arquivo LZ4, baseado no algoritmo de compressão LZ4, é independente do tipo de CPU, sistema operacional, sistema de arquivos e conjunto de caracteres. É adequado para compactação de arquivos e compactação de streaming usando o algoritmo LZ4. A implementação inicial do formato LZ4 foi realizada na linguagem [C](/pt/programming/c/) por Yann Collet em 2011 e está disponível para referência do desenvolvedor no [Github](https://github.com/lz4/lz4) .

### Formato de quadro LZ4

A estrutura geral do formato de arquivo LZ4 é mostrada abaixo.

|MagicNb|F. Descritor| Bloquear|(...)|EndMark |C. Soma de verificação|
---|---|---|---|---|---|
|4 bytes| 3-15 bytes||| 4 bytes| 0-4 bytes|

#### Número mágico

4 Bytes, formato Little endian. Valor: 0x184D2204

#### Descritor de quadro

O descritor de quadro consiste em 3 t0 15 bytes e é a parte mais importante das especificações. Juntos, os campos Magic_Number e Frame_Descriptor são referidos como LZ4 Frame Header, e seu tamanho varia entre 7 e 19 bytes. É como mostrado abaixo.

|FLG| BD| (Tamanho do conteúdo)| (ID do dicionário)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 bytes| 0 - 4 bytes| 1 byte|

#### Blocos de dados

Cada bloco de dados segue a seguinte ordem.

|Tamanho do bloco| dados| (Bloquear soma de verificação)|
---|---|---|
|4 bytes| |0 - 4 bytes|

#### EndMark

O fluxo de blocos termina quando o último bloco de dados é seguido pelo valor de 32 bits 0x00000000.

#### Soma de verificação de conteúdo

O Content_Checksum verifica a validade do conteúdo que está sendo decodificado corretamente e é realizado usando o resultado do algoritmo xxHash-32. Ele valida os resultados da transmissão bem-sucedida de todos os blocos na ordem correta e sem nenhum erro.

## Referências

* [Formato de quadro LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algoritmo de compressão LZ4 - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

