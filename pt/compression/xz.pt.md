{
  "date" : "2022-01-23",
  "keywords" :[ "arquivo xz", "formato de arquivo", "o que é um arquivo xz", "arquivo", "exemplo xz", "extensão de arquivo xz", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo XZ - Arquivo compactado XZ",
  "description":"Saiba mais sobre o formato de arquivo XZ e APIs que podem criar e abrir arquivos XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## O que é um arquivo XZ?

XZ é um formato de arquivo compactado que utiliza o algoritmo de compactação LZMA2. Ele foi projetado como um substituto para os formatos populares gzip e bzip2 e oferece várias vantagens sobre esses padrões mais antigos. Os arquivos XZ são bem suportados em muitas plataformas e podem ser descompactados de maneira rápida e fácil. Embora não sejam tão comuns quanto os arquivos [ZIP](/pt/compression/zip/) ou [RAR](/pt/compression/rar/), os arquivos XZ podem ser usados para armazenar grandes quantidades de dados sem sacrificar a qualidade da compactação. Se você precisar compactar ou descompactar arquivos grandes, vale a pena considerar a extensão do arquivo XZ.

## Formato de arquivo XZ

O arquivo XZ é gerado e salvo como arquivos binários no disco. Ele usa o algoritmo LZMA para compactar dados e pode atingir uma taxa de compactação de até 50%. Os arquivos XZ são normalmente usados para distribuições de software e arquivos de backup. Eles podem ser descompactados usando o utilitário XZ, que está incluído na maioria das distribuições Linux.

## Descompacte arquivos XZ no Linux/Unix

Para descompactar arquivos XZ, instale primeiro o pacote `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Use o comando `unxz` para extrair arquivos .xz:
```
$ unxz compressed_xz_file.xz
```

ou usando com a opção --decompress do XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referências

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

