{
  "date" : "2021-07-29",
  "keywords" :[ "shx-bestand", "shx-bestandsindeling", "wat is een shx-bestand", "bestand", "shx-voorbeeld", "shx-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Shapefile Shape Index Format",
  "description":"Meer informatie over de SHX-bestandsindeling en API's die SHX-bestanden kunnen maken en openen.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Wat is een SHX-bestand?
Het SHX-bestand behoort tot het vormindexformaat, een positionele index van de objectgeometrie om snel vooruit en achteruit te kunnen zoeken. De SHX is een offset-bestand met directe toegang. Dit bestand bevat geen gegevens, alleen een duplicaat van de eerste honderd bytes, het recordnummer en de offset naar de startbyte van dat record in de shp. Houd er rekening mee dat het bestand met de extensie .shx de [SHP](/nl/gis/shp/) en [DBF](/nl/database/dbf/) niet koppelt.

## SHX-bestandsindeling
Het SHX-formaat bevat een positionele index van de objectgeometrie en een kop van 100 bytes, vergelijkbaar met het SHP-bestand, gevolgd door een willekeurig aantal records van 8 bytes met een vaste lengte die de volgende twee velden bevatten:
| Byte | Typ | Endianheid | Gebruik |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | groot | Recordoffset (in 16-bits woorden) |
| 4–7 | int32 | groot | Recordlengte (in 16-bits woorden) |

Deze index maakt het mogelijk om achteruit te zoeken in de shapefile door eerst achteruit te zoeken in de shape-index en vervolgens de recordoffset uit te lezen. Die offset kan worden gebruikt om naar de juiste positie in het SHP-bestand te zoeken. Je kunt ook vooruit zoeken; een willekeurig aantal records met dezelfde methode. Hoewel het mogelijk is om samen met een SHP-bestand een volledige index te genereren, maar het kan de kans vergroten dat het SHP-bestand snel beschadigd raakt.


## Referenties

* [Shapefile - door Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


