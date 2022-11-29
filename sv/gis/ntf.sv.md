{
  "date" : "2021-07-28",
  "keywords" :[ "ntf-fil", "ntf-filformat", "vad är en ntf-fil", "fil", "ntf-exempel", "ntf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - National Transfer Format Files",
  "description":"Läs mer om NTF-filformat och API:er som kan skapa och öppna NTF-filer.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Vad är en NTF fil?
Filerna med tillägget .ntf kallas **National Transfer Format (NTF)**-filer; används mest av UK Ordnance Survey (OS); specifikt för överföring av geospatiala data. Det förvaltas av British Standards Institution. Det har blivit standardöverföringsformatet för Ordnance Survey digitala data. Storbritanniens National Grid-projektion, som är en typ av Transverse Mercator, innehåller all georefererad information för NTF-filer.

## NTF-filformat
NTF-filformatet ägs av Ordnance Survey i Storbritannien; stöds av GDB-biblioteket för import. Den nuvarande versionen av NTF-filformatet är 2.0. Detta filformat introducerades för att ta itu med en begränsning av **PCIDSK** vektorsegment som bara har ett attributfält per struktur, men det finns en mängd olika attribut som kan extraheras med vektordata. För att komma runt består NTF-filformatet som att ha två segment. Varje segment består av samma vektorer, men med olika attribut. Det första segmentet i en NTF-vektorfil innehåller vektorerna med funktionskoden som attribut. Det andra segmentet innehåller vektorerna med värdet som attribut.

### Koordinatreferenssystem
GDB-biblioteket representerar raster- och vektordata med lämpliga TM-projektionsegenskaper:

- Referenslängd: 49,0
- Referenslatitud: 2.0
- Falsk östning: 400 000
- Falsk nordning: -100 000
- Skala: 0,9996012717
- Ellipsoid: Airy 1830 (E009)
Inget stöd finns tillgängligt för uppdatering eller skrivning av NTF-filer, och DTM-filerna kan inte länkas till.

### Ogrinfo exempel
Följande exempel använder **ogrinfo** på en NTF-fil för att hämta lagernummer:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referenser

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Webmapping - Illustrerad av Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

