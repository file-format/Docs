{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid EDB - Comhad Bunachar Sonraí Ríomhphoist Mhalartaithe",
  "description": "Foghlaim faoi fhormáid comhaid EDB agus APIs ar féidir leo comhaid EDB a chruthú agus a oscailt.",
  "linktitle": "EDB",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ed-gab"
}
},
  "lastmod": "2020-09-16"
}

## Cad is comhad EDB ann?

Is bunachar sonraí bosca poist é comhad le síneadh comhad .edb a chruthaigh Microsoft Exchange Server chun sonraí a bhaineann le post a stóráil. Stórálann EDB, Malartú Bunachar Sonraí, teachtaireachtaí atá inphróiseála agus neamh-SMTP. Tugtar comhaid Bhunachair Sonraí Inneall Stórála In-Imlíne (ESE) ar EDB agus comhaid stórála ag baint úsáide as struchtúr b-crann. Ós rud é gur comhaid stórála iad, is féidir comhaid EDB a thiontú go formáidí comhaid stórála ríomhphoist eile ar nós [PST](/email/pst/) agus [OST](/email/ost/).

## Formáid Chomhaid EDB

Níl aon sonraíochtaí oifigiúla/oscailte formáid comhaid EDB ar fáil ar féidir tagairt a dhéanamh dóibh. Tá roinnt dul chun cinn déanta maidir le hinnealtóireacht droim ar ais ar an bhformáid comhaid, rud a d'fhág go ndearnadh cuid de na sonraíochtaí a dhíchódú. Mar atá siad seo, tá comhad EDB comhdhéanta de:
 * Ceanntásc Comhad - Tá eolas ceanntásca comhaid bunachar sonraí ann
 * Leathanaigh Mhéid Shocraithe - Tá an bunachar sonraí ina bhfuil táblaí agus innéacsanna ann

### Ceanntásc Comhad Bunachar Sonraí
Tá ceanntásc comhaid an bhunachair shonraí ar an gcéad leathanach den bhunachar sonraí agus is ionann é agus 668 beart ar a laghad. Tá `Leagan Formáide Comhad` agus `Cineál Comhaid` sa cheanntásc chomh maith le réimsí eile.

#### Cineálacha Comhad
|Cineál|Cur Síos
---|---|
|0| Bunachar Sonraí|
|1| Sruthú|

`Nóta:`Ní eol aitheantóirí na gcineálacha seo.

#### Leagan Formáid Comhaid
Cuireadh tús le leagan amach bunaidh an EDB i mí Aibreáin 1997 agus lean sé ag athrú le haghaidh athruithe ina dhiaidh sin.

|Revsion Date|Version|Revision|description
---|---|---|---|
| Aibreán 1997| 0x00000620|0x00000000| Formáid beta an chórais oibriúcháin bhunaidh.|
| Bealtaine 1997 |0x00000620|0x00000001| Cuir colúin sa chatalóg le haghaidh innéacsú coinníollach agus OLD.|
|Meitheamh 1997|0x00000620|0x00000002|Cuir an bhratach Téacs flocalized san IDB.|
|Deireadh Fómhair 1997|0x00000620|0x00000003|Cuir SPLIT_BUFFER le leathanaigh fhréamh chrainn spáis.|
|Ean 1998|0x00000620|0x00000002|Téigh an t-athbhreithniú ar ais le go bhfanfaidh ESE97 comhoiriúnach ar aghaidh.
||0x00000620|0x00000003|Cuir colúin nua clibeáilte leis an gcatalóg (CallbackData agus CallbackDependencies).|
|Bealtaine 1998|0x00000620|0x00000004|Tacaíocht Super Long Value (SLV): signSLV, fSLVExists in dbheader.|
|Bealtaine 1998|0x00000620|0x00000005|Crann nua spáis SLV.|
|Deireadh Fómhair 1998|0x00000620|0x00000006|Léarscáil spáis SLV.|
|Nollaig 1998|0x00000620|0x00000007|4-beart IDXSEG.|
|Eanáir 1999|0x00000620|0x00000008|Formáid cholúin teimpléid nua. ||
|Meitheamh 1999|0x00000620|0x00000009|Colúin teimpléid sórtáilte. Úsáidte i Windows XP SP3 |
||0x00000620|0x0000000b|Tá ceanntásc an leathanaigh ann leis an tseic ECC a úsáidtear mar mhalartú|
||0x00000620|0x0000000c|A úsáidtear in Windows Vista (SP0)|
||0x00000620|0x00000011|Tacaíocht le haghaidh 2 leathanach KiB, 16 KiB agus 32 KiB. Ceanntásc leathnaithe leathnaithe le seiceálacha breise ECC.Comhbhrú colún. Leideanna spáis.Úsáidte i Windows 7 (SP0)|
|Bealtaine 1999|0x00000623|0x00000000|Bainisteoir Nua Spáis.|

### Comhaid Bunachar Sonraí

Tá scéimre do na táblaí go léir sa bhunachar sonraí i gcomhad bhunachar sonraí an EDB. Ina theannta sin, folaíonn sé freisin taifid do na táblaí bunachar sonraí go léir agus innéacsanna do na táblaí. Cinntear a suíomh ag na haitheantóirí seo a leanas.

* JetCreateDatabase

* JetCreateDatabase2

* Bunachar Sonraí JetAttach

* Bunachar Sonraí JetAttach2


Bunaithe orthu seo, is féidir staid an bhunachair shonraí a mheas mar seo a leanas.

|Luach|Aitheantóir|Cur Síos
---|---|---|
|1|JET_dbstateJustCreated|Cruthaíodh an bunachar sonraí díreach.|
|2|JET_dbstateDirtyShutdown|Tá an bunachar sonraí de dhíth le hathshlánú crua nó bog a rith chun go mbeidh sé inúsáidte nó inaistrithe. Níor cheart iarracht a dhéanamh bunachair shonraí a bhogadh sa stát seo.|
|3|JET_dbstateCleanShutdown|Tá an bunachar sonraí i riocht glan. Is féidir an bunachar sonraí a cheangal gan aon logchomhaid.|
|4|JET_dbstateBeingConverted|Tá an bunachar sonraí á uasghrádú.|
|5|JET_dbstateForceDetachInternal|Tugtar an luach seo isteach in WindowsXP|
 
## Tagairtí
 * [Sonraíochtaí Comhad Bunachar Sonraí Inneall Stórála In-Imlíne (ESE) (EDB)](https://github.com/libyal/libesedb/tree/main/documentation)

