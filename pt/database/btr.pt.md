{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Banco de dados Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo BTR e APIs que podem criar e abrir arquivos BTR.",
  "title" :"BTR - Arquivo de banco de dados Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## O que é um arquivo BTR?

Um arquivo com extensão .btr é um arquivo de banco de dados criado pelo aplicativo de banco de dados transacional [Btrieve](https://www.actian.com/). Ao contrário dos sistemas de gerenciamento de banco de dados relacional (RBMS), o Btrieve é baseado no Indexed Sequential Access Method (ISAM), que é uma maneira de armazenar dados para recuperação rápida. O arquivo BTR armazena uma coleção de registros e é usado para gerar relatórios conforme os requisitos. Os arquivos BTR podem ser abertos usando o Pervasive Btrieve Database Manager, o Pervasive PSQL Maintenance Utility e o Legend Software BTRIEVE Viewer.

## Estrutura do arquivo BTR - Mais informações

A estrutura de dados interna e o alinhamento de cada byte na estrutura de um arquivo BTR não estão disponíveis publicamente. No entanto, Btrieve
fornece a [API Btrieve](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) que pode ser usada para ler as informações dos arquivos BTR. É compatível com as seguintes linguagens de programação e ambientes de desenvolvimento.

* Embarcador C/C++
* Embarcador Delphi
* GNU C/C++
* Micro Focus COBOL
*Microsoft Visual Basic
*MicrosoftVisualC++
* Watcom C/C++

A recuperação de dados de um arquivo BTR depende do arquivo DDF associado a ele. Sem o DDF, não será fácil recuperar as informações desse arquivo.

## Referências

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Introdução às APIs do Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

