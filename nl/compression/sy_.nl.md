{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_-bestandsindeling - gecomprimeerd SYS-bestand",
  "description":"Meer informatie over de SY_-bestandsindeling en API's die SY_-bestanden kunnen maken en openen.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Wat is een SY_-bestand?

Een SY_-bestand is een gecomprimeerd .sys-bestand dat door software-installatieprogramma's wordt gebruikt om de installatiebestanden in het installatieprogramma te verkleinen. Dit verkleint de totale omvang van het installatieprogramma. SY_-bestanden kunnen worden uitgevouwen met behulp van het opdrachtregelprogramma Microsoft Expand waarmee een of meer gecomprimeerde bestanden worden uitgevouwen.

## SY_ Bestandsindeling - Meer informatie

SY_-bestanden worden op schijf opgeslagen als gecomprimeerde binaire bestanden. Hun interne bestandsformaat is echter niet openbaar beschikbaar. Het opdrachtregelprogramma Microsoft Expand kan SY_-bestanden uitvouwen met een van de volgende opdrachtregels.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Wanneer uitgevouwen, worden de SY_-bestanden geconverteerd naar het [SYS](https://docs.fileformat.com/system/sys/)-bestand.

SY_-bestanden lijken op EX_- en DL_-bestanden.

## Referenties

* [StuffIt - Door Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

