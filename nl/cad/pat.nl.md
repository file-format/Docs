{
  "date" : "2020-03-16",
  "keywords" :[ "PAT-bestand", "Formaat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over PAT-bestandsindeling en API's die PAT-bestanden kunnen maken en openen.",
  "title" :"PAT-bestandsindeling",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Wat is een PAT-bestand?

Een bestand met de extensie .pat is een CAD-bestand dat wordt gebruikt door AutoCAD-software. Toepassingen die PAT-bestanden kunnen openen, gebruiken het arceerpatroon dat in deze bestanden is opgeslagen en krijgen informatie over de textuur/vulling van een gebied. De patronen die erin zitten geven informatie over het uiterlijk van materiaal aan getekende objecten. PAT-bestanden kunnen worden geopend in toepassingen zoals Autodesk AutoCAD, CorelDRAW Graphics Suite en Ketron Software. PAT-bestanden kunnen worden geconverteerd naar verschillende afbeeldingsindelingen zoals JPG, PNG, BMP, enz.

## PAT-bestandsindeling

PAT-bestanden zijn geschreven in platte tekst en kunnen in elke teksteditor worden geopend. De arceringspatronen in deze bestanden zijn op vectoren gebaseerd en volgen de syntaxis die wordt beschreven in de AutoCAD-documentatie.

Alle patronen beginnen bij het punt 0,0, het patroon wordt berekend om de arceringsgrens te bedekken.

### Patroondefinitie

Alle patroondefinities bestaan uit de volgende velden:
* Een leidende '\*'
* Een naam - De naam mag geen spaties, leestekens, haakjes of schuine strepen bevatten.
* Een beschrijving

Het standaardformaat voor arceringspatronen is `<\*><name> <, beschrijving>`. De naam en de beschrijving worden gescheiden door een komma en beschrijvingen mogen de regellengte van tachtig tekens niet overschrijden. De arceringspatronen worden gedefinieerd na deze informatie.

### Voorbeelden van arceerpatronen
Hieronder volgt een voorbeeld van een vierkant patroon:
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Een ander voorbeeld dat een parallellogrampatroon laat zien, is als volgt.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referenties ##

* [Hashpatronen door Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

