{
  "date" : "2021-08-09",
  "keywords" :[ "arquivo cso", "formato de arquivo cso", "o que é um arquivo cso", "arquivo", "exemplo cso", "extensão de arquivo cso", "extensão", "formato", "iso", "compactação DAX "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo CSO e APIs que podem criar e abrir arquivos CSO.",
  "title" :"CSO - Imagem de disco ISO compactada",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## O que é um arquivo CSO?

Um arquivo com a extensão .cso é um arquivo de imagem ISO compactado. O CSO é uma alternativa ao método de compactação DAX; também conhecido como CISO; foi o primeiro método para compactar os arquivos [ISO](/pt/compression/iso/) e geralmente é o método preferido para arquivar coisas do PlayStation Portable. Esse formato usa a compactação Deflate, que pode incluir até nove camadas de compactação. Softwares como Prometheus e YACC são usados para criar as imagens.

## Formato de arquivo CSO

O formato de arquivo CSO foi o primeiro método de compactação para ISO para economizar mais espaço de memória. Os aprimoramentos foram feitos de tempos em tempos para uma melhor compactação. O CSO está usando a compactação Deflate com nove níveis de predefinições, geralmente, cada nível pode lidar com blocos de 2 KiB individualmente. Enquanto os níveis mais altos de compactação podem retardar e longos tempos de carregamento em software que depende muito do streaming de disco, também os níveis mais baixos podem realizar uma compactação substancial.

### Estrutura do arquivo CSO

O formato de arquivo CSO contém um cabeçalho de 24 bytes, blocos de dados e uma tabela de índice. Little-endian é assumido para campos maiores que um byte. A arquitetura final do PlayStation Portable é fornecida abaixo.

#### Cabeçalho

| Deslocamento (bytes) | Nome | Tamanho (bytes) | Finalidade |
----------|----------|--------------|---------|
| 0x0 | Magia | 4 | Sempre CISO ou 0x4F534943 quando lido como um inteiro de 32 bits. Este campo é usado para identificar um arquivo CSO. Observe que este campo pode ser diferente para os outros derivados de CSO, por exemplo, ZSO usou o código mágico ZISO. |
| 0x4 | Tamanho do cabeçalho | 4 | Para o formato de arquivo CSO "v1" original, esse campo é ignorado e, portanto, não precisa ser preciso. No entanto, o formato "v2" e ZSO exigem que este campo seja sempre 0x18 (24 bytes). |
| 0x8 | Tamanho não comprimido | 8 | O tamanho do ISO original não compactado em bytes. |
| 0x10 | Tamanho do bloco | 4 | O tamanho de cada bloco de dados em bytes antes da compactação. Normalmente 2048 bytes, o mesmo que o tamanho de cada setor ISO 9660. |
| 0x14 | Versão | 1 | A versão do formato de arquivo em uso. Para o formato "v1", o valor pode ser 0 ou 1. Para o formato "v2", deve ser 2. Além disso, o formato ZSO requer que seja 1. Voltar para o início |
| 0x15 | Alinhamento do índice | 1 | O alinhamento de cada entrada de índice, especificado em bits. |
| 0x16 | Reservado | 2 | Este campo não é utilizado. No formato "v1", este campo é ignorado e pode conter valores arbitrários. No formato "v2", este campo deve ser zero. |

#### Tabela de índice

A tabela de índice contém várias entradas de 4 bytes, que indicam a posição de cada bloco de dados, e uma última entrada adicional que aponta para o final do arquivo.
O conteúdo de cada entrada é o seguinte:
| Bit | Comprimento | Máscara | Nome | Finalidade |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Posição | Este campo, quando deslocado para a esquerda pelo alinhamento do índice fornecido no cabeçalho, fornece a posição onde o bloco de dados começa. |
| 31 | 1 | 0x80000000 | Tipo de compressão | O formato ZSO tem semântica semelhante, apenas que 0 representa LZ4 em vez de Deflate. No formato "v2". O bloco é implicitamente considerado descompactado se o tamanho do bloco for igual ou maior que o tamanho do bloco especificado no cabeçalho do arquivo. |

#### Blocos de dados

Os blocos de dados compreendem os dados não compactados ou compactados. O tamanho de um bloco é calculado obtendo sua posição e, em seguida, subtraindo-o da posição do bloco seguinte. Se o alinhamento do índice for maior que zero, é provável que o tamanho do bloco seja maior que os dados que ele contém.


## Referências

* [CSO - pela Wikipedia](https://en.wikipedia.org/wiki/.CSO)


