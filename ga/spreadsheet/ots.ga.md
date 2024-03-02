{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"comhad",
"síneadh",
"formáid comhaid",
"Excel",
"Scarbhileog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid OTS agus APIanna ar féidir leo comhaid OTS a chruthú agus a oscailt.",
  "title": "OTS - Formáid Chomhaid Teimpléad Scarbhileog OpenDocument",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-gas"
}
},
  "lastmod": "2021-01-19"
}

## Cad is comhad OTS ann?

Is comhad Teimpléad Scarbhileog OpenDocument é comhad le síneadh .ots a chruthaítear leis na bogearraí feidhmchláir Calc atá san áireamh in Apache OpenOffice. Tá bogearraí feidhmchláir Calc cosúil le Excel atá ar fáil i Microsoft Office. Úsáidtear formáid comhaid OTS chun teimpléid a chruthú ina bhfuil socruithe réamhshainithe a bhaineann le stíleanna, cló, sonraí, leagan amach scarbhileog, agus formáidiú. Tá `mime-type application/vnd.oasis.opendocument.spreadsheet-template` ag comhaid OTF. Is féidir na comhaid teimpléid seo a úsáid mar phointe tosaigh chun comhaid sonraí iarbhír a shábháiltear in [ODS file format](/spreadsheet/ods/) a ghiniúint agus a shábháil. Is féidir comhaid OTS a úsáid le feidhmchláir ar nós OpenOffice agus LibreOffice.

## Formáid Chomhaid OTS

Déantar comhaid OTS a shábháil i bhformáid comhaid bunaithe ar OpenDocument XML de chuid OASIS a chuimsíonn bailiúchán roinnt fodhoiciméid le pacáiste mar chartlann [ZIP](/compression/zip/). Stórálann gach zip-cartlann cuid den doiciméad iomlán agus stórálann gach fodhoiciméad gné ar leith den doiciméad. Mar shampla, tá an fhaisnéis stíle i bhfodhoiciméad amháin agus tá ábhar an doiciméid i bhfodhoiciméad eile. Tá na comhpháirteanna seo a leanas i gcáipéis tipiciúil ODF:

### Ábhar OTS.xml

Tá ábhar iarbhír an doiciméid sa chomhad content.xml. Ní chuimsíonn sé seo sonraí dénártha mar íomhánna, áfach.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Stíleanna.xml as Formáid Chomhaid OTS

Tá faisnéis stílithe sa chomhad styles.xml agus baintear úsáid mhór as chun formáidiú agus leagan amach. I measc na gcineálacha stíleanna tá:

 * Stíleanna alt
 * Stíleanna leathanaigh
 * Stíleanna carachtair
 * Stíleanna fráma
 * Liostaigh stíleanna

### Meta.xml

Tá faisnéis sa chomhad meta.xml faoi mheiteashonraí an chomhaid mar Údar, Dáta Athraithe Deiridh, etc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Socruithe.xml

Áirítear sa chomhad `settings.xml` socruithe leibhéal an doiciméid mar fhachtóir súmáil isteach agus suíomh cúrsóra.

## Tagairtí ##

* [sonraíocht OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument - Le Vicipéid](https://en.wikipedia.org/wiki/OpenDocument)


