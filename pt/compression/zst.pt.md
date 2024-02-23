{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo ZST - formato de arquivo compactado Zstandard",
  "description":"Aprenda sobre o formato de arquivo ZST e APIs que podem criar e abrir arquivos ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-pt",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## O que é um arquivo .ZST?

Um arquivo ZST é um arquivo compactado gerado com o algoritmo de compactação Zstandard (zstd). É um arquivo compactado criado com compactação sem perdas pelo algoritmo. Os arquivos ZST podem ser usados para compactar diferentes tipos de arquivos, como bancos de dados, sistemas de arquivos, redes e jogos. O Zstandard é governado por [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) que descreve o mecanismo geral de compactação, tipo de mídia e codificação de conteúdo.

## Formato de arquivo ZST

Os arquivos ZST são armazenados em formato de arquivo compactado em disco. O mecanismo de compactação é descrito pela RFC 8878, que torna a RFC 8478 obsoleta.

## Quadros ZST

Um arquivo ZST consiste em um ou mais quadros. Cada quadro pode ser um quadro Zstandard ou um quadro pulável. Um quadro Zstandard contém dados compactados, enquanto um quadro pulável contém metadados de usuário personalizados.

### Quadro Zstandard

Um quadro Zstandard possui a seguinte estrutura.

|Campo|Tamanho em Bytes|
---|---|
|Número_mágico |4 bytes|
|Frame_Header |2-14 bytes|
|Bloco_dados |n bytes|
|[Mais Data_Blocks] ||
|[Content_Checksum] |4 bytes|

### Quadro ignorável

Um quadro pulável permite a inserção de metadados definidos pelo usuário em um fluxo de quadros concatenados. A estrutura de um quadro ignorável é a seguinte.

|Número_mágico |Tamanho_quadro |Dados_do_usuário|
---|---|---|
|4 bytes |4 bytes |n bytes|

## Referências ##

* [Compressão padrão RFC 8878 Z](https://www.rfc-editor.org/rfc/rfc8878)


