{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo TGZ - Arquivo Tar Gzipado",
  "description":"Saiba mais sobre o formato de arquivo TGZ e APIs que podem criar e abrir arquivos TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## O que é um arquivo TGZ?

Um arquivo com extensão .tgz é um arquivo TAR, composto por vários arquivos e pastas, que foi compactado usando o software de compactação Gnu Zip (gzip). Um arquivo [TAR](/pt/compression/tar/) geralmente combina vários arquivos em um único arquivo para backup ou distribuição pela Internet. É um arquivo descompactado até ser compactado usando o software gzip, após o que se torna o arquivo TGZ. Os arquivos TGZ, sendo arquivos compactados, ocupam menos espaço no disco e são facilmente transferíveis usando a Internet via e-mail. Alguns aplicativos que podem abrir arquivos TGZ incluem WinZip, Apple Archive Utility, 7-Zip e WinRAR. Os arquivos TGZ são usados principalmente no sistema UNIX e Linux.

## Formato de arquivo TGZ

Os arquivos TGZ são salvos como arquivos binários compactados usando o algoritmo de compactação [GZ](/pt/compression/gz/).

## Como descompactar o arquivo .tgz no Linux

No sistema operacional Linux/Unix, o comando a seguir pode ser usado para descompactar arquivos TGZ da linha de comando.

```
tar zxvf tgzCompressedFile.tgz
```

O comando acima descompacta o arquivo TGZ compactado e extrai seus arquivos do arquivo TAR para o disco.
## Referências ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

