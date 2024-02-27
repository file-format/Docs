{
  "date": "2019-10-11",
  "keywords": [
"gml fil",
"hvad er en gml-fil",
"fil",
"gml eksempel",
"gml filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GML - Geography Markup Language File Format",
  "description": "Lær om GML-filformat og API'er, der kan oprette og åbne GML-filer.",
  "linktitle": "GML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gm-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en GML fil?

GML står for Geography Markup Language, der er baseret på XML-specifikationer udviklet af Open Geospatial Consortium (OGC). Formatet bruges til at gemme geografiske datafunktioner til udveksling mellem forskellige filformater. Det fungerer som et modelleringssprog for geografiske systemer såvel som et åbent udvekslingsformat for geografiske transaktioner på internettet.

## GML filformat ##

Som med de fleste XML-baserede grammatikker er der to dele af grammatikken – skemaet, der beskriver dokumentet, og instansdokumentet, der indeholder de faktiske data. Et GML-dokument beskrives ved hjælp af et GML-skema. Dette giver brugere og udviklere mulighed for at beskrive generiske geografiske datasæt, der indeholder punkter, linjer og polygoner. Ved hjælp af applikationsskemaer kan brugere henvise til veje, motorveje og broer i stedet for punkter, linjer og polygoner.

Det er værd at bemærke, at GML ikke bør tolkes til repræsentation af geografiske data på kort. Repræsentationen af GML-indhold er anderledes end det formål, som GML blev oprettet til. Kort sagt ligner GML XML ved, at det kun bruges til at holde det rumlige indhold, der kan bruges ved at kortlægge applikationer til visningsformål.

### Indholdsdannelse i GML ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* point

* linjer

* kurver

* overflader og

* polygoner


De fremtidige versioner af GML er planlagt til at understøtte 3D-geometri samt topologiske forhold mellem funktioner.

GML-kodning giver allerede mulighed for ret komplekse funktioner. En funktion kan for eksempel være sammensat af andre funktioner. En enkelt funktion som en lufthavn kan således være sammensat af andre funktioner såsom taxaveje, landingsbaner, bøjler og luftterminaler. Geometrien af et geografisk træk kan også være sammensat af mange geometrielementer. Et geometrisk komplekst træk kan således bestå af en blanding af geometrityper inklusive punkter, linjestrenge og polygoner.

### Eksempler ###

GML 1.0 og 2.0 koder Polygoner, Points og LineString-objekter som følger:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referencer ##

* [GML-specifikationer](https://www.ogc.org/standard/gml/)

* [GML - Af Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)


