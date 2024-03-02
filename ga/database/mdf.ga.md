{
  "date": "2020-11-11",
  "keywords": [
"MDF",
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
  "description": "Foghlaim faoi fhormáid comhaid MDF agus APIanna ar féidir leo comhaid MDF a chruthú agus a oscailt.",
  "title": "Formáid Comhad MDF - Comhad Bunachar Sonraí Máistir Freastalaí SQL",
  "linktitle": "MDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-gaf"
}
},
  "lastmod": "2020-08-12"
}

## Cad is comhad MDF ann?

Is Máistirchomhad Bunachar Sonraí é comhad a bhfuil iarmhír .mdf air a úsáideann [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) chun sonraí úsáideoirí a stóráil. Tá sé ríthábhachtach mar go bhfuil na sonraí go léir stóráilte sa chomhad seo. Stórálann an comhad MDF sonraí úsáideoirí i mbunachair shonraí choibhneasta sna colúin fhoirmeacha, sna sraitheanna, sna réimsí, sna hinnéacsanna, sna hamharcanna agus sna táblaí. Ceadaíonn Freastalaí SQL socruithe uathfhás agus uathchrapadh a shocrú chun tionchar dearfach a bheith acu ar fheidhmíocht an bhunachair sonraí. Is féidir comhaid MDF a luchtú agus a cheangal le bunachar sonraí ag baint úsáide as Microsoft SQL Server. Tá cineál MIME Feidhmchlár/octet-sruth ag comhaid MDF.

## Formáid Comhaid MDF

Is leathanach é an t-aonad bunúsach stórála sonraí i SQL Server. Roinntear leathanach stórála sannta bunachar sonraí ina leathanaigh loighciúla a bhfuil uimhriú orthu ó 0 go n. Tosaíonn leathanach amháin le ceanntásc 96 beart a chuimsíonn ID an Leathanaigh, an cineál struchtúir lena mbaineann an leathanach, líon na dtaifead ar an leathanach, agus leideanna chuig na leathanaigh roimhe seo agus na chéad leathanaigh eile.

### Struchtúr Comhaid

Tá an struchtúr sonraí seo a leanas ag comhad MDF.

 * Leathanach 0: Ceanntásc
 * Leathanach 1: An Chéad PFS
 * Leathanach 2: An Chéad GAM
 * Leathanach 3: An Chéad SGAM
 * Leathanach 4: Gan úsáid
 * Leathanach 5: Gan úsáid
 * Leathanach 6: An Chéad DCM
 * Leathanach 7: An Chéad BCM

#### Ceanntásc an Chomhaid

Tá ceanntásc ar leathanaigh uimhir 0 de na comhaid go léir a stórálann meiteashonraí faoin gcomhad.

#### Spás Saor Leathanach (PFS)
Aithníonn PFS an stádas leithdháilte agus cinneann sé méid an spáis saor.

 * Giotán 1: Léiríonn sé an bhfuil an leathanach leithdháilte nó nach bhfuil.
 * Giotán 2: Léiríonn sé an bhfuil an leathanach ó mhéid measctha.
 * Giotán 3: Tugann sé le fios gur leathanach IAM é an leathanach seo.
 * Giotán 4: Tugann sé le fios go bhfuil taifid thaibhse ar an leathanach seo
 * Giotán 5 go 7: Comhluach trí ghiotán, a léiríonn iomláine an leathanaigh mar seo a leanas:
   * 0: Tá an leathanach folamh
   * 1: Tá an leathanach 1–50% lán
   * 2: Tá an leathanach 51–80% lán
   * 3: Tá an leathanach 81–95% lán
   * 4: Tá an leathanach 96–100% lán

## Tagairtí

 * [Comhaid Bunachar Sonraí agus Grúpaí Comhad](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Bunachar Sonraí Dícheangail agus Ceangail - Freastalaí SQL](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- leagan 15)
 * [Anailís a dhéanamh ar Anatamaíocht Chomhad Sonraí Freastalaí SQL](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

