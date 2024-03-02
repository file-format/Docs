{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad HDR - Formáid Chomhaid Cheanntásca ESRI BIL",
  "description":"Cad is comhad HDR ann?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr-ga",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Cad is comhad HDR ann?

Is comhad ceanntásca GIS é comhad HDR ina bhfuil faisnéis ceanntásc do chomhad Banna idirdhuilleogach de réir líne (.BIL). Déanann sé cur síos ar shonraí na híomhá agus tá an t-ainm céanna air agus atá ar an gcomhad íomhá. Cuimsíonn comhad HDR sraith iontrálacha, agus cuireann gach ceann acu síos ar tréith ar leith den íomhá. Déanann an comhad HDR cur síos ar leagan amach agus formáidiú an chomhaid BIL le haistriú go comhordanáidí an fhíorshaoil in éineacht le comhad georeagartha ar leith.

## Formáid Comhaid HDR

Déantar comhaid HDR a shábháil i bhformáid téacschomhaid ASCII. Tá sraith iontrálacha ann ina ndéanann gach iontráil cur síos ar tréith ar leith den íomhá. Tá an fhormáid seo a leanas ag gach comhad HDR:

```
<keyword> <value>
```

`<keyword> ` - Léiríonn sé an tréith ar leith atá á leagan síos
`<value> ` - Is é an luach ar a bhfuil an tréith á socrú

Níl aon teorainn le hord na n-iontrálacha sa cheanntásc. Mar sin féin, caithfidh gach iontráil a bheith ar líne ar leith den líne chun cloí leis an modh parsála a úsáideann léitheoirí HDR.

## Achoimre ar na heochairfhocail a úsáidtear i gComhad HDR

|Eochairfhocal |Luach Inghlactha |Réamhshocrú|
---|---|---|
|nrows |aon slánuimhir > 0| aon cheann
|ncols |aon slánuimhir > 0| aon cheann
|nbannaí |aon slánuimhir > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|beartordú| I = Intel;M = Motorola |mar an gcéanna leis an meaisín ósta|
|leagan amach| bíp, bíp, bsq| bil|
| skipbytes | aon slánuimhir ≥ 0| 0
|ulxmapa | aon fhíoruimhir | 0|
|ulymap |réaduimhir ar bith |nrows - 1|
|xdim |aon uimhir réadach | 1
|ydim | fíoruimhir ar bith | 1
|bandrowbytes | aon slánuimhir > 0 | slánuimhir is lú ≥ (ncols x nbits) / 8|
|totalrowbytes |aon slánuimhir > 0| le haghaidh bil: nbands x bandrowbytes;do bíp: an tslánuimhir is lú ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes | slánuimhir ar bith ≥ 0 | 0|

## Tagairtí

* [Formáid Comhaid HDD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


