{
  "date": "2019-12-12",
  "keywords": [
"SQLite",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid SQLITE agus APIanna ar féidir leo comhaid SQLITE a chruthú agus a oscailt.",
  "title": "Formáid Comhaid SQLite",
  "linktitle": "SQLITE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sqlit-gae"
}
},
  "lastmod": "2020-11-09"
}

## Cad is Comhad SQLite ann?

Is comhad éadrom bunachar sonraí SQL é comhad a bhfuil iarmhír .sqlite air a cruthaíodh leis na bogearraí [SQLite](https://www.sqlite.org/index.html). Is bunachar sonraí i gcomhad é féin agus cuireann sé inneall bunachair sonraí [SQL](/database/sql/) atá féinchuimsitheach, lán-léirithe, an-iontaofa i bhfeidhm. Is féidir comhaid bhunachar sonraí SQLite a úsáid chun inneachar saibhir a roinnt idir córais trí na comhaid seo a mhalartú go simplí thar an líonra. Úsáideann beagnach gach fón póca agus ríomhaire SQLite chun sonraí a stóráil agus a roinnt, agus is é an rogha formáid comhaid é d’fheidhmchláir tras-ardáin. Mar gheall ar a úsáid dhlúth agus inúsáidteacht éasca, tagann sé cuachta taobh istigh d'iarratais eile. Tá ceangail SQLite ann do theangacha ríomhchlárúcháin mar C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/), agus go leor eile.

## Formáid Comhaid SQLite

Is leabharlann C-Teanga é SQLite a chuireann an SQLite RDBMS i bhfeidhm ag baint úsáide as formáid comhaid SQLite. Agus gléasanna nua ag teacht chun cinn gach lá, coinníodh a bhformáid comhaid ar gcúl chun freastal ar ghléasanna níos sine. Feictear formáid comhaid SQLite mar fhormáid chartlainne fhadtéarmach do na sonraí.

### An Comhad Bunachar Sonraí

Coinnítear bunachar sonraí SQLite go hiomlán trí dhá chomhad.
 * Príomhchomhad bunachar sonraí - Tá staid iomlán bhunachar sonraí SQLite ann
 * Rollback Journal - Stórálann faisnéis bhreise i gcomhad eile agus úsáidtear é le linn idirbhearta a dhéanamh. Sa chás go bhfuil SQLite i mód WAL, coinnítear logchomhad ceannscríofa.

#### Comhad Dialainne

Tá sé mar aidhm ag an gcomhad seo an fhaisnéis go léir a choimeádtar ar eagla nach bhféadfaí an t-idirbheart deireanach a chur i gcrích i gcásanna ar nós tuairteála ríomhaire. Úsáidtear an comhad seo chun an comhad bunachar sonraí a chur ar ais go staid chomhsheasmhach.

#### Leathanaigh

Cuimsíonn príomhchomhad bhunachar sonraí SQLite leathanach amháin nó níos mó. Ag am ar bith, tá úsáid amháin ag gach leathanach sa phríomhbhunachar sonraí atá ar cheann díobh seo a leanas:

 * An leathanach glas-beart
 * Leathanach liosta saor in aisce,
   * Leathanach teidil saor in aisce,
   * Leathanach duille saor in aisce,
 * Leathanach crann b
   * Leathanach taobh istigh tábla b-crann
   * Leathanach duille tábla b-crann
   * Leathanach taobh istigh innéacs b-crann
   * Leathanach duille innéacs b-crann
 * Leathanach thar maoil pá
 * Leathanach léarscáil pointeoir

Is féidir le méid comhaid bhunachar sonraí SQLite raon ó chúpla cilibheart go dtí cúpla ghigibheart.

### Ceanntásc SQLite

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Tá sonraí na réimsí ceanntásca mar atá sa tábla seo a leanas.

|Fritháireamh|Méid|Cur Síos|
---|---|---|
|0|16|An teaghrán ceanntásca: Formáid SQL 3\000|
|16|2|Méid leathanach an bhunachair shonraí i mbearta. Ní mór dó a bheith ina chumhacht de dhá cheann idir 512 agus 32768 agus an dá cheann san áireamh, nó luach 1 a sheasann do mhéid leathanaigh 65536.|
|18|1|An leagan scríobh formáid comhaid. 1 le haghaidh oidhreacht; 2 le haghaidh WAL.|
|19|1|Leagan le formáid comhaid. 1 le haghaidh oidhreacht; 2 le haghaidh WAL.|
|20|1|Biotáil de spás forchoimeádta nár úsáideadh ag deireadh gach leathanaigh. De ghnáth 0.|
|21|1|Codán pálasta leabaithe uasta. Caithfidh sé a bheith 64. |
|22|1|Codán pá-ualaigh íosta leabaithe. Caithfidh sé a bheith 32.|
|23|1|Codán pálasta duillí. Caithfidh sé a bheith 32.|
|24|4|Cuntasaí athraithe comhad.|
|28|4|Méid an chomhaid bhunachair sonraí sna leathanaigh. An méid an bhunachair shonraí i gceanntásca.|
|32|4|Uimhir leathanaigh an chéad leathanach trunc saorliosta.|
|36|4|Líon iomlán na leathanach saorliosta.|
|40|4|An fianán scéimre.|
|44|4|Uimhir fhormáide na scéimre. Is iad na formáidí scéimre tacaithe ná 1, 2, 3, agus 4.|
|48|4|Méid réamhshocraithe taisce an leathanaigh.|
|52|4|Uimhir leathanaigh leathanach an chrainn b fréimhe is mó nuair atá sé i módanna uathfholús nó incriminteach-folús, nó náid ar shlí eile.|
|56|4|The database text encoding. A value of 1 means UTF-8. Ciallaíonn luach 2 UTF-16le. Ciallaíonn luach 3 UTF-16be.|
|60|4|An leagan úsáideora mar atá léite agus socraithe ag an pragma user_version.|
|64|4|Fíor (neamh-nialas) don mhód incriminteach-folúis. Bréagach (nialas) ar shlí eile.|
|68|4|An Aitheantas Feidhmchláir arna shocrú ag PRAGMA application_id.|
|72|20|Forchoimeádta lena leathnú. Ní mór a bheith nialas.|
|92|4|An leagan-bailí don uimhir.|
|96|4|SQLITE_VERSION_NUMBER|

## Tagairtí ##

* [Formáid Comhaid SQL - SQLite](https://www.sqlite.org/fileformat2.html)

* [SQLite - Vicipéid](https://ga.wikipedia.org/wiki/SQLite)

* [SQLite - Sonraíochtaí Teanga C](https://www.sqlite.org/c3ref/intro.html)


