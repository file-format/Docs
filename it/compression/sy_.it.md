{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file SY_ - File SYS compresso",
  "description":"Scopri il formato di file SY_ e le API che possono creare e aprire file SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Che cos'è un file SY_?

Un file SY_ è un file .sys compresso che viene utilizzato dai programmi di installazione del software per ridurre le dimensioni dei file di installazione inclusi nel pacchetto del programma di installazione. Ciò riduce le dimensioni complessive dell'installatore. I file SY_ possono essere espansi utilizzando l'utilità della riga di comando Microsoft Expand che espande uno o più file compressi.

## SY_ Formato file - Ulteriori informazioni

I file SY_ vengono salvati su disco come file binari compressi. Tuttavia, il loro formato di file interno non è disponibile pubblicamente. L'utilità della riga di comando Microsoft Expand può espandere i file SY_ utilizzando una delle seguenti righe di comando.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Quando espansi, i file SY_ vengono convertiti nel file [SYS](https://docs.fileformat.com/system/sys/).

I file SY_ sono simili ai file EX_ e DL_.

## Riferimenti

* [StuffIt - Di Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

