{
  "date": "2021-09-08",
  "keywords": [
"comhad pcc",
"formáid comhaid pcc",
"Cad is comhad pcc ann",
"comhad",
"sampla pcc",
"Síneadh comhad pcc",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid PCC Mass Effect agus APIs ar féidir leo comhaid PCC a chruthú agus a oscailt.",
  "title": "CSP - Comhad Pacáiste Mais Éifeacht",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pc-gac"
}
},
  "lastmod": "2021-09-08"
}

## Cad is comhad CSP ann?

Is comhad [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) é comhad a bhfuil .pcc ann ina bhfuil sonraí cluiche chun ábhar cluiche ar nós samhlacha, uigeachtaí agus seomraí a mhodhnú. Is iad Mass Effect 2 agus 3 na chéad cluichí lámhachóirí atá bunaithe ar inneall cearrbhachais Unreal Engine 3. D'fhorbair [Bioware](https://www.bioware.com/about/) an cluiche ar dtús, a choinnigh formhór na n-acmhainní cluiche ina bhformáid chomhaid CSP dílsithe. Fuair Electronic Arts, príomhfhoilsitheoir siamsaíochta idirghníomhach domhanda, Bioware.

## Formáid Chomhaid CSP - Tuilleadh Eolais

Bíonn struchtúir chomhbhrúite agus/nó neamh-chomhbhrúite i gcomhaid CSP a chuireann leis an eagraíocht iomlán comhad.

### Struchtúr CCP Comhbhrúite

Cuimsíonn comhad PCC comhbhrúite táblaí agus sonraí atá deighilte ina smután. Tá líon athraitheach bloic chomhbhrúite i ngach smután.

 * `Chunks Header` - Ceanntásc coitianta 16 beart, ina bhfuil faisnéis faoi na smután.
 * `Chunk Header` - Ceanntásc 16 beart ina bhfuil faisnéis faoi na sonraí comhbhrúite amh atá san fhoirm bhloc.

### Struchtúr Neamh-chomhbhrúite PCC

Roinntear comhaid PCC neamh-chomhbhrúite i gcúig chuid a leanas.

 * `Header` - tá faisnéis bhunúsach ann faoi struchtúr an chomhaid CSP.
 * `Tábla Ainm` - tá ainm a fuarthas taobh istigh den phacáiste lena n-áirítear aicmí iompórtála, onnmhairí agus airíonna easpórtála.
 * `Tábla Iompórtála` - ina bhfuil na haicmí agus na réada go léir a allmhairíonn an CSP.
 * `Tábla Easpórtála` - ina bhfuil gach réad atá stóráilte sa phacáiste. Féadfaidh gach onnmhairiú a bheith éagsúil i méid.

## Tagairtí

 * [Me3Explorer - Formáid Chomhaid CSP]( https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Cluiche Aifreann Éifeacht]( https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware]( https://www.bioware.com/about/)

