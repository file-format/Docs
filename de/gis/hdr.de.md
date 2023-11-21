{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR-Datei – ESRI BIL Header-Dateiformat",
  "description":"Was ist eine HDR-Datei?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Was ist eine HDR-Datei?

Eine HDR-Datei ist eine GIS-Header-Datei, die Header-Informationen für eine Band-Interleaved-by-Line-Datei (.BIL) enthält. Es beschreibt die Bilddaten und hat den gleichen Namen wie die Bilddatei. Eine HDR-Datei besteht aus einer Reihe von Einträgen, von denen jeder ein bestimmtes Attribut des Bildes beschreibt. Die HDR-Datei beschreibt das Layout und die Formatierung der BIL-Datei für die Übersetzung in reale Koordinaten in Kombination mit einer separaten Georeferenzierungsdatei.

## HDR-Dateiformat

HDR-Dateien werden im ASCII-Textdateiformat gespeichert. Es enthält eine Reihe von Einträgen, wobei jeder Eintrag ein bestimmtes Attribut des Bildes beschreibt. Jede HDR-Datei hat das folgende Format:

```
<keyword> <value>
```

`<keyword> ` – Es gibt das bestimmte Attribut an, das festgelegt wird
`<value> ` – Dies ist der Wert, auf den das Attribut gesetzt wird

Es gibt keine Einschränkung hinsichtlich der Reihenfolge der Einträge im Header. Allerdings muss jeder Eintrag in einer separaten Zeile der Zeile stehen, um der von HDR-Readern verwendeten Parsing-Methode zu entsprechen.

## Zusammenfassung der in der HDR-Datei verwendeten Schlüsselwörter

|Schlüsselwort |Akzeptabler Wert |Standard|
---|---|---|
|nrows |jede Ganzzahl > 0| keiner
|ncols |beliebige ganze Zahl > 0| keiner
|nbands |jede Ganzzahl > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |identisch mit Host-Rechner|
|Layout| bil, bip, bsq| bil|
|skipbytes| jede ganze Zahl ≥ 0| 0
|ulxmap |beliebige reelle Zahl| 0|
|ulymap |beliebige reelle Zahl |nrows - 1|
|xdim |beliebige reelle Zahl| 1
|ydim |beliebige reelle Zahl| 1
|bandrowbytes |beliebige ganze Zahl > 0| kleinste ganze Zahl ≥ (ncols x nbits) / 8|
|totalrowbytes |jede Ganzzahl > 0| für bil: nbands x bandrowbytes;für bip: kleinste ganze Zahl ≥ (ncols x nbands x nbits) / 8|
|Bandlückenbytes |beliebige Ganzzahl ≥ 0| 0|

## Verweise

* [HRD-Dateiformat – ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

