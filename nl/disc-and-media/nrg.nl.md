{
  "date" : "2021-08-16",
  "keywords" :[ "nrg-bestand", "nrg-bestandsindeling", "wat is een nrg-bestand", "bestand", "nrg-voorbeeld", "nrg-bestandsextensie", "extensie", "format", "nrg-voettekst", "bestand formaat van nrg", "Nero Burning Rom", "Nero AG"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over NRG-bestandsindeling en API's die NRG-bestanden kunnen maken en openen.",
  "title" :"NRG - Bestandsindeling schijfkopie",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Wat is een NRG-bestand?

Een afbeeldingsbestandsindeling die is gemaakt door het gebruik van een optische schijf, wordt beschouwd als een NRG-bestandsindeling. Deze indeling is speciaal door Nero gemaakt voor het hulpprogramma Nero Burning Rom. Voor de opslag van schijfimages wordt dit formaat geacht te worden gebruikt omdat het geschikt is voor deze specifieke bestanden. Deze bestanden kunnen de vorm hebben van een exacte kopie van een cd of dvd of kunnen meerdere bestanden bevatten die als schijf kunnen worden gemount. Andere, meer populaire bestandsindelingen zoals [ISO](/nl/compression/iso/) bestandsindelingen zijn die waarin deze bestanden kunnen worden geconverteerd naar enkele basishulpprogramma's. Meestal worden de NRG-bestanden gebruikt om back-ups of kopieën van enkele belangrijke gegevens of schijven te maken.

## NRG-bestandsindeling ##

Deze bestandsindeling is door Nero AG ontwikkeld als schijfkopie-indeling. Het had de specifieke eigenschap van het hulpprogramma Nero Burning Rom, omdat het werd ontwikkeld om schijfkopieën op te slaan. De eerste versie was gespecificeerd om waarden op te slaan als 32-bits gehele getallen. De tweede versie werd echter gelanceerd en bevatte ondersteuning voor 64-bits gehele getallen.

## Technische specificatie ##

Aan het begin van het bestand slaat dit formaat zijn gegevens niet op als koptekst. Net als een voettekst wordt deze aan het einde van het bestand toegevoegd. In de vorm van stukjes IFF wordt de informatie van de afbeelding opgeslagen. De offset van het eerste stuk kan worden verkregen door de NRG-voettekst bij de laatste 8 bytes tot 12 bytes van het bestand te lezen. In alle versies van het NRG-bestandsformaat zijn er chunks, DAOI, CD-tekst, sessie-informatiemediatype, schijfinformatie, Relo en het einde van de keten die ermee verbonden is. De bytevolgorde is big-endian en alle integerwaarden zijn niet ondertekend op het moment van opslag.

### Hoofdstukjes ###

#### Cue-blad ####

Dit cue-blad is eenvoudig beschikbaar in alle versies van het NRG-bestandsformaat. Het stuk **CUEX** betekent de blokken met aaneenschakeling van een vaste grootte en elk van deze vertegenwoordigt het cue-punt.

#### DAO-informatie ####

Deze informatie is ook aanwezig in alle versies in NRG-formaat. De brokken **DAOI** slaan de relevante specifieke informatie op in 2 delen. Het eerste deel bestaat alleen uit de sessiespecifieke gegevens. Het tweede deel herhaalt gewoon de grijze informatie met betrekking tot tracking en het is slechts één keer voor elke track.

#### CD-tekst ####

Deze is beschikbaar in de tweede versie van NRG. Het stuk **CDTX** bestaat uit de onbewerkte aaneenschakeling van het cd-tekstpakket met elk 18 bytes.

#### Uitgebreide trackinformatie ####

Deze is beschikbaar in elke versie van het bestandsformaat van NRG. Deze chunks worden gebruikt voor het opslaan van de trackinginformatie voor de track in een keer sessies. Deze gegevens worden slechts één keer herhaald in het geval van elk spoor.

#### Sessie-informatie ####

Dit is ook beschikbaar in elke versie van het bestandsformaat van NRG. De informatie van sessiebrokken moet worden gebruikt om het beeld van de sessie snel te scannen en vervolgens het aantal tracks te volgen.

#### Einde van ketting ####

De chunk of end betekent het signaal dat er nu geen chunks meer gelezen hoeven te worden en dit is ook beschikbaar in alle versies van NRG.


## Referenties ##

* [NRG - door Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


