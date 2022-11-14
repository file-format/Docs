{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC-bestand - Google Docs-snelkoppeling",
  "description":"Meer informatie over wat een GDOC-bestand is en API's die GDOC-bestanden kunnen maken en openen.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Wat is een GDOC-bestand?

Een GDOC-bestand is een snelkoppelingsbestand dat verwijst naar een bestand op Google Drive, een cloudgebaseerde documentopslagservice. Wanneer de Google Drive-client op een computer is geïnstalleerd en er een document in wordt gemaakt, maakt de schijf een document in de online cloudopslag en schrijft de [URL](/nl/web/url/) van dit document in het GDOC-bestand in lokale Google Drive-map. Wanneer op dit snelkoppelingsbestand wordt gedubbelklikt, opent de standaardwebbrowser het document vanaf de locatie [URL](/nl/web/url/). Als dit snelkoppelingsbestand uit deze map wordt verplaatst, wordt de link naar het online document verbroken.

## GDOC-bestandsindeling - Meer informatie

GDOC-bestand bevat een snelkoppeling naar het online document geschreven in [JSON](/nl/web/json/) bestandsformaat. De browser die GDOC-bestanden opent, leest de URL-informatie en opent het gekoppelde document voor weergave, op voorwaarde dat de gebruiker is ingelogd op dit Google-account waar het document is opgeslagen. GDOC-bestanden bevatten niet de inhoud van het document.

### GDOC-bestandsvoorbeeld

GDOC-bestand kan worden geopend in een teksteditor en de inhoud ziet er als volgt uit.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Zoals te zien is, is de inhoud opgemaakt in JSON met de URL van een document en de bijbehorende document-ID.

## Referenties

* [Google Documenten opent geen gdoc- of docx-bestanden](https://support.google.com/docs/thread/8408691/google-docs-not-opening-ether-gdoc-or-docx-files?hl=nl )

