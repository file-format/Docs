{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo SY_ - Arquivo SYS compactado",
  "description":"Saiba mais sobre o formato de arquivo SY_ e APIs que podem criar e abrir arquivos SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## O que é um arquivo SY_?

Um arquivo SY_ é um arquivo .sys compactado usado por instaladores de software para reduzir o tamanho dos arquivos de instalação empacotados dentro do instalador. Isso reduz o tamanho geral do instalador. Os arquivos SY_ podem ser expandidos usando o utilitário de linha de comando Microsoft Expand que expande um ou mais arquivos compactados.

## Formato de arquivo SY_ - Mais informações

Os arquivos SY_ são salvos no disco como arquivos binários compactados. No entanto, seu formato de arquivo interno não está disponível publicamente. O utilitário de linha de comando Microsoft Expand pode expandir arquivos SY_ usando uma das seguintes linhas de comando.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Quando expandidos, os arquivos SY_ são convertidos para o arquivo [SYS](https://docs.fileformat.com/system/sys/).

Os arquivos SY_ são semelhantes aos arquivos EX_ e DL_.

## Referências

* [StuffIt - Por Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

