{
  "date": "2021-06-16",
  "keywords": [
"BFC",
"síneadh",
"comhad cdb",
"formáid comhaid cdb",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Cad is comhad cdb ann"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid BFC agus APIanna ar féidir leo comhaid BFC a chruthú agus a oscailt.",
  "title": "CDB - Comhad Bunachar Sonraí Tairiseach",
  "linktitle": "CDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-cd-gab"
}
},
  "lastmod": "2021-06-16"
}

## Cad is comhad BFC ann?
Úsáidtear na comhaid BFC in feidhmchláir atá ríthábhachtach do mhisin mar ríomhphost. Seasann an BFC do bunachar sonraí seasmhach”, pacáiste tapa, iontaofa agus simplí chun bunachair shonraí seasta a chruthú nó a léamh. Tá athsholáthar bunachar sonraí sábháilte i gcoinne tuairteanna córais. Ní gá d'úsáideoirí sos a dhéanamh le linn athscríobh. Feidhmíonn CDB mar eagar comhthiomsaitheach (ar an diosca), ag mapáil eochracha ar luachanna, agus cuireann sé ar chumas luachanna iolracha a stóráil in eochair amháin.

## Formáid Chomhaid BFC

Stórálann formáid comhaid BFC uimhreacha, fritháirimh, faid, agus luachanna hash i bhformáid bheag endian mar shlánuimhreacha 32-giotán gan síniú. Ceaptar gur teaghráin beart teimhneach iad eochracha agus sonraí gan aon chóireáil speisialta. Ag tús an bhunachair shonraí, is ionann an ceanntásc méid seasta agus 256 tábla hash trína n-áit laistigh den chomhad agus a gcuid fad i sliotán a liostú. De ghnáth, stóráiltear na sonraí mar sheicheamh taifead, stórálann gach taifead fad eochrach, fad sonraí, eochair, agus sonraí. Níl aon rialacha sórtála nó ailínithe ann. Tá sraith de 256 tábla hais d'fhaid éagsúla i ndiaidh na dtaifead. Ós rud é gur fad bailí é nialas, d'fhéadfadh go mbeadh níos lú ná 256 tábla hash stóráilte go fisiciúil sa bhunachar sonraí, ach níl aon rud a mheastar a bheith ina 256 tábla. Tá táblaí hash comhdhéanta de shraith sliotán, gach ceann acu ina bhfuil luach hash agus fritháireamh taifead. Tá fritháireamh nialais ag sliotáin fholmha.

### Struchtúr Formáid Chomhaid BFC

Tá bunachar sonraí BFC comhdhéanta de thacar sonraí iomlán i gcomhad ríomhaire amháin. Tá trí chuid ann:
- Ceanntásc de mhéid seasta
- Sonraí
- Sraith de táblaí hash.

Tá cuardaigh ar fáil d'eochracha cruinne amháin. Gníomhaíonn cuardaigh ag baint úsáide as an algartam seo a leanas:

- Hash an eochair.
- Socraigh cén tábla hais agus an sliotán inar cheart an taifead seo a aimsiú.
- Déan tástáil ar an sliotán sonraithe sa tábla hash.

Le haghaidh cuardaigh eochracha le níos mó ná luach amháin, is féidir luachanna breise a fháil ach an cuardach a atosú ag an gcéad sliotán eile.

#### Gnéithe

Soláthraíonn struchtúr bunachar sonraí CDB roinnt gnéithe:

##### Cuardaigh tapa
Go hiondúil ní gá ach dhá dhiosca a rochtain chun cuardach rathúil i mbunachar sonraí ollmhór agus ní thógann sé ach ceann amháin chun cuardach nár éirigh leis.
##### Íseal lastuas
Úsáideann bunachar sonraí 2048 beart, 24 beart in aghaidh an taifid agus an spás le haghaidh eochracha agus sonraí.
##### Gan teorainn randamach
Is féidir le BFC aon bhunachar sonraí suas le 4 ghigibheart a bhainistiú. Ós rud é nach bhfuil aon srianta eile ann, ní gá go n-oireann na taifid fiú sa chuimhne. Stóráiltear bunachair shonraí i bhformáid meaisín neamhspleách.
##### Athsholáthar tapa bunachar sonraí adamhach
Is féidir leis an ordú **cdbmake** bunachar sonraí iomlán a athscríobh ina dhá ord méide, níos tapúla ná pacáistí hashing eile.
##### Dumpáil tapa bunachar sonraí
Is féidir le **cdbdump** a bhfuil i mbunachar sonraí a phriontáil i bhformáid cdbmake-comhoiriúnach.


## Tagairtí ##

* [cdb (bogearraí) - Vicipéid](https://ga.wikipedia.org/wiki/Cdb_(software))

* [sonraíocht CDB](http://cr.yp.to/cdb.html)


