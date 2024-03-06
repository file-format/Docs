{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "HDR fails - ESRI BIL galvenes faila formāts",
  "description":"Kas ir HDR fails?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr-lv",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Kas ir HDR fails?

HDR fails ir GIS galvenes fails, kas satur galvenes informāciju joslas interleaved by line (.BIL) failam. Tas apraksta attēla datus, un tam ir tāds pats nosaukums kā attēla failam. HDR fails sastāv no ierakstu kopas, no kuriem katrs apraksta noteiktu attēla atribūtu. HDR fails apraksta BIL faila izkārtojumu un formatējumu, lai to pārtulkotu uz reālās pasaules koordinātām kombinācijā ar atsevišķu ģeogrāfiskās norādes failu.

## HDR faila formāts

HDR faili tiek saglabāti ASCII teksta faila formātā. Tas satur ierakstu kopu, kur katrs ieraksts apraksta noteiktu attēla atribūtu. Katram HDR failam ir šāds formāts:

```
<keyword> <value>
```

`<keyword> ` — tas norāda konkrēto atribūtu, kas tiek iestatīts
`<value> ` — tā ir vērtība, kurai tiek iestatīts atribūts

Ierakstu secībai galvenē nav ierobežojumu. Tomēr katram ierakstam ir jāatrodas atsevišķā rindas rindā, lai atbilstu HDR lasītāju izmantotajai parsēšanas metodei.

## HDR failā izmantoto atslēgvārdu kopsavilkums

|Atslēgvārds |Pieņemamā vērtība |Noklusējums|
---|---|---|
|nrows |jebkurš vesels skaitlis > 0| neviens
|ncols |jebkurš vesels skaitlis > 0| neviens
|nbands |jebkurš vesels skaitlis > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|baitu secība| I = Intel;M = Motorola |tāds pats kā saimniekdators|
|izkārtojums| bil, bip, bsq| bil|
|izlaist baitus| jebkurš vesels skaitlis ≥ 0| 0
|ulxmap |jebkurš reāls skaitlis| 0|
|ulymap |jebkurš reāls skaitlis |nrows - 1|
|xdim |jebkurš reāls skaitlis| 1
|ydim |jebkurš reāls skaitlis| 1
|joslas baiti |jebkurš vesels skaitlis > 0| mazākais veselais skaitlis ≥ (ncols x nbits) / 8|
|kopā baiti |jebkurš vesels skaitlis > 0| bil: njoslas x joslas baiti; bip: mazākais veselais skaitlis ≥ (ncols x nbands x nbits) / 8|
|joslasgapbaiti |jebkurš vesels skaitlis ≥ 0| 0|

## Atsauces

* [HRD faila formāts — ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


