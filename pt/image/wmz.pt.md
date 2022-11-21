{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo wmz", "formato de arquivo wmz", "o que é um arquivo wmz", "arquivo", "exemplo wmz", "extensão de arquivo wmz","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo WMZ - Meta-arquivo do Windows compactado",
  "description":"Saiba mais sobre o formato de arquivo WMZ e APIs que podem criar e abrir arquivos WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## O que é um arquivo WMZ?

Um arquivo com extensão .wmz é uma versão compactada de [WMF](/pt/image/wmf/) e é usado para armazenar meta-arquivos. É um arquivo de nível intermediário gerado por versões mais antigas de aplicativos do Microsoft Office e não é muito usado popularmente. Os arquivos WMZ são gerados ao salvar documentos no formato [HTML](/pt/web/html/). Eles também podem ser gerados durante o envio de documentos por e-mail que contenham clip-arts, equações, etc. incorporados. Os aplicativos que podem abrir arquivos WMZ incluem (mas não se limitam a) Corel Winzip e Apple Archive Utility.

## Formato de arquivo WMZ

Os arquivos WMZ são [Gzip](/pt/compression/gz/) compactados e contêm [WMF](/pt/image/WMF/) dentro. O Gzip usa o algoritmo DEFLATE para compactação do arquivo. O GZIP é diferente do formato de arquivo [ZIP](/pt/compression/zip/), pois aplica o algoritmo de compactação ao arquivo completo em vez dos arquivos individuais. O formato do arquivo consiste em:

* Cabeçalho do arquivo
* Cabeçalhos opcionais
* Dados compactados
* Rodapé de arquivo

O formato de arquivo GZIP [especificações versão 4.3](http://tools.ietf.org/html/rfc1952) publicado pela Internet Engineering Task Force (IETF) contém informações detalhadas sobre o formato do arquivo.

## Referências

* [RFC1952: especificação de formato de arquivo GZIP](http://tools.ietf.org/html/rfc1952), por [IETF](https://ietf.org)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

