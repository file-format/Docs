{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - Formáid Chomhaid Oscailte Gréasáin",
  "description": "Is formáid chló oscailte é comhad WOFF a cruthaíodh i bhFormáid Cló Oscailte Gréasáin.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-gaf"
}
},
  "lastmod": "2020-09-30"
}

## Cad is comhad WOFF ann?

Is comhad cló gréasáin é comhad le síneadh .woff bunaithe ar an bhFormáid Cló Oscailte Gréasáin (WOFF). Tá coimeádán comhbhrúite formáid-sonrach aige bunaithe ar chineálacha cló TrueType (.TTF) nó OpenType (.OTT). Tugadh WOFF isteach agus é mar aidhm aige clónna gréasáin a dhifreáil ó chomhaid chlónna a úsáidtear in fheidhmchláir deisce. Ina theannta sin, an fhormáid atá dírithe chun laghdú ar an latency aistriú clónna ó fhreastalaí go ríomhaire an chliaint thar an líonra. Tá roinnt uirlisí ar fáil ar féidir comhaid WOFF a thiontú go TTF agus formáidí clóchomhaid eile.

## Formáid Comhaid WOFF

Comhbhrúíonn formáid chló WOFF táblaí sonraí cló de struchtúir sfnt bunaithe ar thábla a úsáidtear i gcineálacha éagsúla cló ar nós TrueType, OpenType, agus Open Font Format. Tá sé cosúil le coimeádán do na cineálacha cló seo agus tá spás ann freisin chun meiteashonraí an chló agus sonraí úsáide príobháideacha a chur san áireamh sa choimeádán. Úsáideann tiontairí na comhaid sfnt isteach i gcomhad formáidithe WOFF agus cuireann gníomhairí úsáideora an comhad ionchódaithe ar ais lena úsáid leis an doiciméad gréasáin. Ní mór a thabhairt faoi deara go dtagann na sonraí cló athchóirithe go díreach leis an bhformáid cló ionchuir ó gach gné.

Comhad WOFF Is minic a bhíonn gnéithe breise i bhfóntais mar fhoshraith glyph, bailíochtú nó breisithe clóghnéithe ach ní gá é. Ní mór don chruthaitheoir agus do ghníomhairí úsáide araon a chinntiú go gcaomhnaítear bailíocht na sonraí cló bunúsacha.

### Struchtúr Comhad WOFF

Tá struchtúr comhaid WOFF cosúil le struchtúr clónna sfnt. Tá sé bunaithe ar eolaire tábla ina bhfuil na faid agus na fritháirimh do gach tábla sonraí cló. Leantar na táblaí go léir tar éis an t-eolas tosaigh seo. Tá bunachar clónna sa chomhad atá mar an gcéanna leis na clónna bunaidh. Tá ord na táblaí mar an gcéanna freisin ach féadfar gach ceann díobh a chomhbhrú. Tagann eolaire tábla WOFF in ionad an eolaire tábla bunaidh áfach.

Is éard atá i gcomhad WOFF ná seo a leanas:

 * WOFFHeader - Ceanntásc comhaid le cineál cló bunúsach agus leagan, mar aon le fritháirimh go meiteashonraí agus bloic sonraí príobháideacha.
 * TableDirectory - Eolaire na dtáblaí cló, ag léiriú méid bunaidh, méid comhbhrúite agus suíomh gach tábla laistigh den chomhad WOFF.
 * FontTables - Na táblaí sonraí cló ón gcló sfnt ionchuir, comhbhrúite chun riachtanais bandaleithead a laghdú.
 * ExtendedMetadata - Bloc roghnach meiteashonraí leathnaithe, léirithe i bhformáid XML agus comhbhrúite le haghaidh stórála sa chomhad WOFF.
 * PrivateData- Bloc roghnach sonraí príobháideacha le húsáid ag an dearthóir cló, teilgcheárta nó díoltóir.

### Ceanntásc WOFF
Cuimsíonn an ceanntásc WOFF síniú aitheantais a léiríonn an cineál sonraí atá sa chomhad. Seo a leanas ceanntásc WOFF mar aon lena réimsí.

|Cineál|Ainm Réimse|Cur Síos|
---|---|---|
|Uint32|síniú |0x774F4646 'wOFF' |
|Uint32| blas |An leagan sfnt den chló ionchuir.|
|Uint32| fad |Méid iomlán an chomhaid WOFF.|
|Uint16| numTables |Líon na n-iontrálacha san eolaire táblaí cló.|
|Uint16| in áirithe | in áirithe; socraithe go nialas.|
|Uint32| totalSfntSize |Méid iomlán atá ag teastáil le haghaidh na sonraí cló neamh-chomhbhrúite, lena n-áirítear an ceanntásc sfnt, eolaire, agus táblaí na gclónna (stuáil san áireamh).|
|Uint16| majorVersion |Mórleagan den chomhad WOFF.|
|Uint16| minorVersion |Mionleagan den chomhad WOFF.|
|Uint32| metaOffset |Fritháireamh go bloc meiteashonraí, ó thús an chomhaid WOFF.|
|Uint32| metaLength |Fad an bhloc meiteashonraí comhbhrúite.|
|Uint32| metaOrigLength |Méid neamh-chomhbhrúite an bhloc meiteashonraí.|
|Uint32| privOffset |Fritháireamh go bloc sonraí príobháideacha, ó thús an chomhaid WOFF.|
|Uint32| privLength |Fad an bhloca sonraí príobháideacha.|

## Tagairtí

 * [W3 WOFF Formáid Comhaid]( https://www.w3.org/TR/WOFF/)

