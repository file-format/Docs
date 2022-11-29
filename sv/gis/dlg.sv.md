{
  "date" : "2021-07-30",
  "keywords" :[ "dlg-fil", "dlg-filformat", "vad är en dlg-fil", "fil", "dlg-exempel", "dlg filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Shapefile Shape Index Format",
  "description":"Läs mer om DLG-filformat och API:er som kan skapa och öppna DLG-filer.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Vad är DLG fil?
En fil med filtillägget .dlg innehåller Digital Line Graph som är en kartografisk kartfunktion som visas i digital vektorform som administreras av US Geological Survey (USGS). DLG-filerna finns i två olika format:
1. **Valfritt format**: Ett enkelt att använda format som innehåller en logisk postlängd på 80 byte, UTM-jordkoordinatsystemet och topologilänkar som ingår i linje-, nod- och områdeselement.
2. **Spatial Data Transfer Standard (SDTS) format**: ett format som underlättar överföring av rumslig data mellan olika datorsystem.

## DLG filformat
DLG-filformat är designat för USGS-kartor och sänds i stor, medelstor och liten skala med upp till nio olika kategorier av funktioner. DLG-filerna kommer i valfria och Spatial Data Transfer Standard-format (SDTS) som har topologiskt strukturerade för användning i kartläggning och GIS-applikationer.
### Specifikationer för DLG-filformat
DLG-filerna distribueras i tre olika skalor:

1. **Stor skala** - motsvarar normalt:
- USGS 7,5- med 7,5 minuter
- 1:24 000 och 1:25 000 skala topografisk fyrkantskartserie
- Skala 1:63 360 för Alaska
- Skala 1:30 000 för Puerto Rico
 

2. **Mellanskala** - härledd från USGS:

- 30- gånger 60 minuter

- Kartserie i skala 1:100 000
3. **Småskalig** - härledd från USGS 1:2 000 000 sektionskartor över National Atlas of the United States
### Datakategorier
Nio olika kategorier av lager, eller funktioner, är tillgängliga i DLG-filer:
1. Offentligt lantmäterisystem (PLSS)
2. Gränser (BD)
3. Transport (TR)
4. Hydrografi (HY)
5. Hypsografi (HP)
6. Icke-vegetativa egenskaper (NV)
7. Undersökningskontroll och markörer (SM)

8. Konstgjorda funktioner (MS)

9. Vegetativ yttäckning (SC)

Storskaliga DLG-filer erbjuder alla nio lager, medan mellanskala erbjuder fem lager av PLSS, BD, TR, HY och HP. Småskaliga DLG:er erbjuder fem lager av PLSS, BD, TR, HY och MS.

## Referenser

* [Digital linjediagram - av Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


