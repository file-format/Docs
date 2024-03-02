{
  "date": "2021-04-21",
  "keywords": [
"comhad pea",
"formáid comhaid pea",
"cad is comhad pea ann",
"comhad",
"sampla pea",
"síneadh comhad pea",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEA - Formáid Chomhaid Cartlainne PeaZip",
  "description": "Foghlaim faoi fhormáid comhaid PEA agus APIs ar féidir leo comhaid PEA a chruthú agus a oscailt.",
  "linktitle": "PEA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pe-gaa"
}
},
  "lastmod": "2021-04-21"
}

## Cad is comhad PEA ann?

Is cartlann [zip](/compression/zip/) é comhad a bhfuil iarmhír .pea air, acrainm do Pack, Encrypt, and Authenticate, a cruthaíodh le feidhmchlár cartlannaithe [PeaZip](https://peazip.github.io/). Gnéithe sé comhbhrú agus aschur toirte iolrach, agus cuireann sé múnla slándála solúbtha trí Criptiú Fíordheimhnithe agus cripteagrafaíochta. Soláthraíonn sé seo príobháideacht agus fíordheimhniú na sonraí araon. Tá an fóntais PeaZip ar fáil mar inneall foinse oscailte is féidir a chur le chéile le haghaidh OS éagsúla de réir riachtanas.

## Formáid Comhaid PEA

Tá na [PEA file format specifications](https://peazip.github.io/pea_help.pdf) ar fáil go poiblí mar thagairt ón bhforbróir. Is comhaid dhénártha iad cartlanna PEA le samhail slándála solúbtha agus seiceálacha sláine iomarcacha ó sheiceanna go hashes láidir cripteagrafach. Sainmhíníonn sé seo trí leibhéal éagsúla cumarsáide le rialú:

 * Sruthanna - an sruth sonraí aschuir iarbhír a fhoirmítear trí chomhaid ionchuir iolracha agus is féidir iad a scríobh go dtí méideanna aschuir iolracha
 * Cuspóirí - comhaid ionchuir agus fillteáin seolta chuig cartlann .pea
 * Imleabhair - comhad cartlainne aschuir is féidir a shíneadh go méid sainithe úsáideora

Tá gach ceann díobh seo roghnach agus is féidir iad a ionchorprú de réir riachtanais an úsáideora. Is féidir le formáid comhaid PEA sruth amháin a stóráil ina bhfuil rudaí gan teorainn. Tá gach sruth suas le 2^64 beart i méid.

Tairgeann comhaid PEA seiceáil sláine roghnach agus criptiú fíordheimhnithe ag baint úsáide as AES i mód EAX nó HMAC, mar mhalairt air sin Twofish agus Serpent i mód EAX.

### Ceanntásc Cartlainne PEA

10 mbeart atá i gceanntásc na cartlainne agus tá sé struchtúrtha mar seo a leanas.

| Beart | Cur síos |
---|---|
|1 | Réimse beart draíochta le haghaidh dí-athbhrí formáide comhaid: $EA|
|1 | Uimhir Leagan|
|1 | Uimhir Athbhreithnithe|
|1 | Scéim rialaithe toirte|
|1 | Ag dearbhú an OS inar tógadh an sruth|
|1 | Ionchódú dáta agus ama an OS á dhearbhú|
|1 | Rudaí á dhearbhú, ainm ionchódú carachtar|
|1 | Ag dearbhú cineál LAP (ionchódaithe i 7 giotán) agus endianness (i msb)|
|1 | Forchoimeádta le húsáid sa todhchaí|

## Tagairtí

* [Sonraíochtaí Formáid Comhaid PEA](https://peazip.github.io/pea_help.pdf)

* [Formáid Comhaid PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)


