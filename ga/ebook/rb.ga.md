{
  "date": "2021-03-08",
  "keywords": [
"RB",
"Gléas eBook Rocket Nuvo Media",
"comhad",
"síneadh",
"formáid",
"ríomhleabhar"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid RB le haghaidh gléas eBook Rocket Nuvo Media agus APInna ar féidir leo comhaid RB a chruthú agus a oscailt.",
  "title": "RB - Comhad Ríomhleabhar Rocket",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-gab"
}
},
  "lastmod": "2021-03-08"
}

## Cad is comhad RB ann?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Cé go bhfuil Rocket eBook in ann íomhánna a thaispeáint, ach amháin i taispeáint dubh agus bán. Tá scáileán 106 dpi nó 480 x 320 picteilín aige ar scáileán tadhaill 4.5 x 3-orlach. Ceanglaíonn an Rocket eBook le ríomhaire trí nasc port srathach chun ríomhleabhair a íoslódáil i bhformáid comhaid RB. Tá na comhaid RB in ann DRM a úsáid ach níl an teicneolaíocht seo á húsáid i ríomhleabhair nua-aimseartha. Go hiondúil bíonn comhad HTML leis na híomhánna sa chomhad RB agus comhad pseudo-OPF leis na meiteashonraí ar fad (.info).

## Sonraíocht Theicniúil d'Fhormáid Chomhaid RB ##

Tá uimhir draíochta (i heics) le feiceáil sa chéad 4 beart an chomhaid: B0 0C B0 0C.

Dealraíonn sé gur uimhir leagain an chéad dá beart eile, cosúil le 02 00”, a sheasann do mhórleagan 2 agus mionleagan 0.

Sna ceithre beart eile tá an téacs NUVO, agus 4 beart 00h ina dhiaidh sin.

The next 4-byte is the date when the book was created, encoded as an int16. Cuireann sé seo muid ag fritháireamh 0Eh. Ionchódaigh seanleagan ORocketLibrary luach iomlán na bliana (ie, ba é 1999 CF 07, ba é 2000 D0 07). Sa leagan is déanaí, stóráiltear tm_year focal ar fhocal, ie 100 don bhliain 2000 (64 00). Tar éis na bliana tagann slánuimhir8 a sheasann don uimhir choibhneasta 1 mhí, agus int8 a ionadaíonn lá na míosa.

Is é 00h an chéad 6 beart eile. Chun am a shocrú, féadfar iad seo a chur in áirithe.

Tá glanfhritháireamh an Clár na nÁbhar le fáil in int32 ar fhritháireamh 18h.

Ina dhiaidh seo tá int32 ina bhfuil fad an chomhaid .rb. Úsáidtear é seo chun a chinneadh an bhfuil na comhaid iomlán nó nach bhfuil.

Is cosúil nach bhfuil gá leis an smután iomlán beart seo (20h go 128h) ach amháin le teideal atá criptithe. I teidil neamhchriptithe, tá siad i gcónaí nialas.

I bhformhór na gcásanna, seo a leanas an clár ábhair (ar fhritháireamh 128). Tosaíonn sé le comhaireamh int32 de líon na n-iontrálacha leathanach (rannáin .rb-comhad) sa ToC. Is éard atá i ngach iontráil ainm (stuáil nialasach go 32 beart), agus 3 int32 ina dhiaidh sin: fad na míre sonraí, an suíomh sa chomhad .rb, agus bratach don iontráil seo. Ón lá atá inniu ann, is iad na luachanna atá ar eolas ná: 1 (criptithe), 2 (leathanach faisnéise), agus 8 (deflated). Tá na hainmneacha go léir in oiriúint, de réir mar is gá, chun a chinntiú go bhfuil siad ar fad uathúil.

## Tagairtí

* [Ríomhléitheoir - Le MobileRead]( https://en.wikipedia.org/wiki/E-reader)


