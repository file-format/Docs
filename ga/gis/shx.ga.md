{
  "date": "2021-07-29",
  "keywords": [
"comhad shx",
"formáid comhaid shx",
"Cad is comhad shx ann",
"comhad",
"shx shampla",
"síneadh comhad shx",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SHX - Formáid Innéacs Cruth Shapefile",
  "description": "Foghlaim faoi fhormáid comhaid SHX agus APIs ar féidir leo comhaid SHX a chruthú agus a oscailt.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-gax"
}
},
  "lastmod": "2021-07-29"
}

## Cad is comhad SHX ann?
Baineann an comhad SHX le formáid innéacs crutha atá ina innéacs suímh den ghné-chéimseata chun cuardach a dhéanamh chun cinn agus siar go tapa. Is comhad fritháirimh rochtana díreach é an SHX. Níl aon sonraí sa chomhad seo, ach cóip dhúblach den chéad céad beart, uimhir thaifid agus fritháireamh go beart tosaigh an taifid sin sa shp. Tabhair faoi deara le do thoil nach bhfuil an comhad leis an iarmhír .shx ceangailte leis na [SHP](/gis/shp/) agus [DBF](/database/dbf/).

## Formáid comhaid SHX
San fhormáid SHX tá innéacs suímh den ghné-chéimseata agus ceanntásc 100 beart cosúil leis an gcomhad SHP, agus ina dhiaidh sin tá líon ar bith de thaifid fad seasta 8-beart ina bhfuil an dá réimse seo a leanas:
| Bearta | Cineál | Endianness | Úsáid |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | mór | Fritháireamh taifead (i bhfocail 16-giotán) |
| 4–7 | int32 | mór | Fad taifead (i bhfocail 16 ghiotán) |

Leis an innéacs seo is féidir cuardach a dhéanamh ar gcúl sa chomhad cruth trí, ar dtús, cuardach ar gcúl san innéacs cruthanna agus ansin an taifead a fhritháireamh a léamh. Is féidir an fritháireamh sin a úsáid chun an áit cheart a aimsiú sa chomhad SHP. Is féidir leat chun cinn a lorg freisin; líon treallach taifead a úsáideann an modh céanna. Mar sin féin, is féidir innéacs iomlán a ghiniúint mar aon le comhad SHP, ach is féidir leis an seans go mbeidh an comhad SHP truaillithe go tapa a mhéadú.


## Tagairtí

* [Shapefile - le Vicipéid)]( https://en.wikipedia.org/wiki/Shapefile)



