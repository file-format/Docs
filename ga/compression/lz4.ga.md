{
  "date": "2021-04-08",
  "keywords": [
"comhad lz4",
"formáid comhaid lz4",
"cad é comhad lz4",
"comhad",
"lz4 shampla",
"Síneadh comhad lz4",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ4 - LZ4 Formáid Chomhaid Chomhbhrúite",
  "description": "Foghlaim faoi fhormáid comhaid LBR agus APInna ar féidir leo comhaid LZ4 a chruthú agus a oscailt.",
  "linktitle": "LZ4",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-ga4"
}
},
  "lastmod": "2021-04-19"
}

## Cad is comhad LZ4 ann?

Is comhad cartlainne comhbhrúite é comhad a bhfuil iarmhír .lz4 air a cruthaíodh le feidhmchláir/fóntais a thacaíonn le comhbhrú [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). Díríonn algartam LZ4 ar chomhbhabhtáil idir luas agus cóimheas comhbhrú. Is féidir cartlann LZ4 comhbhrúite a chruthú trí úsáid a bhaint as fóntais líne ordaithe LZ4 agus is féidir iad a dhí-chomhbhrú ag baint úsáide as an gcéanna.

## Formáid Comhaid LZ4

Tá formáid comhaid LZ4, bunaithe ar algartam comhbhrú LZ4, neamhspleách ar chineál LAP, córas oibriúcháin, córas comhaid agus tacar carachtar. Tá sé oiriúnach le haghaidh comhbhrú comhad agus comhbhrú sruthú ag baint úsáide as an algartam LZ4. Rinne Yann Collet cur i bhfeidhm tosaigh na formáide LZ4 i dteanga [C](/programming/c/) in 2011 agus tá sé ar fáil mar thagairt ón bhforbróir ar [Github](https://github.com/lz4/lz4).

### Formáid Fráma LZ4

Tá struchtúr ginearálta formáid comhaid LZ4 mar a thaispeántar thíos.

|DraíochtNb|F. Tuairisceoir| Bloc |(...)|Críochmharc |C. Seiceam|
---|---|---|---|---|---|
|4 beart| 3-15 beart || 4 beart| 0-4 beart|

#### Uimhir Dhraíochta

4 Beart, formáid bheag endian. Luach: 0x184D2204

#### Tuairisceoir Fráma

Tá 3 t0 15 beart sa tuairisceoir fráma agus is é an chuid is tábhachtaí de na sonraíochtaí é. Le chéile, tagraítear do na réimsí Magic_Number agus Frame_Descriptor mar Cheanntásc Fráma LZ4, agus athraíonn a mhéid idir 7 agus 19 bytes. Tá sé mar a thaispeántar thíos.

|FLG| BD| (Méid an Ábhair)| (Aitheantas Foclóra)| HC|
---|---|---|---|---|
|1 beart| 1 beart| 0 - 8 beart| 0 - 4 beart| 1 beart|

#### Bloic Sonraí

Leanann gach bloc sonraí an t-ordú seo a leanas.

|Méid Bloc| sonraí| (Seic Bloc)|
---|---|---|
|4 beart| |0 - 4 beart|

#### EndMark

Críochnaíonn sreabhadh na mbloic nuair a leanann an luach 32-giotán 0x00000000 an bloc sonraí deiridh.

#### Seiceáil Ábhar

Fíoraíonn an Content_Checksum bailíocht an ábhair atá á dhíchódú i gceart agus déantar é ag baint úsáide as toradh algartam xxHash-32. Déanann sé torthaí tarchur rathúil na mbloc go léir a bhailíochtú san ord ceart agus gan aon earráid.

## Tagairtí

* [Formáid Fráma LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)

* [Algartam Comhbhrú LZ4 - Vicipéid]( https://ga.wikipedia.org/wiki/LZ4_(compression_algorithm))


