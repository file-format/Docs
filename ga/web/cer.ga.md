{
  "date": "2021-07-13",
  "keywords": [
"CER",
"síneadh",
"comhad",
"formáid",
"gréasáin",
"teastas",
"teanga"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CER - Formáid Chomhaid Deimhnithe",
  "description": "Foghlaim faoi fhormáid comhaid CER agus APIanna ar féidir leo comhaid CER a chruthú agus a oscailt.",
  "linktitle": "CER",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ce-gar"
}
},
  "lastmod": "2021-07-13"
}

## Cad is comhad CER ann? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. Is iad na húdaráis deimhnithe atá urraithe go sonrach iad siúd a bhaineann le HTTPS, prótacal brabhsála a bhfuil muinín ann agus a bhfuil muinín ann  
Is deimhniú do fhreastalaí é an CER. Faigheann údarás deimhniúcháin an fhearainn é de ghnáth. Meastar go bhfuil CER mar an gcéanna le [CRT](/web/crt/) den chuid is mó, cé go bhfuil an dá fhormáid chéanna de theastas SSL ach gur síntí difriúla ainm comhaid iad.
Is féidir iad seo a úsáid ar chórais oibriúcháin ach brabhsálaí a oscailt agus slándáil an bhrabhsálaí nó an tsuímh Ghréasáin atá á úsáid a sheiceáil.

## Stair Ghearr ##

Sa bhliain 1995, tháinig Thawte ar an gcéad údarás deimhniúcháin chun eisiúint na ndeimhnithe poiblí SSL (nasc soicéad daingnithe) as na SA a réiteach. Ina dhiaidh sin, tá sraith údarás den sórt sin a bunaíodh ó 1995 go 2020.

## Formáid Chomhaid CER ##

Is féidir na comhaid seo a bheith simplí
* Cuimsíonn an PKC S#7 ionchódú Base64 ASCII
* Is iad na síntí comhad atá aige ná p7b nó p7cZ
* Maidir le hábhar dénártha, is é DER nó pkcs12/pfx an deimhniú.
Tá go leor cineálacha comhaid deimhnithe ann le roinnt sonraíochtaí uathúla:
* .pem, Nuair a úsáideann eagraíocht a shlabhraíonn an fhormáid seo is eol go maith deimhnithe a chruthú
* .arm, nuair is gá an modh chun deimhniú a bhaint as féin-shínithe, is é .arm an fhormáid shonraithe chun na críche sin. Léirítear é in ionchódú bonn-64 ASCII.
* .der, Tá sé comhdhéanta de shonraí dénártha. Ciallaíonn sé seo gur féidir é a úsáid le haghaidh teastas aonair amháin
* .pfx (PKC512), Is éard atá ann eochair phríobháideach a fhreagraíonn do dheimhniú arna eisiúint ag CA nó deimhniú féin-shínithe. Tá an-aithne ar an bhformáid seo as cur i bhfeidhm SSL amháin a thiontú go ceann eile.


