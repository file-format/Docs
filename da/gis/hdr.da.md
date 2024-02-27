{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "HDR-fil- ESRI BIL Header-filformat",
  "description":"Hvad er en HDR fil?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr-da",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Hvad er en HDR fil?

En HDR-fil er en GIS-header-fil, der indeholder header-information for en Band interleaved by line (.BIL)-fil. Den beskriver billeddataene og har samme navn som billedfilens. En HDR-fil består af et sæt poster, som hver beskriver en bestemt egenskab ved billedet. HDR-filen beskriver layoutet og formateringen af BIL-filen til oversættelse til den virkelige verdens koordinater i kombination med en separat georeferencefil.

## HDR filformat

HDR-filer gemmes i ASCII-tekstfilformat. Den indeholder et sæt poster, hvor hver post beskriver en bestemt egenskab ved billedet. Hver HDR-fil har følgende format:

```
<keyword> <value>
```

`<keyword> ` - Det angiver den særlige attribut, der er ved at blive indstillet
`<value> ` - Det er den værdi, som attributten indstilles til

Der er ingen begrænsning på rækkefølgen af posterne i overskriften. Hver post skal dog være på en separat linje på linjen for at overholde den parsingmetode, der bruges af HDR-læsere.

## Oversigt over søgeord, der bruges i HDR-fil

|Søgeord |Acceptabel værdi |Standard|
---|---|---|
|nrows |ethvert heltal > 0| ingen
|ncols |ethvert heltal > 0| ingen
|nbånd |ethvert heltal > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|byteordre| I = Intel;M = Motorola |samme som værtsmaskine|
|layout| bil, bip, bsq| bil|
|skipbytes| ethvert heltal ≥ 0| 0
|ulxmap |ethvert reelt tal| 0|
|ulymap |ethvert reelt tal |nrows - 1|
|xdim |ethvert reelt tal| 1
|ydim |ethvert reelt tal| 1
|bandrowbytes |ethvert heltal > 0| mindste heltal ≥ (ncols x nbits) / 8|
|totalrowbytes |ethvert heltal > 0| for bil: nbånd x bandrowbytes;for bip: mindste heltal ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |ethvert heltal ≥ 0| 0|

## Referencer

* [HRD-filformat - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


