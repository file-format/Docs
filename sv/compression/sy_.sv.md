{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ Filformat - Komprimerad SYS-fil",
  "description":"Läs mer om SY_ filformat och API:er som kan skapa och öppna SY_ filer.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Vad är SY_ fil?

En SY_-fil är en komprimerad .sys-fil som används av programvaruinstallatörer för att minska storleken på installationsfilerna som är paketerade i installationsprogrammet. Detta minskar installationsprogrammets totala storlek. SY_-filer kan utökas med kommandoradsverktyget Microsoft Expand som expanderar en eller flera komprimerade filer.

## SY_ Filformat - Mer information

SY_-filer sparas på skivan som komprimerade binära filer. Deras interna filformat är dock inte tillgängligt offentligt. Kommandoradsverktyget Microsoft Expand kan expandera SY_-filer med en av följande kommandorader.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
När de expanderas konverteras SY_-filerna till filen [SYS](https://docs.fileformat.com/system/sys/).

SY_ filer liknar EX_ och DL_ filer.

## Referenser

* [StuffIt - av Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

