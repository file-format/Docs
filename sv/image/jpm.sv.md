{
  "date" : "2019-11-25",
  "keywords" :[ "jpm-fil", "jpm-filformat", "vad är en jpm-fil", "fil", "jpm-exempel", "jpm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - JPEG 2000 sammansatt filformat",
  "description":"Läs mer om JPM-filformat och API:er som kan skapa och öppna JPM-filer.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## Vad är JPM fil?

JPM hänvisar till JPEG 2000 bildkodningssystem del 6 som används för dokumentavbildning. Den är baserad på Mixed Raster Content Standard (ISO/IEC 16485) och innehåller skiktade stillbilder som använder JPEG 2000 och andra kodningar. Förutom sina egna specifikationer ärver JPM-filformatet funktioner från sitt överordnade, dvs filformatet [jp2](/sv/image/jp2/).

## JPM filformat

JPM-filformatet definieras av [ISO/IEC 15444-6:2003](https://www.iso.org/standard/61124.html) -- JPEG 2000-bilden kodningssystem -- Del 6: Sammansatt bildfilformat. En sammansatt bild kan innehålla skannade bilder, syntetiska bilder eller båda, vilket kräver en blandning av kontinuerlig ton och tvånivåkomprimeringsmetoder. JPM-filformatet definierar en kompositionsmodell som beskriver metoden för att kombinera flera bilder för att generera en sammansatt bild med hjälp av multi-layer Mixed Raster Content (MRC) avbildningsmodell, definierad i ITU-T T.44 | ISO/IEC 16485.

### JPM-specifikationer
JPM-filformatstandarden anger att den ska vara en binär behållare för att representera en sammansatt bild med vilken flera bilder kan kombineras till en enda bild. Den ställer in mekanismen för att gruppera flera bilder i en hierarki av layoutobjekt, sidor och sidsamlingar för att lagra JPEG 2000 och andra komprimerade bilddataformat. Formatet inkluderar mekanismen för att införliva metadata (ofta kallad strukturell metadata i digitala biblioteksprojekt).

## Referenser

* [ITU-T Rec. T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](https://www.iso.org/standard/61124.html)
* [Wikipedia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

