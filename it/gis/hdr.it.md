{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HDR - Formato file di intestazione ESRI BIL",
  "description":"Cos'è un file HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Cos'è un file HDR?

Un file HDR è un file di intestazione GIS che contiene informazioni di intestazione per un file Band interleaved by line (.BIL). Descrive i dati dell'immagine e ha lo stesso nome di quello del file immagine. Un file HDR è composto da una serie di voci, ognuna delle quali descrive un particolare attributo dell'immagine. Il file HDR descrive il layout e la formattazione del file BIL per la traduzione in coordinate del mondo reale in combinazione con un file di georeferenziazione separato.

## Formato file HDR

I file HDR vengono salvati in formato file di testo ASCII. Contiene una serie di voci in cui ciascuna voce descrive un particolare attributo dell'immagine. Ogni file HDR ha il seguente formato:

```
<keyword> <value>
```

`<keyword> ` - Indica il particolare attributo che viene impostato
`<value> ` - È il valore su cui viene impostato l'attributo

Non vi è alcuna limitazione all'ordine delle voci nell'intestazione. Tuttavia, ciascuna voce deve trovarsi su una riga separata della riga per conformarsi al metodo di analisi utilizzato dai lettori HDR.

## Riepilogo delle parole chiave utilizzate nel file HDR

|Parola chiave |Valore accettabile |Predefinito|
---|---|---|
|nrows |qualsiasi numero intero > 0| nessuno
|ncols |qualsiasi intero > 0| nessuno
|nbands |qualsiasi intero > 0| 1
|nbit |1, 4, 8, 16, 32| 8
|ordinebyte| I = Intel;M = Motorola |uguale alla macchina host|
|disposizione| bil, bip, bsq| bil|
|skipbytes| qualsiasi intero ≥ 0| 0
|ulxmap |qualsiasi numero reale| 0|
|ulymap |qualsiasi numero reale |nrighe - 1|
|xdim |qualsiasi numero reale| 1
|ydim |qualsiasi numero reale| 1
|bandrowbytes |qualsiasi intero > 0| numero intero più piccolo ≥ (ncols x nbits) / 8|
|totalrowbytes |qualsiasi numero intero > 0| per bil: nbands x bandrowbytes; per bip: numero intero più piccolo ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |qualsiasi intero ≥ 0| 0|

## Riferimenti

* [Formato file HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

