{
  "date": "2021-04-08",
  "keywords": [
"comhad lzma",
"formáid comhaid lzma",
"cad is comhad lzma ann",
"comhad",
"sampla lzma",
"Síneadh comhad lzma",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZMA - LZMA Formáid Chomhaid Chomhbhrúite",
  "description": "Cad é comhad LZMA agus APIs is féidir comhaid LZMA a chruthú agus a oscailt.",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzm-gaa"
}
},
  "lastmod": "2021-04-18"
}

## Cad is comhad LZMA ann?

Is comhad cartlainne comhbhrúite é comhad le síneadh .lzma a cruthaíodh ag baint úsáide as modh comhbhrú LZMA (Algartam slabhra Lempel-Ziv-Markov). Faightear/úsáidtear iad seo go príomha ar chóras oibriúcháin Unix agus tá siad cosúil le halgartaim chomhbhrú eile ar nós [ZIP](/compression/zip/) chun méid comhaid a íoslaghdú. Is formáid comhaid oidhreachta é LZMA, atá á nó curtha ina hionad ag an bhformáid .xz. Is é an cineál MIME den fhormáid .lzma ná \`application/x-lzma'. Dhear Igor Pavlov an fhormáid comhaid seo le húsáid i LZMA SDK.

## Formáid Comhaid LZMA

Tá dhá phríomhchuid i gcomhad LZMA:

 1. Ceanntásc
 1. Sonraí Comhbhrúite


### Ceanntásc LZMA

Tá ceanntásc 13 beart ag na comhaid LZMA a leanann sonraí comhbhrúite LZMA. Is éard atá i gceanntásc LZMA ná:

 * Airíonna
 * Méid an Fhoclóra
 * Méid Neamh-chomhbhrúite

#### Airíonna Ceanntásca LZMA

Tá trí airí sa réimse Airíonna. Tugtar giorrúchán i lúibíní, agus raon luacha na maoine ina dhiaidh sin. Is éard atá sa réimse

1) líon na ngiotán comhthéacs litriúil (lc, [0, 8]);
2) líon na n-giotán suímh litriúil (lp, [0, 4]); agus
3) líon na n-giotán suímh (pb, [0, 4]).

#### Méid an Fhoclóra LZMA

Stóráiltear é seo mar shlánuimhir endian beag 32-giotán gan síniú le luachanna idir 2^n agus 2^n + 2^(n-1). Is féidir le LZMA Utils comhaid a dhí-chomhbhrú le haon mhéid foclóir.

#### Méid Neamh-chomhbhrúite
Stóráiltear an Méid Neamh-chomhbhrúite mar shlánuimhir endian beag 64-giotán gan síniú. Léiríonn luach speisialta 0xFFFF_FFFF_FFFF_FFFF go bhfuil Méid Neamh-chomhbhrúite anaithnid. Léirítear an luach ag Marcálaí Deireadh Pá-Ualach (\*) más rud é agus mura bhfuil an Méid Neamh-chomhbhrúite anaithnid.

## Tagairtí

* [Formáid Comhaid LZMA](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)

* [algartam slabhra Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)


