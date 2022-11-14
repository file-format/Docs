{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over KIT-bestandsindeling en API's die KIT-bestanden kunnen maken en openen.",
  "title" :"KIT-bestandsindeling - CodeKit-bestand",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Wat is een KIT-bestand?

Een bestand met de extensie .kit is een HTML-bestand dat is gemaakt met de programmeertaaltoepassing [CodeKit](https://codekitapp.com/). Het bevat `imports` en `variables` naast bestaande [HTML](/nl/web/html/)-bestanden, waardoor het ideaal is voor statische sites. CodeKit compileert KIT-bestanden naar HTML die gemakkelijk kunnen worden gebruikt als statische websitebestanden.

## KIT-bestandsindeling

KIT-bestanden zijn HTML-bestanden die bovendien importen en variabelen bevatten. Deze worden opgeslagen als platte tekstbestanden en kunnen worden geopend met elke teksteditor of webbestandseditors.

### KIT-bestand geïmporteerd

Bijna elk type bestand kan in een Kit-bestand worden geïmporteerd. Hieronder volgt de importsyntaxis die wordt gebruikt om bestanden in een .kit-bestand te importeren.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Wanneer een import aan een KIT-bestand wordt toegevoegd en opgeslagen, wordt deze vervangen door de tekst van het bestand dat wordt geïmporteerd. U kunt ook @include gebruiken in plaats van @import.

### Meerdere imports in een KIT-bestand

U kunt ook meer dan één bestand tegelijk importeren door een door komma's gescheiden lijst te gebruiken:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referenties

* [Wat is Kit?](https://codekitapp.com/help/kit/)

