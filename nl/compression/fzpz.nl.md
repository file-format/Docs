{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ-bestandsindeling - Fritzing Part-bestand",
  "description":"Meer informatie over wat een FZPZ-bestand is en API's die FZPZ-bestanden kunnen maken en openen.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Wat is een FZPZ-bestand?

Een FZPZ-bestand is een component/onderdeel dat wordt gebruikt in een elektronisch circuitontwerp dat is gemaakt met de circuitprototyping- en ontwerptoepassing **Fritzing**. Het is een gecomprimeerd archief dat een [FZP](/nl/cad/fzp/)-bestand en vier [SVG](/nl/page-description-language/svg/)-afbeeldingen bevat die het algehele deel in Fritzing beschrijven. Het voordeel van het gebruik van deze bestanden is dat gebruikers hun FZPZ-bestanden met elk kunnen delen vanuit het oogpunt van herbruikbaarheid. Het delen van FZPZ-onderdelen helpt bij het integreren van circuitonderdelen om op een snelle manier grotere PCB-ontwerpen te maken.

## FZPZ-bestandsindeling - Meer informatie

FZPZ-bestanden worden op schijf opgeslagen als gecomprimeerde [ZIP](/nl/compression/zip/)-archieven. U kunt de extensie hernoemen van .fzpz naar .zip en elk standaard decompressieprogramma zoals WinZIP gebruiken om de bestanden uit het archief te extraheren.

### FZPZ-bestandsstructuurinformatie

Zoals vermeld, is een FZPZ-bestand een archiefbestand dat meerdere bestanden bevat voor de weergave van een onderdeel dat wordt gebruikt op een printplaat. De FZPZ bevat de volgende bestanden:

* `Vier SVG-bestanden` - die de breadboard-, schema-, PCB- en pictogramafbeeldingen van een onderdeel vertegenwoordigen
* `FZP-bestand` - Een XML-bestand dat informatie bevat over de eigenschappen, connectoren en bussen van het onderdeel

De bestanden worden meestal als volgt genoemd.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.bestand.svg
* svg.schema.bestand.svg

## Referenties ##

* [Nieuwe onderdelen met fzpz-extensie](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

