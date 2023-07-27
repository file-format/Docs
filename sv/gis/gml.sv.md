{
  "date" : "2019-10-11",
  "keywords" :[ "gml-fil", "vad är en gml-fil", "fil", "gml-exempel", "gml-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Geography Markup Language File Format",
  "description":"Läs mer om GML-filformat och API:er som kan skapa och öppna GML-filer.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en GML fil?

GML står för Geography Markup Language som är baserat på XML-specifikationer utvecklade av Open Geospatial Consortium (OGC). Formatet används för att lagra geografiska datafunktioner för utbyte mellan olika filformat. Det fungerar som ett modelleringsspråk för geografiska system såväl som ett öppet utbytesformat för geografiska transaktioner på internet.

## GML-filformat ##

Som med de flesta XML-baserade grammatiker finns det två delar i grammatiken – schemat som beskriver dokumentet och instansdokumentet som innehåller den faktiska datan. Ett GML-dokument beskrivs med ett GML-schema. Detta tillåter användare och utvecklare att beskriva generiska geografiska datamängder som innehåller punkter, linjer och polygoner. Med hjälp av applikationsscheman kan användare referera till vägar, motorvägar och broar istället för punkter, linjer och polygoner.

Det är värt att notera att GML inte ska tolkas för representation av rumsliga data på kartor. Representationen av GML-innehåll skiljer sig från syftet som GML skapades för. Kort sagt, GML liknar XML genom att det endast används för att hålla det rumsliga innehållet som kan användas genom att kartlägga applikationer för visningsändamål.

### Innehållsbildning i GML ###

GML representerar rumslig data med hjälp av funktioner som är en lista över egenskaper och geometrier. En fastighet har ett namn, typ och värdebeskrivning. Geometrier är sammansatta av grundläggande geometribyggnadsblock som:

* poäng
* linjer
* kurvor
* ytor och
* polygoner

De framtida versionerna av GML är planerade att stödja 3D-geometri såväl som topologiska samband mellan funktioner.

GML-kodning tillåter redan ganska komplexa funktioner. En funktion kan till exempel vara sammansatt av andra funktioner. En enskild funktion som en flygplats kan således bestå av andra funktioner som taxibanor, landningsbanor, hängare och flygterminaler. Geometrin för ett geografiskt särdrag kan också vara sammansatt av många geometrielement. En geometriskt komplex egenskap kan alltså bestå av en blandning av geometrityper inklusive punkter, linjesträngar och polygoner.

### Exempel ###

GML 1.0 och 2.0 kodar Polygoner, Points och LineString-objekt enligt följande:

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

## Referenser ##

* [GML-specifikationer](https://www.ogc.org/standard/gml/)
* [GML - av Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

