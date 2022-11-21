{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Comprimido", "Arquivo", "Extensão", "Formato de arquivo", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo LZO",
  "description":"Saiba mais sobre o formato de arquivo LZO e APIs que podem criar e abrir arquivos LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## O que é um arquivo LZO? ##

Um arquivo com extensão .lzo é combinado com recursos de arquivamento de arquivos que podem diminuir o tamanho de todos os arquivos no arquivo compactado. Todos os arquivos compactados podem compreender um ou mais arquivos ou mesmo grupos de fichários com vários arquivos de diferentes tipos e dimensões. O tamanho de um arquivo compactado é menor em comparação com o tamanho conjunto de todos os arquivos e pastas armazenados em um arquivo compactado LZO. Todos os arquivos compactados LZO são armazenados no formato LZO e são executados explicitamente com recursos de compactação usados pelo software de compactação e descompactação de arquivos LZOP. Todas as especificações de compactação são combinadas neste programa de compactação e descompactação de arquivos originado da biblioteca de compactação de arquivos Lempel-Ziv-Oberhume. Velocidade de descompactação mais rápida e taxas de compactação desenvolvidas também são combinadas nesses arquivos LZO.

## Especificação LZO ##

Markus Franz Xaver Johannes Oberhumer desenvolveu o algoritmo "lzop" original, baseado em algoritmos anteriores de Abraham Lempel e Jacob Ziv, em 1996. Esta biblioteca implementa uma variedade de algoritmos com as seguintes características:

* Compressão mais rápida que DEFLATE
* Descompressão rápida
* Buffers adicionais necessários durante a compactação (de 8 KB ou 64 KB, dependendo do nível de compactação)
* Os buffers de origem e destino são toda a memória necessária para descompressão
* Fornece controle sobre a taxa de compressão e a velocidade de compressão

Como um algoritmo de compactação de bloco, o LZO executa a compactação sobreposta, bem como a descompactação no local. Para obter a compactação sobreposta, o tamanho do bloco de compactação e descompactação deve corresponder. O algoritmo de compressão LZO divide os dados de entrada em correspondências (um dicionário deslizante) e literais que não correspondem, dando bons resultados com dados altamente redundantes e resultados aceitáveis com dados não compactáveis, aumentando apenas os dados incompressíveis em 1/64 do original Tamanho.

## Problemas para abrir um arquivo LZO ##

A seguir estão alguns problemas que podem causar mau funcionamento do formato de arquivo LZO:
  


* O arquivo pode estar corrompido. Para resolver esse problema, baixe o arquivo novamente ou peça ao remetente para reenviar o arquivo novamente
* O segundo motivo é o arquivo infectado, neste caso, verifique o arquivo corretamente
* Links impróprios para o arquivo LZO
* Remoção da descrição do LZO
* Não há recursos de hardware suficientes
* Drivers desatualizados do equipamento
  


## Referências ##

* [LZO - Por Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

