{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR fájl - ESRI BIL fejlécfájl formátum",
  "description":"What is an HDR file?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Mi az a HDR fájl?

A HDR-fájl egy GIS-fejlécfájl, amely egy soronkénti sáv (.BIL) fájl fejléc-információit tartalmazza. Leírja a képadatokat, és ugyanaz a neve, mint a képfájlé. A HDR-fájl egy sor bejegyzésből áll, amelyek mindegyike a kép egy adott attribútumait írja le. A HDR-fájl leírja a BIL-fájl elrendezését és formázását a valós világ koordinátáira történő fordításhoz, egy külön földrajzi hivatkozási fájllal kombinálva.

## HDR fájlformátum

A HDR fájlok ASCII szöveges fájlformátumban kerülnek mentésre. Egy sor bejegyzést tartalmaz, ahol minden bejegyzés a kép egy adott attribútumait írja le. Minden HDR-fájl a következő formátumú:

```
<keyword> <value>
```

`<keyword> ` - A beállítandó adott attribútumot jelzi
`<value> ` - Ez az az érték, amelyre az attribútumot beállítják

A fejlécben a bejegyzések sorrendje nincs korlátozva. Azonban minden bejegyzésnek a sor külön sorában kell lennie, hogy megfeleljen a HDR-olvasók által használt elemzési módszernek.

## A HDR-fájlban használt kulcsszavak összefoglalása

|Kulcsszó |Elfogadható érték |Alapértelmezett|
---|---|---|
|nrows |bármely egész > 0| egyik sem
|ncols |bármely egész > 0| egyik sem
|nbands |bármely egész > 0| 1
|nbit |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |ugyanaz, mint a gazdagép|
|elrendezés| bil, bip, bsq| bil|
|kihagyás byte| bármely egész szám ≥ 0| 0
|ulxmap |bármilyen valós szám| 0|
|ulymap |bármilyen valós szám |nrows - 1|
|xdim |bármilyen valós szám| 1
|ydim |bármely valós szám| 1
|sávbájtok |bármely egész > 0| legkisebb egész ≥ (ncols x nbits) / 8|
|összes bájt |bármely egész > 0| bil esetén: nsávok x sávszélesség; bip esetén: legkisebb egész ≥ (ncols x nbands x nbits) / 8|
|bandgapbyte |bármely egész ≥ 0| 0|

## Hivatkozások

* [HRD fájlformátum – ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

