{
  "date" : "2021-07-29",
  "keywords" :[ "shx-fil", "shx-filformat", "vad är en shx-fil", "fil", "exempel på shx", "shx filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Shapefile Shape Index Format",
  "description":"Läs mer om SHX-filformat och API:er som kan skapa och öppna SHX-filer.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Vad är en SHX fil?
SHX-filen tillhör formindexformatet som är ett positionsindex för funktionsgeometrin för att snabbt kunna söka framåt och bakåt. SHX är en offsetfil för direktåtkomst. Det finns inga data i den här filen, bara en kopia av de första hundra byten, postnummer och offset till startbyten för den posten i shp. Observera att filen med tillägget .shx inte binder [SHP](/sv/gis/shp/) och [DBF](/sv/database/dbf/).

## SHX filformat
SHX-formatet innehåller positionsindex för funktionsgeometrin och 100-byte-huvud som liknar SHP-filen, följt av valfritt antal 8-byte poster med fast längd som innehåller följande två fält:
| Bytes | Skriv | Endianness | Användning |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | stor | Record offset (i 16-bitars ord) |
| 4–7 | int32 | stor | Rekordlängd (i 16-bitars ord) |

Detta index gör det möjligt att söka bakåt i shapefilen genom att först söka bakåt i shape index och sedan läsa postoffset. Den offseten kan användas för att söka till rätt position i SHP-filen. Du kan också söka forwards; ett godtyckligt antal poster med samma metod. Även om det är möjligt att generera komplett index tillsammans med en SHP-fil, men det kan öka chanserna att göra SHP-filen korrupt snabbt.


## Referenser

* [Shapefile - av Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


