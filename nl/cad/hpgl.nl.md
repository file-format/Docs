{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Bestandsindeling", "Openen", "Lezen", "Maken", "CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over de HPGL-bestandsindeling en API's die HPGL-bestanden kunnen maken en openen.",
  "title" :"HPGL-bestandsindeling - leer van experts op het gebied van bestandsindelingen!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Wat is een HPGL-bestand?

Een HPGFL-bestand (Hewlett-Packard Graphics Language) bevat een door HP ontwikkelde instructieset voor plotterbesturing. HP plotters gebruiken dit bestand om vector- en rasterinhoud op het papier te tekenen en af te drukken.

### HPGL-opdracht

Een HPGL-opdracht bestaat uit het volgende.
* Een opdrachtgedeelte van het alfabet van twee tekens
* Een parametersectie
* Terminator-sectie

Elke parameter in het bestand moet worden gescheiden door een scheidingsteken in het geval van meerdere parameters.

### HPGL-opdrachtvoorbeeld

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Coördinatie systeem

Coördinatensystemen bestaan uit 2-dimensionale meetindicatoren om een specifieke locatie te lokaliseren. De HPGL gebruikt voor dit doel zowel het Plotter-coördinaten- als het gebruikerscoördinatensysteem.

#### Plotter Coördinatensysteem

Dit coördinatensysteem wordt gebruikt om tekeningen te plotten op basis van plotterbewegingen. Een typische XY-eenheid van minimale plotterbeweging is 0,025 mm. Het mogelijke bereik van tekeningen verandert met plottersoorten.

#### Gebruiker coördinatensysteem

Door de gebruiker gespecificeerd coördinatensysteem kan worden ingesteld met behulp van de schaal en oorsprong. Deze worden geconverteerd naar plottercoördinaten met behulp van het IP-commando en SC-commando. Plottersysteemcoördinaten worden standaard gebruikt als deze conversie niet wordt uitgevoerd.

## HPGL-bestandsindeling
HPGL-bestanden zijn in ASCII-indeling (tekstbestand) en beginnen met een paar setup-opdrachten. Dit stelt bepaalde parameters in voor de plotter voor het plotten. Een typisch HPGL-bestand ziet er als volgt uit.

|Commando|Betekenis
---|---|
|IN;|initialiseren, plotten starten|
|IP;|zet de schaalpunten (P1 en P2) op hun standaardposities|
|SP1;|selecteer pen 1|
|PU0,0;|Pen omhoog en naar het beginpunt gaan voor de volgende actie|
|PD100,0,100,100,0,100,0,0;|leg Pen neer en ga naar de volgende locaties (teken een kader rond de pagina)|
|PU50,50;|Pen omhoog en ga naar X,Y-coördinaten 50,50|
|CI25;|teken een cirkel met straal 25|
|SS;|selecteer de standaard tekenset|
|DT*,1;|zet het tekstscheidingsteken op het sterretje, en druk ze niet af (de 1, betekent "waar")|
|PU20,80;|til de pen op en ga naar 20,80|
|LBHello World*;|teken een label|

## Referenties
* [HPGL door Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [HPGL-referentiegids](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

