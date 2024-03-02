{
  "date": "2020-11-11",
  "keywords": [
"BAK",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid BAK",
"Síneadh Comhad BAK",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid BAK agus APIanna ar féidir leo comhaid BAK a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid BAK - Comhad Cúltaca Bunachar Sonraí",
  "linktitle": "BAK",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ba-gak"
}
},
  "lastmod": "2020-12-04"
}

## Cad is comhad BAK ann?

De ghnáth is comhad cúltaca é comhad le síneadh .bak a úsáideann uirlisí bogearraí éagsúla chun cúltacaí sonraí a stóráil. Ó thaobh an bhunachair shonraí de, úsáideann Microsoft SQL Server comhad BAK chun ábhar bunachar sonraí a stóráil. Stóráiltear na sonraí agus na comhaid go léir a bhaineann leis an mbunachar sonraí san fhormáid comhaid seo le haisghabháil ar eagla go n-éireoidh an bunachar sonraí truaillithe nó neamhbhailí ar chúis ar bith. Is féidir na comhaid chúltaca a stóráil agus a innéacsú ar fhreastalaithe eile chun críche sábháilteachta. Is féidir le roinnt feidhmchlár comhaid BAK a chruthú mar SQL Server Management Studio, Transact-SQL, agus Windows PowerShell.

## Formáid Chomhaid BAK

Ní fios sonraí inmheánacha comhad BAK ach glactar leis go forleathan go bhfuil sé bunaithe ar Fhormáid Téip Microsoft (MTF). Tá sonraíochtaí MTF ar fáil agus is féidir tagairt a dhéanamh dóibh chun struchtúr an chomhaid a thuiscint. Soláthraíonn an doiciméad sonraí maidir le stóráil MTF d'aon duine a bhfuil eolas ginearálta aige faoi oibríochtaí bainistíochta stórála, tiomántáin téipe, agus córais comhaid.

### Tacar Sonraí

Is éard is tacar sonraí ann ná bailiúchán rudaí a scríobhtar chuig meán stórála (téip, diosca optúil, etc.) le linn cúltaca nó athchóiriú sonraí. Cuimsíonn tacair sonraí meáin iolracha i gcás líon mór sonraí.

### Eilimintí Bunúsacha MTF

Is éard atá i gcomhad MTF roinnt gnéithe bunúsacha a chomhdhéanann a bloic thógála. Is iad na heilimintí seo:

#### Bloic Tuairisceora

Úsáidtear bloic tuairisceora (DBLK) chun formáid a rialú agus is iad na bunsraitheanna is mó do chomhad MTF. Sainmhíníonn comhad MTF amháin DBLKanna iolracha do gach ról ar leith. Is bloc fad athraitheach sonraí é gach DBLK atá roinnte ina cheithre chuid:

 * `Ceanntásca Coitianta` - Struchtúr fad seasta atá comónta do gach DBLK. Is é seo an t-aon Bloc Ceanntásc atá ag teastáil.
 * `Faisnéis Chineál DBLK` - Bloc Fad Seasta a bhaineann go sonrach leis an gcineál DBLK atá á shainiú
 * `Sonraí an Chórais Oibriúcháin` - Sonraí sonracha a shainmhínítear bunaithe ar chineál na gcóras DBLK agus Oibriúcháin
 * `Faisnéis DBLK` - Faisnéis shainiúil DBLK ar fhad athraitheach nach féidir a shábháil leis an bhfaisnéis DBLK Fad Seasta.

{{< figure src = ../bak.png alt=Formáid Comhaid Chúltaca Microsoft SQL> }}

#### Sruth Sonraí

Úsáidtear sruthanna sonraí i gcomhad MTF chun sonraí a chuimsiú agus a ailíniú. Cuimsíonn sé Ceanntásc Sruth, agus Sonraí Srutha ina dhiaidh sin. Ní féidir le ceanntásc srutha ach cineál amháin Sonraí Srutha a chuimsiú.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL Formáid Comhad Cúltaca" >}}

####Marcanna Comhad

Úsáidtear comhadmharc le haghaidh scaradh loighciúil agus rochtain thapa laistigh de mheán. Déanann tiománaí an ghléis aithris ar na comharthaí comhad nó trí úsáid a bhaint as an mbloc Tuairisceoir Comhad Bog ar chás nach soláthraíonn an gléas atá á úsáid marcanna comhaid.

## Comhaid BAK eile

Seo cineálacha comhaid eile a úsáideann an síneadh comhad **.bak**.

**Bunachar Sonraí**
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**cluiche**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Misc**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Socruithe**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Tagairtí ##

* [[MS-BCP]: Formáid Cóipe Bulc](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


