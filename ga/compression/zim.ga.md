{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid ZIM - Comhad Cartlainne OpenZIM",
  "description": "Foghlaim faoi fhormáid comhaid ZIM agus APIs ar féidir leo comhaid ZIM a chruthú agus a oscailt.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-gam"
}
},
  "lastmod": "2019-12-09"
}

## Cad is comhad ZIM ann? ##

Is cartlann iad comhaid a bhfuil iarmhír .zim orthu a cruthaíodh chun ábhar Vicí a stóráil as líne. Meastar gurb é an fhormáid comhaid oscailte is oiriúnaí chun Vicipéid a stóráil ar USB. Stórálann sé inneachar an tsuímh i bhformáid dhlúth. Tagann a ainm ó Zeno fheabhsaithe a bhí an fhormáid comhaid Zeno níos luaithe. Tá ZIM á chothabháil ag [openZIM ](https://openzim.org/)tionscadal atá urraithe ag Wikimedia CH, agus a fhaigheann tacaíocht ón Wikimedia Foundation. Is féidir le feidhmchláir mar Kiwix agus ZIMReader comhaid ZIM a oscailt. D'óstáil tionscadal OpenZIM cur i bhfeidhm formáid comhaid ZIM ar [Github](https://github.com/openzim) le haghaidh ranníocaíochta ó phobal OpenSource.

## Sonraíochtaí Formáid Comhaid ZIM

Forbraíodh formáid comhaid ZIM ar bharr [Zeno file format](https://openzim.org/wiki/Zeno_file_format) agus níl sé comhoiriúnach ar gcúl. Is iad na sonraíochtaí formáide maidir le formáid comhaid ZIM ná [available online](https://openzim.org/wiki/ZIM_file_format) le openZIM le haghaidh tagartha an fhorbróra. Chuir OpenZIM feidhmiú foinse oscailte C++, [LibZim](https://openzim.org/wiki/Zimlib), ar fáil chun comhaid ZIM a léamh agus a scríobh.

Úsáideann formáid comhaid ZIM comhbhrú LZMA2 chun an t-ábhar a dhéanamh dlúth.

{{< figure src="../ZIM_File_Format.jpeg" alt="Formáid Comhaid ZIM" >}}


### Ceanntásc ZIM

A ZIM file starts with a header that is at offset 0. Tá na comhábhair go léir bunaithe ar an gceann beag agus is slánuimhreacha gan síniú iad na slánuimhreacha go léir ie uint_16, uint_32, uint_64.

|Ainm Réimse |Cineál| Fritháireamh| Fad| Cur Síos|
---|---|---|---|---|
|uimhir draíochta| slánuimhir| 0| 4| Uimhir draíochta chun formáid an chomhaid a aithint, ní mór 72173914 (0x44D495A)|
|mórleagan| slánuimhir| 4| 2| Mórleagan den fhormáid comhaid ZIM (5 nó 6)|
|mionleagan| slánuimhir| 6| 2| Mionleagan den fhormáid comhaid ZIM|
|uuid| slánuimhir| 8| 16| aitheantas uathúil an chomhaid zim seo|
|altComhaireamh| slánuimhir| 24| 4| líon iomlán na n-alt|
|Cnuasáireamh| slánuimhir| 28| 4| líon iomlán na gcnuasach|
|urlPtrPos| slánuimhir| 32| 8| suíomh an liosta pointeora eolaire arna ordú ag URL|
|teidealPtrPos| slánuimhir| 40| 8| suíomh an liosta pointeora eolaire arna ordú de réir Teideal|
|cnuasachPtrPos| slánuimhir| 48| 8| suíomh an liosta pointeoir braisle|
|mimeListPos| slánuimhir| 56| 8| suíomh liosta na gcineálacha MIME (méid an chinn chomh maith)|
|príomhleathanach| slánuimhir| 64| 4| príomhleathanach nó 0xffffffff mura bhfuil príomhleathanach ann|
|leathanach leagan amach| slánuimhir| 68| 4| leathanach leagan amach nó 0xffffffffff mura bhfuil leathanach leagan amach ann|
|seiceáilPos| slánuimhir| 72| 8| pointeoir chuig md5checksum an chomhaid seo gan an tseiceáil féin. Léiríonn sé seo 16 beart i gcónaí roimh dheireadh an chomhaid.|

## Tagairtí ##

* [OpenZIM](https://openzim.org/)

* [C++ LibZim](https://openzim.org/wiki/Zimlib)


