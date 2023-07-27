{
  "date" : "2021-01-21",
  "keywords" :[ "ai file", "ai file format", "wat is een ai file", "file", "ai example", "ai file extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator-kunstwerkbestand",
  "description":"Meer informatie over AI-bestandsindeling en API's die AI-bestanden kunnen maken en openen.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Wat is een AI-bestand?

Een bestand met de extensie .ai is een Adobe Illustrator Artwork-bestand dat vectorafbeeldingen op één pagina bevat. het gebruikt punten om paden te creëren voor het weergeven van de afbeeldingsgegevens, waardoor het veilig is voor verlies van beeldkwaliteit als het wordt vergroot. AI-bestandsformaat is gebaseerd op het PGF-bestandsformaat dat vergelijkbaar is met AI-bestanden. Het AI-formaat wordt het meest gebruikt voor logo's en gedrukte media, en de eerste versies werden beschouwd als vergelijkbaar met die van [EPS](/nl/page-description-language/eps/)-bestanden. AI-bestanden kunnen worden geopend met Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro en CorelDraw Graphics-tools.

## AI-bestandsindeling

AI is het eigen bestandsformaat van Adobe Illustrator en gebruikt de dual-path-benadering vergelijkbaar met PGF voor het opslaan van EPS-compatibele bestanden. De [specificaties van Adobe Illustrator-bestandsindelingen](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) bieden een gedetailleerde ontwikkelaarsreferentie voor interne details van dit bestandsformaat. Alle documenten (bestanden) die door Adobe Illustrator zijn gemaakt, zijn documenten in de PostScript-taal en hebben twee hoofdonderdelen die voldoen aan de documentstructureringsconventies: een `prolog` en een `script`.

### Proloog

De proloogsectie bevat informatie die nodig is voor de interpretatie van het bestand. Een voorbeeld is het selectiekader dat alle markeringen op de pagina bevat. Het bevat ook informatie over bronnen, zoals lettertypen en proceduredefinities. Deze bronnen zijn logisch gegroepeerd in sets die procsets worden genoemd en bevatten expliciete methoden voor het initialiseren en beëindigen van hun procedures.

### Script

Grafische elementen op de pagina worden beschreven door het script. Een script bevat verwijzingen naar de operators en procedures in de proloog, samen met operanden en gegevens. De drie logische secties van een script zijn:

* Set-upvolgorde - die de bronnen initialiseert en activeert die zijn gedefinieerd in de proloog
* Volgorde van beschrijvende operatoren
* Trailer die bronnen deactiveert

Operators in het script zijn opeenvolgingen van grafische elementen die zijn geschreven in de taal die is gedefinieerd door procsets in de proloog. Deze reeksen bestaan uit verzamelingen van gegevenselementen, grafische attribuutdefinities en aanroepen van de procedures die in de processen zijn gedefinieerd.

### Objecttags

Objecttags worden gebruikt om aangepaste informatie aan een Adobe Illustrator-kunstobject toe te voegen. Tags bestaan uit een:

* Tag-ID
* Tagtype
* Gegevens

## Referenties
* [specificaties van Adobe Illustrator-bestandsindelingen](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [AI-bestandsindeling door PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

