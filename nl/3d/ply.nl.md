{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "bestand", "extensie", "formaat", "3D-bestandsformaat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over PLY-bestandsindeling en API's die PLY-bestanden kunnen maken en openen.",
  "title" :"PLY - Polygoon 3D-bestandsformaat",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PLY-bestand?

PLY, Polygon File Format, staat voor 3D-bestandsindeling waarin grafische objecten worden opgeslagen die worden beschreven als een verzameling polygonen. Het doel van dit bestandsformaat was om een eenvoudig en gemakkelijk bestandstype vast te stellen dat algemeen genoeg is om bruikbaar te zijn voor een breed scala aan modellen. Het PLY-bestandsformaat wordt geleverd als ASCII- en binair formaat voor compacte opslag en voor snel opslaan en laden. Het bestandsformaat wordt gebruikt door verschillende toepassingen die ondersteuning bieden voor het lezen van 3D-bestanden.

Objecten in een PLY-indeling worden beschreven door een verzameling hoekpunten, vlakken en andere elementen, samen met eigenschappen zoals kleur en normaalrichting die aan deze elementen kunnen worden gekoppeld. Andere eigenschappen die ook bij het object kunnen worden opgeslagen, zijn onder meer:

* Oppervlakte normalen
* textuur coördinaten
* transparantie
* betrouwbaarheid van bereikgegevens
* eigenschappen voor de voor- en achterkant van een polygoon

Een object vertegenwoordigd door het PLY-formaat kan het resultaat zijn van verschillende bronnen, zoals met de hand gedigitaliseerde objecten, polygoonobjecten uit modelleringstoepassingen, afstandsgegevens, driehoeken uit marcherende kubussen, terreingegevens en radiosity-modellen.

## Korte geschiedenis

Het PLY-formaat is in de jaren negentig ontwikkeld door Greg Turk en anderen in het grafische lab van Stanford en daarom staat het ook bekend als Stanford Triangle Format. Het bestandsformaat heeft sindsdien versie 1.0 en er zijn geen verdere wijzigingen aangebracht.

## PLY-bestandsindeling

Een eenvoudig PLY-object bestaat uit een verzameling elementen voor de weergave van het object. Het bestaat uit een lijst van (x,y,z) triples van een hoekpunt en een lijst van vlakken die eigenlijk indexen zijn in de lijst van hoekpunten. Hoekpunten en vlakken zijn twee voorbeelden van elementen en het grootste deel van het PLY-bestand bestaat uit deze twee elementen. Er kunnen ook nieuwe eigenschappen worden gemaakt en aan de elementen van een object worden gekoppeld, maar deze moeten op zo'n manier worden toegevoegd dat oude programma's niet kapot gaan wanneer deze nieuwe eigenschappen worden aangetroffen. Dergelijke eigenschappen kunnen ook worden weggegooid door toepassingen te lezen. Bovendien kunnen met dit element nieuwe elementen worden gemaakt en kunnen ook eigenschappen worden gedefinieerd.

### Bestandsstructuur

De bestandsstructuur van een PLY-bestandsindeling is als volgt:

|Veld
---|
|Bestandskop
|Vertex lijst
| Gezichtenlijst
|Lijst met andere elementen

#### Voorbeeldstructuur

We zullen het volgende voorbeeld hieronder gebruiken in onze volgende bespreking voor verschillende delen van een PLY-bestandsindeling.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Bestandskoptekst

PLY-bestandsindelingskop bestaat uit ASCII-tekst voor zowel het ASCII- als het binaire formaat. Het begin en einde van de koptekst wordt geïdentificeerd door de trefwoorden laag en eindkop. Het begin van de koptekst heeft het toverwoord ply dat wordt gebruikt voor de herkenning van het PLY-bestandsformaat door lezers. De volgende regel toont het versienummer van dit bestand. Opmerkingen in een PLY-bestandsindeling beginnen met het trefwoord commentaar aan het begin van elke opmerkingsregel.

#### Element Trefwoord

Het sleutelwoord element vertelt dan wat er in het bestand staat. Het wordt gevolgd door eigenschappen voor dat specifieke elementtype waarbij voor elke eigenschap zijn eigenschapstype en volgorde is gespecificeerd, zoals hieronder weergegeven:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

In dit specifieke voorbeeld heeft het specifieke hoekpuntelement 3 eigenschappen van het type float met de opgegeven volgorde.

#### Soorten gegevenstypen

Er zijn twee soorten gegevenstypen die een eigenschap kan hebben.

`Scalair`: De scalaire gegevenstypen zijn zoals hieronder weergegeven:

|#Naam|#Type|#Aantal bytes
|char|karakter|1
|uchar|unsigned karakter|1
|kort|kort geheel getal|2
|ushort|unsigned short integer|2
|int|Geheel getal|4
|uint|unsigned Integer|4
|float|single-precision float|4
|dubbel|dubbele precisie vlotter|8

`Lijst`: Er is een speciale vorm van eigenschapsdefinities die het gegevenstype lijst gebruikt. Een voorbeeld hiervan komt uit het bovenstaande kubusbestand:

`eigenschappenlijst uchar int vertex_index`

Dit betekent dat de eigenschap "vertex_index" eerst een teken zonder teken bevat dat aangeeft hoeveel indices de eigenschap bevat, gevolgd door een lijst met zoveel gehele getallen. Elk geheel getal in deze lijst met variabele lengte is een index naar een hoekpunt.

## Referenties ##

* [PLY-bestandsindeling](http://paulbourke.net/dataformats/ply/)
* [PLY - Door Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

