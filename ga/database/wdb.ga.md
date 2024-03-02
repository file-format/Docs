{
  "date": "2021-08-24",
  "keywords": [
"comhad wdb",
"formáid comhaid wdb",
"cad is comhad wdb ann",
"comhad",
"sampla wtb",
"síneadh comhad wdb",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid WDB agus APIs ar féidir leo comhaid WDB a chruthú agus a oscailt.",
  "title": "WDB - Rianchomhad Freastalaí SQL",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wd-gab"
}
},
  "lastmod": "2021-08-24"
}

## Cad is comhad WDB ann?
Is comhad bunachar sonraí é comhad le síneadh .wdb cruthaithe ag Microsoft Works a úsáideadh chun feidhmeanna cosúil le córas bainistíochta bunachar sonraí a chomhlíonadh. Tá an comhad WDB cosúil leis an gcomhad Bunachar Sonraí Rochtana ([MDB](/database/mdb/)), ach níl sé chomh héifeachtach agus is mó teorainneacha. Ní féidir na comhaid WDB a oscailt trí úsáid a bhaint as Microsoft Access. Mar sin féin, is féidir leat an comhad WDB a oscailt i Microsoft Works agus ansin é a onnmhairiú chuig comhad MDB, chun comhad WDB a oscailt i MS Access.

## Formáid comhaid WDB
Is é Microsoft Works Database an fhormáid bhunachair shonraí dhúchais atá ag sraith oifigí Microsoft Works. Mar gheall ar nádúr dílseánaigh na formáide agus roinnt teorainneacha. Ní féidir na comhaid WDB a oscailt in aon bhogearraí eile seachas Microsoft Works. San fhormáid comhaid is féidir ceanntásc athfhillteach 10 beart a fháil roimh gach ceann de na teaghráin téacs ASCII a léiríonn luachanna na réimsí ar cuireadh deireadh leo le luach NULLComment. Tosaíonn an ceanntásc de ghnáth le beart ** \x0f** agus NULL, agus 4 beart sonraí ina dhiaidh sin agus NULLanna eile.

### Struchtúr comhaid

Tá struchtúr an chomhaid WDB tugtha thíos:
- **1ú ceanntásc**: ó thús an chomhaid, ag críochnú le \x25\x00\xf2 agus 244 NULL bytes
- **2ú ceanntásc**: ag tosú le \xffT - ie \xff\x54 agus ag síneadh le haghaidh 4096 beart, ina bhfuil ainmneacha colúin/réimsí agus rudaí eile, agus is cosúil go dtosaíonn sé ag suíomh beart 6144.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. Is é beart sonraí 2 an uimhir réimse, is é beart sonraí 3 an uimhir thaifid (ag cur beart sonraí 3, cuid 2 nuair a théann sé thar 256 taifead).


## Tagairtí ##

* [Úsáideoir:Formáid JesseW/wtb](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)


