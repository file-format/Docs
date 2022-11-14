{
  "date" : "2019-10-11",
  "keywords" :[ "mng file", "mng file format", "wat is een mng file", "file", "mng example", "mng file extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG File Format - Multiple Image Network Graphics File Format",
  "description":"Meer informatie over MNG-bestandsindeling en API's die MNG-bestanden kunnen maken en openen.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een MNG-bestand?

Een bestand met de extensie .mng is een Mutliple-image Network Graphics-bestandsindeling die vergelijkbaar is met de [PNG](/nl/image/png/) afbeeldingsindeling, maar geanimeerde afbeeldingen ondersteunt. Het is ontwikkeld om overbelasting van het PNG-formaat te voorkomen met een extra functie van animaties. MNG lijkt ook op [GIF](/nl/image/gif/)-bestanden, maar gebruikt meer compressie en ondersteunt de volledige alfafunctie. Het onofficiële MIME-mediatype voor MNG-bestanden is video/x-mng. MNG-bestanden kunnen worden geopend in toepassingen zoals ImageMagik en IrfanView.

## MNG-bestandsindeling

Het MNG-bestandsformaat is vergelijkbaar met dat van PNG en gebruikt dezelfde chunkstructuur als gedefinieerd in de PNG-specificaties. Een MNG-decoder moet de PNG-gegevensstromen kunnen decoderen zonder speciale vlaggen voor decoderingsinstructies op te geven. MNG groepeert meerdere afbeeldingen samen in een "frame", waarbij sommige afbeeldingen worden gebruikt als sprite om van de ene naar de andere locatie te gaan. Het mechanisme maakt hergebruik van beeldgegevens mogelijk zonder deze opnieuw te verzenden. Er kan worden verwezen naar de [MNG-specificaties](http://www.libpng.org/pub/mng/spec/) als referentie voor de ontwikkelaar.

### MNG-handtekening

De MNG-datastroom begint met een handtekening van 8 bytes met daarin:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Dit is vergelijkbaar met die van PNG-handtekening, maar bevat MNG in plaats van PNG.

### MNG-frame

Een MNG-frame bestaat uit een tweedimensionaal beeld van kleinere afbeeldingen. Elke kleine afbeelding is toegankelijk met behulp van de rij- en kolomindexcombinatie. Het formaat kan driedimensionale "voxel" -gegevens opslaan die zijn gerangschikt in een reeks tweedimensionale vlakken. Elk vlak wordt vertegenwoordigd door een PNG- of Delta-PNG-gegevensstroom. Elke Delta-PNG-gegevensstroom definieert een afbeelding als de verschillen met de bovenliggende PNG-afbeelding. Dit biedt een veel compactere manier om opeenvolgende afbeeldingen weer te geven dan voor elk een volledige PNG-gegevensstroom te gebruiken.

## Referenties ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG-indeling v 1.0](http://www.libpng.org/pub/mng/spec/)

