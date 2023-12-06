{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier HDR- Format fișier antet ESRI BIL",
  "description":"Ce este un fișier HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Ce este un fișier HDR?

Un fișier HDR este un fișier antet GIS care conține informații de antet pentru un fișier Band interleaved by line (.BIL). Descrie datele imaginii și are același nume cu cel al fișierului imagine. Un fișier HDR constă dintr-un set de intrări, fiecare dintre acestea descriind un anumit atribut al imaginii. Fișierul HDR descrie aspectul și formatarea fișierului BIL pentru traducere în coordonatele lumii reale în combinație cu un fișier de georeferențiere separat.

## Format de fișier HDR

Fișierele HDR sunt salvate în format de fișier text ASCII. Conține un set de intrări în care fiecare intrare descrie un anumit atribut al imaginii. Fiecare fișier HDR are următorul format:

```
<keyword> <value>
```

`<keyword> ` - Indică atributul particular care este setat
`<value> ` - Este valoarea la care este setat atributul

Nu există nicio limitare în ordinea intrărilor din antet. Cu toate acestea, fiecare intrare trebuie să se afle pe o linie separată a liniei pentru a se conforma cu metoda de analiză utilizată de cititorii HDR.

## Rezumatul cuvintelor cheie utilizate în fișierul HDR

|Cuvânt cheie |Valoare acceptabilă |Implicit|
---|---|---|
|nrows |orice număr întreg > 0| nici unul
|ncols |orice număr întreg > 0| nici unul
|nbands |orice număr întreg > 0| 1
|biți |1, 4, 8, 16, 32| 8
|ordinea octetilor| I = Intel;M = Motorola |la fel ca mașina gazdă|
|aspect| bil, bip, bsq| bil|
|skipbytes| orice număr întreg ≥ 0| 0
|ulxmap |orice număr real| 0|
|ulymap |orice număr real |nrows - 1|
|xdim |orice număr real| 1
|ydim |orice număr real| 1
|bandrowbytes |orice număr întreg > 0| cel mai mic număr întreg ≥ (ncols x nbiți) / 8|
|totalrowbytes |orice număr întreg > 0| pentru bil: nbenzi x bandrowbytes;pentru bip: cel mai mic număr întreg ≥ (ncols x nbenzi x nbiți) / 8|
|bandgapbytes |orice număr întreg ≥ 0| 0|

## Referințe

* [Format fișier HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

