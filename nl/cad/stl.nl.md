{
  "date" : "2020-03-16",
  "keywords" :[ "STL-bestand", "Formaat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over STL-bestandsindeling en API's die STL-bestanden kunnen maken en openen.",
  "title" :"STL-bestandsindeling",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een STL-bestand?

STL, afkorting voor stereolithrografie, is een uitwisselbaar bestandsformaat dat driedimensionale oppervlaktegeometrie vertegenwoordigt. Het bestandsformaat wordt gebruikt op verschillende gebieden, zoals rapid prototyping, 3D-printen en computerondersteunde productie. Het vertegenwoordigt een oppervlak als een reeks kleine driehoeken, bekend als facetten, waarbij elk facet wordt beschreven door een loodrechte richting en drie punten die de hoekpunten van de driehoek vertegenwoordigen. Resulterende gegevens worden door applicaties gebruikt om de dwarsdoorsnede van de door de fabber te bouwen 3D-vorm te bepalen. Er is geen informatie beschikbaar in het STL-bestandsformaat voor de weergave van kleur, textuur of andere veelvoorkomende [CAD](/nl/cad/) modelattributen.

## Korte geschiedenis ##

De ontwikkeling van het STL-bestandsformaat gaat terug tot 1987. Het is ontwikkeld door 3D Systems voor gebruik in commerciële 3D-printers. Een herziene versie van het STL-bestandsformaat, bekend als STL 2.0, werd in 2009 voorgesteld met updates van het bestandsformaat.

## Specificaties bestandsindeling ##

Een STL-bestand vertegenwoordigt een oppervlaktegeometrie met behulp van facetten. De facetten definiëren het oppervlak van een 3D-object en worden uniek geïdentificeerd door een eenheidsnormaal, een lijn loodrecht op de driehoek met een lengte van 1,0, en door drie hoekpunten. Er zijn in totaal 12 getallen opgeslagen voor elk facet als Normaal en elk hoekpunt wordt gespecificeerd door drie coördinaten elk. Het StL-bestand bevat geen schaalinformatie; de coördinaten zijn in willekeurige eenheden.

De specificaties van het STL-bestandsformaat kunnen worden onderzocht vanuit de volgende twee aspecten.

### Facetten Oriëntatie ###

Oriëntatie van een facet wordt bepaald door de richting van de eenheidsnormaal en de volgorde waarin de hoekpunten worden vermeld. De oriëntatie van de facetten wordt als volgt op twee manieren gespecificeerd:

* De richting van de normaal is naar buiten
* De hoekpunten worden van buitenaf tegen de klok in weergegeven, volgens de rechterhandregel.

### Vertex naar Vertex-regel ###

Volgens deze regel deelt elke driehoek twee hoekpunten met elk van zijn aangrenzende driehoeken. Een hoekpunt van een driehoek kan dus niet aan de zijde van een andere driehoek liggen.

## Bestandsformaten ##

STL is beschikbaar in ASCII en in binaire representaties voor compact bestandsformaat.

### STL ASCII-formaat ###

De ASCII-versie van het STL-bestandsformaat is geschreven in gewone ASCII. Vanwege de grote omvang wordt het bestandsformaat echter niet geselecteerd als voorkeursformaat voor gebruik. De syntaxis van een ASCII STL-bestand is als volgt:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
De vetgedrukte woorden vertegenwoordigen trefwoorden die altijd in kleine letters moeten zijn. Cursief gedrukte symbolen zijn variabelen die moeten worden vervangen door door de gebruiker opgegeven waarden. De numerieke gegevens in de lijnen **facet normaal** en **vertex** zijn enkelvoudige precisie floats, bijvoorbeeld 1.23456E+789. Een **facet normaal** coördinaat kan een leidend minteken hebben; een **vertex**-coördinaat mag niet.

### STL binair formaat ###

Het binaire formaat gebruikt de IEEE integer en floating point numerieke representatie. Het bestandsformaat wordt als volgt weergegeven:

|Veld|Info|
---|---|
|Koptekst|80 tekens|
|Aantal driehoeken|4-byte little endian geheel getal zonder teken|
|Gegevens voor elke driehoek|12 32-bits getallen met drijvende komma|

Een meer uitgebreide weergave van het bestandsformaat is zoals hieronder weergegeven.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referenties ##

* [Het STL-formaat](http://www.fabbers.com/tech/STL_Format)
* [STL - door Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

