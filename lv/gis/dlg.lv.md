{
  "date": "2021-07-30",
  "keywords": [
"dlg failu",
"dlg faila formātā",
"kas ir dlg fails",
"failu",
"dlg piemērs",
"dlg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "DLG — Shapefile formas indeksa formāts",
  "description": "Uzziniet par DLG failu formātu un API, kas var izveidot un atvērt DLG failus.",
  "linktitle": "DLG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dl-lvg"
}
},
  "lastmod": "2021-07-30"
}

## Kas ir DLG fails?
Fails ar paplašinājumu .dlg satur digitālo līniju diagrammu, kas ir kartogrāfiskās kartes līdzeklis, kas parādīts digitālā vektora formā un ko pārvalda ASV Ģeoloģijas dienests (USGS). DLG faili ir pieejami divos dažādos formātos:
1. **Izvēles formāts**: vienkārši lietojams formāts, kas ietver 80 baitu loģiskā ieraksta garumu, UTM zemes koordinātu sistēmu un topoloģijas saites, kas ietvertas līnijas, mezgla un apgabala elementos.
2. **Spatial Data Transfer Standard (SDTS) formāts**: formāts, kas atvieglo telpisko datu pārsūtīšanu starp dažādām datorsistēmām.

## DLG faila formāts
DLG failu formāts ir paredzēts USGS kartēm un tiek pārraidīts lielā, vidējā un mazā mērogā ar līdz pat deviņām dažādu kategoriju funkcijām. DLG faili ir pieejami neobligātos un telpisko datu pārsūtīšanas standarta (SDTS) formātos, kas ir topoloģiski strukturēti izmantošanai kartēšanas un ĢIS lietojumprogrammās.
### DLG faila formāta specifikācijas
DLG faili tiek izplatīti trīs dažādos mērogos:

1. **Lielā mērogā** — parasti atbilst:
- USGS 7,5 reiz 7,5 minūtes
- 1:24 000 un 1:25 000 mēroga topogrāfisko četrstūra karšu sērija
- 1:63 360 mērogs Aļaskai
- 1:30 000 mērogs Puertoriko
 
2. **Starpposma skala** — iegūta no USGS: 
- 30 līdz 60 minūtes
- 1:100 000 mēroga karšu sērija
3. **Maza mēroga** — iegūts no ASV Nacionālā atlanta USGS 1:2 000 000 mēroga sekciju kartēm
### Datu kategorijas
Nine different categories of layers, or features, are available in DLG files:
1. Valsts mērīšanas sistēma (PLSS)
2. Robežas (BD)
3. Transports (TR)
4. Hidrogrāfija (HY)
5. Hipsogrāfija (HP)
6. Neveģetatīvās pazīmes (NV)
7. Aptaujas vadība un marķieri (SM) 
8. Cilvēka radītas funkcijas (MS) 
9. Veģetatīvās virsmas segums (SC)

Liela mēroga DLG faili piedāvā visus deviņus slāņus, savukārt vidēja mēroga faili piedāvā piecus PLSS, BD, TR, HY un HP slāņus. Maza mēroga DLG piedāvā piecus PLSS, BD, TR, HY un MS slāņus.

## Atsauces

* [Digitālā līniju diagramma — Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)



