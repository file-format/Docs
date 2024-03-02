{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid ACCDB agus APIanna ar féidir leo comhaid ACCDB a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid ACCDB - Comhad Bunachar Sonraí Microsoft Access 2007",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-gab"
}
},
  "lastmod": "2020-11-12"
}

## Cad is comhad ACCDB ann?

Is comhad bunachar sonraí de chuid Microsoft Access 2007 é comhad le síneadh .accdb a stórálann sonraí úsáideoirí i dtáblaí. Tacaíonn sé le stóráil
foirmeacha saincheaptha, ceisteanna SQL, agus sonraí eile. Tháinig comhaid ACCDB in ionad comhaid [MDB](/database/mdb/) tar éis do Microsoft aistriú go struchtúr comhaid bunaithe ar XML. Is féidir comhaid ACCDB a thiontú go MDB fós le sean-chomhoiriúnacht. Mar sin féin, is é an ACCDB an fhormáid comhaid bunachar sonraí Access a úsáidtear go forleathan anois. Thacaigh Microsoft freisin le gnéithe breise i bhformáid ACCDB ar nós an fhéidearthacht ceangaltáin chomhaid, sonraí dénártha, agus tacaíocht allamuigh illuacha a stóráil.

## Formáid Chomhaid ACCDB

Cosúil le MDB, níl aon sonraíochtaí poiblí ar fáil maidir le formáid comhaid ACCDB. Tacaíonn Microsoft le rochtain a fháil ar na comhaid seo go clárach trí chaighdeán Nascacht Bunachar Sonraí Oscailte (ODBC) agus Visual Basic for Applications (VBA).

### Léargas

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. I gcomhaid ACCDB, is cosúil go léiríonn an táscaire seo comhoiriúnacht an chomhaid seachas an leagan den inneall ACE a úsáideadh chun é a chruthú.

## Tagairtí

* [Rochtain ar Sonraíochtaí 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Innill Bunachar Sonraí Scaird Microsoft](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [Cén formáid comhaid Rochtana ar cheart dom a úsáid?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


