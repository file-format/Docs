{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad WOFF2 - Formáid Cló Oscailte Gréasáin 2.0 Comhad",
  "description": "Foghlaim faoi cad is comhad WOFF2 ann agus APIanna ar féidir comhad WOFF2 a chruthú agus a oscailt.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-ga2"
}
},
  "lastmod": "2023-01-10"
}

## Cad is comhad WOFF2 ann?

Is clófhormáid é WOFF2 atá ina leagan níos comhbhrúite den Fhoirm Chló Oscailte Gréasáin (WOFF). Forbraíodh é mar bhealach chun méid comhaid clónna gréasáin a laghdú, rud a ligeann dóibh luchtú níos tapúla agus níos lú bandaleithead a úsáid. Úsáideann WOFF2 algartam comhbhrú ar a dtugtar Brotli chun na sonraí cló a chomhbhrú, rud a d’fhéadfadh méideanna comhaid a bheith i bhfad níos lú ná clónna coibhéiseacha [WOFF](/font/woff/) mar thoradh air. Tacaíonn formhór na mbrabhsálaithe gréasáin nua-aimseartha leis an bhformáid seo, lena n-áirítear Chrome, Firefox, Safari, Opera agus Edge (leagan 14 ar aghaidh).

## Formáid Chomhaid WOFF2 - Tuilleadh Eolais

Tá struchtúr inmheánach comhad clóchomhad WOFF2 comhdhéanta de roinnt codanna éagsúla, lena n-áirítear ceanntásc, meiteashonraí, eolaire tábla, agus na sonraí cló féin.

 1. Tá faisnéis sa cheanntásc faoi fhormáid iomlán an chomhaid, lena n-áirítear uimhir an leagain agus líon na dtáblaí atá sa chomhad.

 1. Tá faisnéis ar nós ainm cló, cóipcheart, agus faisnéis eile a bhaineann le cló.

 1. Tá faisnéis san eolaire táblaí faoi na táblaí éagsúla atá sa chló, lena n-áirítear a suíomh sa chomhad agus a fhad.

 1. Tá na sonraí cló féin roinnte i roinnt táblaí éagsúla, gach ceann acu ina bhfuil faisnéis shonrach faoin gcló, mar a charachtair agus a glyphs comhfhreagracha. D’fhéadfadh go gcuimseodh na táblaí seo:

 * Tá imlíne an chló iarbhír sa tábla 'glyf', lena n-áirítear cruth agus méid gach carachtar.
 * Tá faisnéis ghinearálta faoin gcló sa tábla 'ceann', mar shampla a uimhir leagain, méid an dearaidh, agus mar sin de.
 * Tá faisnéis sa tábla ‘hmtx’ faoi mhéadracht an chló, lena n-áirítear leithid agus suímh na gcarachtar.
 * Déantar gach tábla a chomhbhrú agus a stóráil i bhformáid comhaid WOFF2 tar éis dó an próiseas ionchódaithe a chríochnú.

Tá an struchtúr iomlán deartha chun parsáil agus díchódú tapa a cheadú, ionas gur féidir le brabhsálaithe gréasáin an cló a luchtú agus a thaispeáint go tapa agus go héifeachtach ar shuíomh Gréasáin.

### Ceanntásc WOFF2
Cuimsíonn an ceanntásc WOFF síniú aitheantais a léiríonn an cineál sonraí atá sa chomhad. Seo a leanas ceanntásc WOFF mar aon lena réimsí.

|Cineál|Ainm Réimse|Cur Síos|
---|---|---|
|Uint32|síniú |0x774F4632 'wOF2' |
|Uint32| blas |An leagan sfnt den chló ionchuir.|
|Uint32| fad |Méid iomlán an chomhaid WOFF.|
|Uint16| numTables |Líon na n-iontrálacha san eolaire táblaí cló.|
|Uint16| in áirithe | in áirithe; socraithe go nialas.|
|Uint32| totalSfntSize |Méid iomlán atá ag teastáil le haghaidh na sonraí cló neamh-chomhbhrúite, lena n-áirítear an ceanntásc sfnt, eolaire, agus táblaí na gclónna (stuáil san áireamh).|
|Uint32| totalCompressedSize Fad iomlán an bhloic chomhbhrúite sonraí.|
|Uint16| majorVersion |Mórleagan den chomhad WOFF.|
|Uint16| minorVersion |Mionleagan den chomhad WOFF.|
|Uint32| metaOffset |Fritháireamh go bloc meiteashonraí, ó thús an chomhaid WOFF.|
|Uint32| metaLength |Fad an bhloc meiteashonraí comhbhrúite.|
|Uint32| metaOrigLength |Méid neamh-chomhbhrúite an bhloc meiteashonraí.|
|Uint32| privOffset |Fritháireamh go bloc sonraí príobháideacha, ó thús an chomhaid WOFF.|
|Uint32| privLength |Fad an bhloca sonraí príobháideacha.|


## Tagairtí
 * [W3 WOFF2 Formáid Comhaid](https://www.w3.org/TR/WOFF2/)

