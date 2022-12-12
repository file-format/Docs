{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier SY_ - Fișier SYS comprimat",
  "description":"Aflați despre formatul de fișier SY_ și despre API-urile care pot crea și deschide fișiere SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Ce este un fișier SY_?

Un fișier SY_ este un fișier .sys comprimat care este utilizat de instalatorii de software pentru a reduce dimensiunea fișierelor de instalare ambalate în programul de instalare. Acest lucru reduce dimensiunea totală a instalatorului. Fișierele SY_ pot fi extinse folosind utilitarul de linie de comandă Microsoft Expand care extinde unul sau mai multe fișiere comprimate.

## SY_ Format de fișier - Mai multe informații

Fișierele SY_ sunt salvate pe disc ca fișiere binare comprimate. Cu toate acestea, formatul lor intern de fișier nu este disponibil public. Utilitarul de linie de comandă Microsoft Expand poate extinde fișierele SY_ utilizând una dintre următoarele linii de comandă.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Când sunt extinse, fișierele SY_ sunt convertite în fișierul [SYS](https://docs.fileformat.com/system/sys/).

Fișierele SY_ sunt similare cu fișierele EX_ și DL_.

## Referințe

* [StuffIt - După Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

