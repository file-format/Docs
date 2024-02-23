{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BIF-bestand - Ventana-beeldformaat voor hele dia's",
  "description":"Leer meer over de BIF-bestandsindeling en API's waarmee BIF-bestanden kunnen worden gemaakt en geopend.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-nl",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Wat is een BIF-bestand?

Een BIF-bestand is een rasterafbeeldingsbestand dat de afbeelding van het objectglaasje bevat. Het bestaat uit meerdere TIFF-afbeeldingen die door toepassingen voor diaweergave worden gecombineerd tot één samengesteld beeld. BIF-bestanden zijn gemaakt door de digitale objectglaasjesscanner van Ventana Medical Systems en voldoen volledig aan de BigTIFF-variant van de [TIFF](/image/tiff/) v 6.0-definitie.

## BIF-bestandsformaat

Een BIF-bestand wordt opgeslagen als binair afbeeldingsbestand en bestaat uit maar liefst 200.000 x 200.000 pixels. Dit kan leiden tot grote bestandsgroottes, waardoor de limiet van 4 GB wordt overschreden die wordt opgelegd door de 32-bits bestandsaanwijzers die zijn gedefinieerd door de TIF-standaard. Bij 64-bits bestandspointers wordt deze barrière qua bestandsgrootte echter overwonnen door de BigTIFF-variant van de TIFF-standaard.

### Wie gebruikt BIF-bestand?

BIF-bestanden worden door digitale diascanners gebruikt om digitale kopieën van diaspecimens te scannen en te maken. Als u patholoog bent, kunt u deze BIF-bestanden openen in toepassingen voor diaweergave. Met een hoog detailniveau en gegevens met een hoge resolutie kunt u in- en uitzoomen op een diaafbeelding om monstersecties in meer of minder details te bekijken. Het metadatabestand [XML](/web/xml/) dat in deze bestanden aanwezig is, definieert hoe de afbeeldingen moeten worden gecombineerd en welke afbeelding als miniatuur van het bestand moet worden gebruikt.

## Hoe BIF-bestand openen?

U kunt BIF-bestanden openen met:

 * OpenSlide (platformonafhankelijk)
 * ImageJ (platformonafhankelijk)
 * NetScope-viewer (Windows)

## Referenties ##

 * [Roche Digital Pathology BIF-whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

