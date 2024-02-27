{
  "date": "2022-06-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SY_ Filformat - Komprimeret SYS-fil",
  "description": "Lær om SY_ filformat og API'er, der kan oprette og åbne SY_ filer.",
  "linktitle": "SY_",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-sy-da_"
}
},
  "lastmod": "2022-06-24"
}

## Hvad er en SY_ fil?

En SY_-fil er en komprimeret .sys-fil, der bruges af softwareinstallatører til at reducere størrelsen af installationsfilerne pakket inde i installationsprogrammet. Dette reducerer den samlede størrelse af installatøren. SY_-filer kan udvides ved hjælp af Microsoft Expand-kommandolinjeværktøjet, der udvider en eller flere komprimerede filer.

## SY_ Filformat - Flere oplysninger

SY_ filer gemmes på disken som komprimerede binære filer. Deres interne filformat er dog ikke offentligt tilgængeligt. Microsoft Expand-kommandolinjeværktøjet kan udvide SY_-filer ved hjælp af en af følgende kommandolinjer.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Når de udvides, konverteres SY_ filerne til [SYS](/system/sys/) fil.

SY_ filer ligner EX_ og DL_ filer.

## Referencer

 * [StuffIt - af Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

