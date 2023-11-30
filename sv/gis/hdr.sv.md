{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR-fil- ESRI BIL Header File Format",
  "description":"Vad är en HDR-fil?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Vad är en HDR-fil?

En HDR-fil är en GIS-header-fil som innehåller rubrikinformation för en Band interleaved by line (.BIL)-fil. Den beskriver bilddata och har samma namn som bildfilen. En HDR-fil består av en uppsättning poster, som var och en beskriver ett visst attribut för bilden. HDR-filen beskriver layouten och formateringen av BIL-filen för översättning till verkliga koordinater i kombination med en separat georeferensfil.

## HDR-filformat

HDR-filer sparas i ASCII-textfilformat. Den innehåller en uppsättning poster där varje post beskriver ett speciellt attribut för bilden. Varje HDR-fil har följande format:

```
<keyword> <value>
```

`<keyword> ` - Det indikerar det specifika attributet som ställs in
`<value> ` - Det är värdet som attributet sätts till

Det finns ingen begränsning på ordningen på posterna i rubriken. Varje post måste dock finnas på en separat rad på raden för att följa den analysmetod som används av HDR-läsare.

## Sammanfattning av nyckelord som används i HDR-fil

|Sökord |Acceptabelt värde |Standard|
---|---|---|
|nrows |något heltal > 0| ingen
|ncols |valfritt heltal > 0| ingen
|nbands |valfritt heltal > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |samma som värddator|
|layout| bil, bip, bsq| bil|
|hopp över bytes| vilket heltal som helst ≥ 0| 0
|ulxmap |valfritt reellt tal| 0|
|ulymap |valfritt reellt tal |nrows - 1|
|xdim |valfritt reellt tal| 1
|ydim |valfritt reellt tal| 1
|bandrowbytes |valfritt heltal > 0| minsta heltal ≥ (ncols x nbits) / 8|
|totalrowbytes |alla heltal > 0| för bil: nband x bandrowbytes;för bip: minsta heltal ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |alla heltal ≥ 0| 0|

## Referenser

* [HRD-filformat - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

