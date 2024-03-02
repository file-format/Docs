{
  "date": "2021-06-09",
  "keywords": [
"cda",
"comhad",
"síneadh",
"formáid",
"cad is comhad cda ann",
"Ceol",
"formáid comhaid cda",
"Sonraíocht formáid comhaid cda"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid CDA agus APIanna ar féidir leo comhaid CDA a chruthú, a thiontú agus a oscailt.",
  "title": "CDA - Comhad Aicearra Rianta Fuaime CD",
  "linktitle": "CDA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-cda"
}
},
  "lastmod": "2021-06-09"
}

## Cad is comhad CDA ann?

Is éard atá i gcomhad le síneadh .cda ná stubchomhad beag ginte ag Microsoft Windows do gach rian fuaime ar CD fuaime. Tá gnáthfhaisnéis sna comhaid seo mar amanna riain agus aicearra Windows a chuireann ar chumas úsáideoirí rochtain a fháil ar na rianta fuaime ar leith. Ní ceol iad na comhaid CDA, ach tá siad ag díriú ar chomhad ceoil atá ann áit éigin ar an stór. Is féidir linn é a rá mar aicearra de chomhad fuaime atá suite ar CD.

## Formáid Comhaid CDA

Úsáidtear formáid comhaid CDA chun a insint do ríomhaire cén comhad fuaime atá le seinnt ar CD. Mar sin, éiríonn na comhaid CDA scartha óna chéile ó CD a seasann siad. Meastar go coitianta gur acmhainní RIFF iad na comhaid CDA. Níl ach smután amháin darb ainm CDDA agus níl ann ach bloc sonraí amháin ar a dtugtar FMT sa leagan reatha de chomhad .cda. Tá an bloc seo 24 beart ar fad. Úsáideann an tiomántán CD a bhaineann le Windows 95 agus Windows 98 an t-aitheantóir cruthaithe ag Windows agus ní féidir leis an seinnteoir a nascadh le FreeDB nó CDDB. Ionas gur féidir leis teideal an amhráin agus ainm an ealaíontóra a thaispeáint, a chaithfidh tú an fhaisnéis seo a chur isteach sa chomhad cdplayer.ini de láimh.

### Comhad CDA a eagrú

Léiríonn an tábla seo a leanas an fhaisnéis faoi ghnáthfhritháireamh:
| fhritháireamh | fad | ábhar |
---|---|---|
| 0x00 | 4 | na 4 charachtar ASCII RIFF |
| 0x04 | 4 | méid an smutáin seo a leanas: i gcónaí 36 (44 - 8), ar 4 beart (ord Intel) |
| 0x08 | 4 | chunk identifier: the 4 ASCII characters "CDDA"-ga |
| 0x0C | 4 | na 3 charachtar ASCII fmt agus spás ina dhiaidh |
| 0×10 | 4 | fad an smután: i gcónaí 24, ar 4 bytes (ordú Intel) |
| 0x14 | 2 | version of the CD format, on 2 bytes (Intel order). In May 2006, always equal to 1. |
| 0x016 | 2 | number of the range, on 2 bytes (Intel order). The first track has the number 1. |
| 0×18 | 4 | aitheantóir arna ríomh ag Windows le haghaidh cdplayer.exe. |
| 0x1c | 4 | fritháireamh raon, i líon na bhfrámaí (ordú Intel) |
| 0×20 | 4 | fad an riain, líon iomlán na bhfrámaí (ord Intel) |
| 0×24 | 1 | suíomh raon: frámaí |
| 0×25 | 1 | suíomh raon: soicind |
| 0×26 | 1 | suíomh raon: nóiméad |
| 0×27 | 1 | beart nialasach (luach dénártha 0) |
| 0×28 | 1 | fad an rian: frámaí |
| 0×29 | 1 | fad an riain: soicind |
| 0x2a | 1 | fad an riain: nóiméad |
| 0x2b | 1 | beart nialasach (luach dénártha 0) |

## Tagairtí

* [comhad .cda - Le Vicipéid](https://en.wikipedia.org/wiki/.cda_file)


