{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo pkg", "formato de arquivo pkg", "o que é um arquivo pkg", "arquivo", "exemplo de pkg", "extensão de arquivo pkg", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Formato de arquivo de arquivo extensível",
  "description":"Saiba mais sobre o formato de arquivo PKG e APIs que podem criar e abrir arquivos PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## O que é um arquivo PKG?

Um arquivo com extensão .pkg é um arquivo de pacote do instalador usado para instalar software no macOS. Além dos computadores Macintosh, também é usado no iPhone. O aplicativo instalador integrado da Apple pode ser usado para instalar o conteúdo de um arquivo PKG. Um arquivo PKG é semelhante a um arquivo MSI usado no sistema operacional Windows para instalação de software. Durante a instalação, esses arquivos de pacote podem registrar mensagens que dão uma ideia de quais itens extras são instalados por este pacote.

## Formato de arquivo PKG

PKR são arquivos binários compactados para reduzir o tamanho geral do arquivo. Desde o OSX 10.5, pacotes simples com arquivos de instalação únicos foram introduzidos pela Apple. Eles são diferentes dos formatos de empacotamento anteriores que vinham como pacotes em vez de arquivos únicos. Esses pacotes agrupados continham uma hierarquia de diretórios estruturada que armazenava arquivos de uma maneira que facilitava sua recuperação por meio de algum arquivo de índice. O formato de arquivo PKG simples é na verdade um arquivo [XAR](/pt/compression/xar/) que possui:

* Cabeçalho - Define as informações de tamanho, checksum e versão
* Índice - Um documento XML que é (e deve) ser codificado como UTF-8 e é armazenado no início do arquivo, facilitando a varredura pelo arquivo para extrair um arquivo individual
* Heap - heap não estruturado de dados referenciados pelo TOC

## Referências

* [Formato de arquivo de pacote simples](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

