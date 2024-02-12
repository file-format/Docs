{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE-bestand - Gaussiaans kubusbestand - Wat is een .cube-bestand en hoe u het kunt openen?",
  "description" : "Leer meer over het Gaussiaanse kubusbestand en hoe u het kunt openen.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-nl-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Wat is een CUBE-bestand?

CUBE-bestandsindeling, ook bekend als Gaussian Cube-bestand (.cube), wordt in de computationele chemie gebruikt voor het opslaan van moleculaire gegevens, met name informatie over de elektronendichtheid die voortkomt uit kwantumchemische berekeningen. Dit formaat wordt vaak geassocieerd met het **Gaussiaanse softwarepakket**, dat veel wordt gebruikt voor het uitvoeren van ab initio elektronische structuurberekeningen.

Gaussiaanse kubusbestanden slaan driedimensionale gegevens op, die doorgaans de elektronendichtheid of andere eigenschappen van moleculen vertegenwoordigen, verkregen door middel van kwantumchemische berekeningen. Het bestand bevat een koptekstgedeelte met metagegevens (zoals oorsprong, aantal gegevenspunten langs elke as en afstand), gevolgd door een raster van numerieke waarden die de betreffende eigenschap vertegenwoordigen (bijvoorbeeld elektronendichtheid) op elk rasterpunt in de ruimte.

Gaussiaans kubusbestand (.cube) is een tekstbestand met een specifieke structuur. De kop bevat informatie over het moleculaire systeem en het gegevensraster, en de gegevenswaarden zijn gerangschikt in een driedimensionaal rasterformaat. Gaussiaanse kubusbestanden worden vaak gebruikt om moleculaire eigenschappen te visualiseren met behulp van moleculaire visualisatiesoftware. Programma's zoals **VMD (Visual Molecular Dynamics)** of **PyMOL** kunnen Gaussiaanse kubusbestanden lezen om moleculaire oppervlakken, elektronendichtheid of andere berekende eigenschappen weer te geven.

## Vereenvoudigd voorbeeld van een Gauss-kubusbestand:

```
Cubefile-voorbeeld
Gegenereerd door Gaussiaans
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (gegevenswaarden voor elektronendichtheid op elk roosterpunt)
```

## Over Gaussiaans

Gaussian is een pakket softwaretoepassingen voor de kwantumchemie en computationele chemie. De primaire focus van Gaussian ligt op ab initio kwantumchemische methoden, die zeer nauwkeurige maar computationeel intensieve benaderingen zijn voor het bestuderen van de elektronische structuur van moleculen. De software wordt veel gebruikt in onderzoeks- en academische omgevingen voor verschillende toepassingen, waaronder het voorspellen van moleculaire eigenschappen, het bestuderen van reactiemechanismen en het verkennen van moleculaire structuren.

## Over NWChem

NWChem is open-source computationele chemiesoftware ontworpen voor hoogwaardige kwantumchemiesimulaties. Het maakt gebruik van ab initio-methoden zoals Hartree-Fock en dichtheidsfunctionaaltheorie, ondersteunt parallelle berekeningen voor efficiënte berekeningen op clusters, en vindt toepassingen op diverse wetenschappelijke gebieden, waaronder computationele chemie, biochemie en materiaalkunde. NWChem staat bekend om zijn veelzijdigheid, waardoor onderzoekers verschillende chemische systemen kunnen bestuderen, en het open-source karakter stimuleert bijdragen van de gemeenschap en maatwerk.

## Over VMD

VMD, wat staat voor Visual Molecular Dynamics, is een krachtig en veelgebruikt moleculair visualisatieprogramma voor het weergeven, analyseren en animeren van moleculaire dynamica (MD) trajecten, evenals statische moleculaire structuren. Het is vooral populair op het gebied van computationele chemie, moleculaire biologie en structurele bio-informatica. VMD blinkt uit in het visualiseren van moleculaire structuren en biedt hoogwaardige 3D-weergaven van moleculen en moleculaire complexen. Het ondersteunt verschillende moleculaire bestandsformaten.

## Over PyMOL

PyMOL is een moleculair visualisatiesysteem en softwaretool dat wordt gebruikt voor driedimensionale visualisatie van moleculaire structuren. Het is vooral populair op het gebied van structurele biologie, bio-informatica en computationele chemie. PyMOL biedt hoogwaardige 3D-weergaven van moleculaire structuren, waardoor gebruikers vormen, oppervlakken en interacties van biologische macromoleculen kunnen visualiseren en onderzoeken.

## Hoe open je een CUBE-bestand?

CUBE-bestand kan worden geopend en er kan naar worden verwezen met de volgende programma's.

- **NWChem** (gratis) voor (Windows, MAC, Linux)

## Referenties
* [Gaussiaanse kubusbestandsindeling](https://paulbourke.net/dataformats/cube/)
