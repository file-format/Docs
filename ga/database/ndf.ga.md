{
  "date": "2020-11-11",
  "keywords": [
"NDF",
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
  "description": "Foghlaim faoi fhormáid comhaid MDF agus APIanna ar féidir leo comhaid NDF a chruthú agus a oscailt.",
  "title": "Formáid Comhad NDF - Comhad Bunachar Sonraí Máistir Freastalaí SQL",
  "linktitle": "NDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nd-gaf"
}
},
  "lastmod": "2020-08-12"
}

## Cad is comhad NDF ann?

Is comhad bunachar sonraí tánaisteach é comhad le iarmhír .ndf a úsáideann [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) chun sonraí úsáideoirí a stóráil. Is comhad stórála tánaisteach é NDF toisc go stórálann freastalaí SQL sonraí úsáideora sonraithe sa phríomhchomhad stórála ar a dtugtar [MDF](/database/mdf/). Tá comhad sonraí an NDF roghnach agus sainítear é don úsáideoir chun stóráil sonraí a bhainistiú ar eagla go n-úsáideann an príomhchomhad MDF an spás leithdháilte ar fad. De ghnáth déantar é a stóráil ar dhiosca ar leith agus féadann sé scaipeadh chuig ilfheistí stórála. Tá gá le comhaid MDF a bheith ann chun comhaid NDF a oscailt.

## Formáid Comhaid NDF

Níl aon difríocht idir formáid comhaid NDF agus [MDF](/database/mdf/) agus úsáidtear leathanaigh mar bhunaonad stórála sonraí. tosaíonn gach leathanach le ceanntásc 96 beart a chuimsíonn:

 * ID leathanaigh
 * Cineál Struchtúir
 * Líon na dtaifead sna leathanaigh
 * Leideanna chuig na leathanaigh roimhe seo agus na chéad leathanaigh eile

### Struchtúr Comhad NDF

Tá an struchtúr sonraí seo a leanas ag comhad MDF.

 * Leathanach 0: Ceanntásc
 * Leathanach 1: An Chéad PFS
 * Leathanach 2: An Chéad GAM
 * Leathanach 3: An Chéad SGAM
 * Leathanach 4: Gan úsáid
 * Leathanach 5: Gan úsáid
 * Leathanach 6: An Chéad DCM
 * Leathanach 7: An Chéad BCM

#### Ceanntásc Comhad NDF

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

## Leathanach Comhad Sonraí

Tosaíonn leathanaigh i gcomhad sonraí SQL Server ó nialas (0) agus incrimint go seicheamhach. Aithnítear gach comhad le huimhir aitheantais comhaid uathúil. Aithníonn ID an chomhaid agus an péire uimhir leathanaigh leathanach i mbunachar sonraí. Tá sampla a thaispeánann uimhreacha na leathanach i mbunachar sonraí mar atá san íomhá seo a leanas.

{{< figure src="../ndf.png" alt="Formáid Comhaid Bunachar Sonraí NDF" >}}

Taispeánann an sampla seo uimhreacha na leathanach i mbunachar sonraí ina bhfuil comhad sonraí príomhúla 4-MB agus comhad sonraí tánaisteacha 1-MB.

## Tagairtí

 * [Comhaid Bunachar Sonraí agus Grúpaí Comhad](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
 * [Bunachar Sonraí Dícheangail agus Ceangail - Freastalaí SQL](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- leagan 15)
 * [Anailís a dhéanamh ar Anatamaíocht Chomhad Sonraí Freastalaí SQL](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

