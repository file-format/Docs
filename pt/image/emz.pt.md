{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo emz", "formato de arquivo emz", "o que é um arquivo emz", "arquivo", "exemplo emz", "extensão de arquivo emz", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ File Format - Um arquivo Meta aprimorado compactado do Windows",
  "description":"Saiba mais sobre o formato de arquivo EMZ e APIs que podem criar e abrir arquivos EMZ.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## O que é um arquivo EMZ?

Um arquivo com extensão .emz é um contêiner compactado de Metaarquivo Avançado (arquivo [EMF](/pt/image/emf/)). Eles são compactados usando a técnica de compactação [GZIP](/pt/compression/gz/), que é o método de compactação comumente usado nos sistemas operacionais UNIX e LINUX. Desvincular ZIP (/pt/compression/zip/), o GZIP compacta o arquivo como um todo, em vez de compactar arquivos individuais. Os arquivos EMZ são menores em tamanho em comparação com os arquivos EMF e ajudam na transferência rápida durante o compartilhamento de arquivos online. Alguns dos aplicativos que podem abrir arquivos EMZ incluem Microsoft Visio 2019, Microsoft Office 2019, XnView MP e File Viewer Plus.

## Formato de arquivo EMZ

Os arquivos EMZ são [Gzip](/pt/compression/gz/) compactados e contêm [EMF](/pt/image/emf/) dentro. O Gzip usa o algoritmo DEFLATE para compactação do arquivo e é diferente na aplicação da compactação. Um arquivo EMZ pode ser descompactado usando utilitários de compactação GZip, como GNU Zip. O formato do arquivo consiste em:

* Cabeçalho do arquivo
* Cabeçalhos opcionais
* Dados compactados
* Rodapé de arquivo

O formato de arquivo GZIP [especificações versão 4.3](http://tools.ietf.org/html/rfc1952) publicado pela Internet Engineering Task Force (IETF) contém informações detalhadas sobre o formato do arquivo.

## Referências

* [RFC1952: especificação de formato de arquivo GZIP](http://tools.ietf.org/html/rfc1952), por [IETF](https://www.ietf.org/)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

