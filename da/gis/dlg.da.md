{
  "date": "2021-07-30",
  "keywords": [
"dlg fil",
"dlg filformat",
"hvad er en dlg fil",
"fil",
"dlg eksempel",
"dlg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "DLG - Shapefil Shape Index Format",
  "description": "Lær om DLG filformat og API'er, der kan oprette og åbne DLG filer.",
  "linktitle": "DLG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dl-dag"
}
},
  "lastmod": "2021-07-30"
}

## Hvad er DLG fil?
En fil med filtypenavnet .dlg indeholder Digital Line Graph, som er en kartografisk kortfunktion vist i digital vektorform, som administreres af US Geological Survey (USGS). DLG-filerne er tilgængelige i to forskellige formater:
1. **Valgfrit format**: Et brugervenligt format, der inkorporerer en 80-byte logisk registreringslængde, UTM-jordkoordinatsystemet og topologiforbindelser indeholdt i linje-, knude- og områdeelementer.
2. **Spatial Data Transfer Standard (SDTS) format**: et format, der letter overførsel af rumlige data mellem forskellige computersystemer.

## DLG filformat
DLG-filformatet er designet til USGS-kort og transmitteres i stor, mellem- og lille skala med op til ni forskellige kategorier af funktioner. DLG-filerne kommer i valgfri og Spatial Data Transfer Standard (SDTS) formater, der er topologisk strukturerede til brug i kortlægning og GIS-applikationer.
### Specifikationer for DLG-filformat
DLG-filerne er distribueret i tre forskellige skalaer:

1. **Stor skala** - svarer normalt til:
- USGS 7,5- gange 7,5 minutter
- 1:24.000 og 1:25.000 skala topografisk firkantkortserie
- 1:63.360 skala for Alaska
- Skala 1:30.000 for Puerto Rico
 
2. **Mellemskala** - afledt af USGS: 
- 30- gange 60 minutter
- Kortserie i skala 1:100.000
3. **Små skala** - afledt af USGS 1:2.000.000 snitkort over USA's National Atlas
### Datakategorier
Nine different categories of layers, or features, are available in DLG files:
1. Public Land Survey System (PLSS)
2. Grænser (BD)
3. Transport (TR)
4. Hydrografi (HY)
5. Hypsografi (HP)
6. Ikke-vegetative egenskaber (NV)
7. Opmålingskontrol og markører (SM) 
8. Menneskeskabte funktioner (MS) 
9. Vegetativ overfladedækning (SC)

DLG-filer i stor skala tilbyder alle ni lag, mens mellemskala tilbyder de fem lag af PLSS, BD, TR, HY og HP. DLG'er i lille skala tilbyder de fem lag af PLSS, BD, TR, HY og MS.

## Referencer

* [Digital linjegraf - af Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)



