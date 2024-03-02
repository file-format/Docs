{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"comhad",
"síneadh",
"formáid",
"ríomhleabhar",
"Leabhar digiteach"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid LRF agus APIanna ar féidir leo comhaid LRF a chruthú agus a oscailt.",
  "title": "Formáid Comhaid LRF - Comhad Léitheoir Inaistrithe Sony",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-gaf"
}
},
  "lastmod": "2019-12-12"
}

## Cad is comhad LRF ann?

Comhad le síneadh .lrf is ea comhad ríomhleabhair Bhanda Leathan (BBeB) ina bhfuil sonraí do BBeB Sony, lena n-áirítear téacs, íomhánna agus sonraí uimhriúcháin. Sábháiltear an comhad i bhformáid dhénártha chomhbhrúite ina bhfuil ceanntásc, líon sonraithe réad, agus innéacs oibiachta. Cuimsíonn comhaid LRF agus LRX an dá fhormáid leabhair BBeB atá ar fáil. Níl na comhaid LRF criptithe agus is féidir iad a thiomsú ó chomhaid [LRX](/ebook/lrf/). Is féidir na comhaid LRF a thiontú ó go leor cineálacha comhaid eile lena n-áirítear PDF agus HTML. Mura féidir le do ríomhaire an comhad LRF a oscailt, is dócha nach bhfuil na bogearraí suiteáilte agat chun na comhaid LRF a oscailt nó a chur in eagar. Is iad na cláir is féidir comhaid LRF a oscailt ná Calibre, BookDesigner, Makelrf agus Canon Book Creator do Windows, Calibre le haghaidh Linux, Calibre, agus Sony Reader le haghaidh Macintosh.

## Stair Ghearr

Baineann cineál comhaid LRF go príomha le Line Rider faoi [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Bréagán fisice idirlín é The Line Rider agus ba mac léinn ollscoile Slóivéineach, Boštjan Čadež, a chum é i Meán Fómhair 2006. Úsáideann ríomhléitheoirí ríomhleabhair bhranda Sony (cosúil le léitheoirí Sony PRS-500 agus Sony Librie) an síneadh comhad LRF le haghaidh a gcuid doiciméad agus téacsanna. Tá an cineál comhaid dílsithe seo imithe i léig anois, chomh maith leis na comhaid LRS agus LRX gaolmhara. Ba iad na trí chineál comhaid sin an ríomhleabhar Leathanbhanda (BBeB) a scoireadh in 2010 nuair a thosaigh Sony ag díol a ríomhleabhair i bhformáid EPUB.

## Formáid Comhaid LRF

Tá sonraíochtaí mionsonraithe formáid comhaid LRF ar fáil ag [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Tá comhad LRF comhdhéanta de:
* ceanntásc

* roinnt rudaí

* innéacs oibiachta.


Tá na luachanna seo go léir in ord Intel (LSB ar dtús).

### ceanntásc LRF

|Fritháireamh (heicsidheachúlach) |Méid(bearta) |Ainm/Brí| Luach samplach|
---|---|---|---|
|0 |8| Síniú LRF| 4C 00 52 00 46 00 00 00=LRF in Unicode |
|8 |2| leagan?| 999 i bhformhór na gcomhad|
|A |2| Criptiúchán Psuedo | beart eochrach 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| Líon na nOibiachtaí |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| anaithnid | 0|
|24 |1| Bratacha| (16 - cúl le tosaigh, 1 = tosaigh le cúl) 16|
|25 |1| anaithnid |(stuáil?) 0|
|26 |2| anaithnid | 1600|
|28 |2| anaithnid | (stuáil?) 0|
|2A |2| Airde?| 600|
|2C |2| Leithead?| 800|
|2E |1| anaithnid | 24|
|2F |1| anaithnid |(stuáil?) 0|
|30 |0×14| anaithnid | nialais |
|44 |4| Aitheantas an oibiachta de réad PlaneStream (0x1E) amháin| 0x0042|
|48 |4| anaithnid |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Tagairtí

* [Formáid Comhaid LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB - Le Vicipéid]( https://ga.wikipedia.org/wiki/BBeB)


