{
  "date": "2021-04-08",
  "keywords": [
"lz comhad",
"formáid comhaid lz",
"cad is comhad lz ann",
"comhad",
"lz shampla",
"lz síneadh comhad",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ - Lzip Formáid Comhaid Chomhbhrúite",
  "description": "Foghlaim faoi fhormáid comhaid LZ agus APIs ar féidir leo comhaid LZ a chruthú agus a oscailt.",
  "linktitle": "LZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-l-gaz"
}
},
  "lastmod": "2021-04-19"
}

## Cad is comhad LZ ann?

Is comhad cartlainne comhbhrúite é comhad le síneadh .lz a cruthaíodh le Lzip, ar uirlis ordú-líne saor in aisce é le haghaidh comhbhrú. Tacaíonn sé le comhdhlúthú chun comhaid tacaíochta a chomhbhrú. Tá feidhmchlár den chineál meán/lzip ag comhaid LZ agus tacaíonn siad le ciondálacha comhbhrú níos airde ná [BZ2](/compression/bz2/). Tá LZ bunaithe ar algartam LZMA (slabhra Lempel-Ziv-Markov) agus áirítear leo seiceála CRC 32-giotán agus bearta aitheantais chun sláine an chomhaid a sheiceáil.

## Formáid Chomhbhrúite LZMA

Is éard atá i bhformáid comhbhrúite LZMA ná sruth comhbhrúite giotán atá ionchódaithe ag baint úsáide as códóir raon dénártha oiriúnaitheach. Tá an sruth roinnte ina phaicéid. Déanann gach paicéad cur síos ar bheart amháin nó ar sheicheamh LZ77. Tá fad agus fad gach paicéad ionchódaithe go hintuigthe nó go sainráite.

Seo a leanas na seacht gcineál paicéad ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + byteCód| LIT| Beart amháin atá ionchódaithe ag baint úsáide as códóir raon dénártha oiriúnaitheach.|
|1+0 + leann + dist| MATCH| Seicheamh tipiciúil LZ77 a dhéanann cur síos ar fhad agus fad seichimh.|
|1+1+0+0| GEARDREP| Sraith amháin-beart LZ77. Is ionann an fad agus an fad LZ77 a úsáideadh go deireanach. ||
|1+1+0+1 + lionsa| LONGREP[0] | Sraith LZ77 saor in aisce,. Is ionann an fad agus an fad LZ77 a úsáideadh go deireanach. ||
|1+1+1+0 + lionsa| LONGREP[1] | Sraith LZ77 saor in aisce,. Tá an fad cothrom leis an dara fad is déanaí a úsáideadh LZ77.|
|1+1+1+1+0 + lionsa| LONGREP[2] | Sraith LZ77 saor in aisce,. Tá an fad cothrom leis an tríú fad is déanaí a úsáideadh LZ77.|
|1+1+1+1+1+leann| LONGREP[3] | Sraith LZ77 saor in aisce,. Tá an fad cothrom leis an gceathrú fad is déanaí a úsáideadh LZ77.|


## Tagairtí

* [LZMA - Vicipéid]( https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)

* [Lzip]( https://ga.wikipedia.org/wiki/Lzip)


