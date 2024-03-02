{
  "date": "2021-02-15",
  "keywords": [
"comhad asf",
"formáid comhaid asf",
"cad is comhad asf ann",
"comhad",
"sampla asf",
"síneadh comhad asf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF - Formáid Chomhaid Ardchórais",
  "description": "Foghlaim faoi fhormáid comhaid ASF agus APIanna ar féidir leo comhaid ASF a chruthú agus a oscailt.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-gaf"
}
},
  "lastmod": "2021-02-16"
}

## Cad is comhad ASF ann?

Is formáid comhaid ilmheán é comhad le síneadh .asf chun sruthanna meán digiteach a stóráil agus a sheinm thar an líonra. Is formáid comhaid coimeádán é ar féidir ábhar físe agus fuaime a bheith ann le haghaidh sruthú ar líne. Is annamh a bhfaighidh tú comhaid ASF, agus is dócha go dtiocfaidh tú trasna ar chomhaid Windows Media Audio ([WMA](/audio/wma/)) agus Windows Media Video ([WMV](/video/wmv/)) a shonraíonn comhaid ASF araon a bhfuil inneachar ionchódaithe acu le codecs faoi seach. Is féidir comhaid meán Windows a chruthú agus a léamh ag baint úsáide as an Windows Media Formáid SDK.

## Formáid Comhaid ASF

Is féidir le sruthanna neamhspleácha nó cleithiúnacha iolracha a bheith i gcomhad ASF. Féadfaidh sé seo sruthanna fuaime iolracha a áireamh le haghaidh fuaime ilchainéil nó sruthanna físeáin ilráta giotán. Déanann na giotánráití iolracha na sruthanna oiriúnach le tarchur thar bandaleithead éagsúla. Ina theannta sin, is féidir leis na sruthanna i gcomhad ASF a bheith i bhformáid chomhbhrúite nó neamh-chomhbhrúite. Baintear an comhbhrú is fearr amach le codecs Sraith 9 Sraith Fuaime agus Físeáin Microsoft Windows Media. Tá sonraíochtaí iomlána formáid comhaid ASF ar fáil ar [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Struchtúr Comhaid Barrleibhéil ASF

Go loighciúil bíonn trí chineál réad barrleibhéil i gcomhaid ASF:

* `Header Object` - éigeantach agus ní mór é a chur ag tús gach comhad ASF

* `Réad Sonraí` - éigeantach agus ní mór dó an réad ceanntásc a leanúint

* `Réad(í) Innéacs' - roghnach, ach úsáideach chun rochtain randamach bunaithe ar am a sholáthar ar chomhaid ASF


Taispeánann an íomhá seo a leanas struchtúr comhad barrleibhéil na gcomhad ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Cuspóir Ceanntásc Barrleibhéil ASF

Soláthraíonn an réad Ceanntásc seicheamh beart a bhfuil aithne mhaith air ag tús na gcomhad ASF agus is féidir meiteashonraí ar nós faisnéis bhibleagrafaíochta a chuimsiú go roghnach. Tá an fhaisnéis go léir ann a theastaíonn chun an fhaisnéis laistigh den réad sonraí a léirmhíniú i gceart. Féadfaidh roinnt rudaí caighdeánacha a bheith san Cuspóir Ceanntásc lena n-áirítear, ach gan a bheith teoranta do:

 * File Properties Object - Tá tréithe comhaid dhomhanda ann.
 * Stream Properties Object - Sainmhíníonn sruth meán digiteach agus a saintréithe.
 * Réad Síneadh Ceanntásc - Ligeann sé feidhmiúlacht bhreise a chur le comhad ASF agus comhoiriúnacht siar á choinneáil.
 * Cur síos ar an ábhar Cuspóir - Tá faisnéis bhibleagrafaíochta ann.
 * Script Command Object - Tá orduithe ann is féidir a fhorghníomhú ar an amlíne athsheinm.
 * Réad Marcála - Soláthraíonn sé pointí léim ainmnithe laistigh de chomhad.

Léirítear an Cuspóir Ceanntásc ag baint úsáide as an struchtúr seo a leanas:

|Ainm an raoin |Cineál réimse |Méid (giotáin)|
---|---|---|
|Aitheantas an ábhair| GUID| 128|
|Méid an Réad| QWORD| 64|
|Líon na nOibiachtaí Ceanntásca| DWORD| 32|
|Ar cosaint1| BYTE| 8|
|Ar cosaint2| BYTE| 8|

#### Réad Sonraí Barrleibhéil ASF

Tá na sonraí meán digiteach go léir do chomhad ASF san oibiacht sonraí agus stóráiltear iad i bhfoirm paicéid sonraí ASF. Tá fad seasta ag gach paicéad sonraí agus tá sonraí ann maidir le sruth meán digiteach amháin nó níos mó.

#### Cuspóirí Innéacs Barrleibhéil ASF

Tá an dá chineál seo a leanas ag réada innéacs barrleibhéil ASF:

 * `Réad Innéacs Simplí` - Tá innéacs ama-bhunaithe de na sonraí físeáin i gcomhad ASF. Tá an t-eatramh ama idir iontrálacha innéacs tairiseach agus stóráiltear é san Oibiacht Innéacs Simplí.
 * `Réad Innéacs` - Tagraíonn sé don Réad Innéacs, an Réad Innéacsaithe Meáin, agus an Réad Innéacs Cóid Ama, a bhfuil a bhformáidí comhchosúil. Cosúil leis an Oibiacht Innéacs Simplí, déanann an Innéacs Object innéacsú de réir ama le eatramh ama socraithe ach níl sé teoranta do shruthanna físeáin.

## Tagairtí

* [Formáid Comhaid ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [Formáid Comhaid QuickTime - Vicipéid](https://en.wikipedia.org/wiki/QuickTime_File_Format)


