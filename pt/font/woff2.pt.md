{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Arquivo WOFF2 - Arquivo de formato de fonte aberta da Web 2.0",
  "description": "Saiba mais sobre o que é um arquivo WOFF2 e APIs que podem criar e abrir arquivos WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-pt2"
}
},
  "lastmod": "2023-01-10"
}

## O que é um arquivo .WOFF2?

WOFF2 é um formato de arquivo de fonte que é uma versão mais compactada do Web Open Font Format (WOFF). Ele foi desenvolvido como uma forma de reduzir o tamanho do arquivo de fontes da web, permitindo que carreguem mais rápido e usem menos largura de banda. WOFF2 usa um algoritmo de compactação chamado Brotli para compactar os dados da fonte, o que pode resultar em tamanhos de arquivo significativamente menores do que fontes [WOFF](/font/woff/) equivalentes. Este formato é compatível com a maioria dos navegadores modernos, incluindo Chrome, Firefox, Safari, Opera e Edge (versão 14 em diante).

## Formato de arquivo WOFF2 – Mais informações

A estrutura interna de um arquivo de fonte WOFF2 é composta de várias partes diferentes, incluindo um cabeçalho, metadados, um diretório de tabela e os próprios dados da fonte.

 1. O cabeçalho contém informações sobre o formato geral do arquivo, incluindo o número da versão e o número de tabelas presentes no arquivo.

 1. A seção de metadados contém informações como nome da fonte, direitos autorais e outras informações relacionadas à fonte.

 1. O diretório table contém informações sobre as diferentes tabelas que compõem a fonte, incluindo sua localização no arquivo e seu comprimento.

 1. Os dados da fonte em si são divididos em diversas tabelas diferentes, cada uma contendo informações específicas sobre a fonte, como seus caracteres e seus glifos correspondentes. Essas tabelas podem incluir:

 * A tabela 'glyf' contém os contornos reais da fonte, incluindo a forma e o tamanho de cada caractere.
 * A tabela 'head' contém informações gerais sobre a fonte, como número de versão, tamanho do design e assim por diante.
 * A tabela 'hmtx' contém informações sobre as métricas da fonte, incluindo as larguras e posições dos caracteres.
 * Cada tabela é compactada e armazenada no formato de arquivo WOFF2 após a conclusão do processo de codificação.

A estrutura geral é projetada para permitir análise e decodificação rápidas, para que os navegadores da web possam carregar e exibir a fonte em um site de forma rápida e eficiente.

### Cabeçalho WOFF2
O cabeçalho WOFF é composto por uma assinatura identificadora que indica o tipo de dados incluídos no arquivo. O cabeçalho WOFF junto com seus campos é o seguinte.

|Tipo|Nome do campo|Descrição|
---|---|---|
|UInt32|assinatura |0x774F4632 'wOF2' |
|UInt32| sabor |A versão sfnt da fonte de entrada.|
|UInt32| length |Tamanho total do arquivo WOFF.|
|UInt16| numTables |Número de entradas no diretório de tabelas de fontes.|
|UInt16| reservado |Reservado; definido como zero.|
|UInt32| totalSfntSize |Tamanho total necessário para os dados de fonte descompactados, incluindo o cabeçalho sfnt, diretório e tabelas de fontes (incluindo preenchimento).|
|UInt32| totalCompressedSize Comprimento total do bloco de dados compactados.|
|UInt16| majorVersion |Versão principal do arquivo WOFF.|
|UInt16| minorVersion |Versão secundária do arquivo WOFF.|
|UInt32| metaOffset |Deslocamento para bloco de metadados, desde o início do arquivo WOFF.|
|UInt32| metaLength |Comprimento do bloco de metadados compactado.|
|UInt32| metaOrigLength |Tamanho não compactado do bloco de metadados.|
|UInt32| privOffset |Deslocamento para bloco de dados privados, desde o início do arquivo WOFF.|
|UInt32| privLength |Comprimento do bloco de dados privados.|


## Referências
 * [Formato de arquivo w3 WOFF2](https://www.w3.org/TR/WOFF2/)

