{
  "date": "2019-10-11",
  "keywords": [
"comhad gz",
"formáid comhaid gz",
"cad is comhad gz ann",
"comhad",
"gz shampla",
"síneadh comhad gz",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid GZ - Comhad Cartlainne GNU Zipped",
  "description": "Foghlaim faoi cad is comhad GZ ann agus APIanna ar féidir comhaid GZ a chruthú agus a oscailt.",
  "linktitle": "GZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-g-gaz"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad GZ ann?

Is cartlann chomhbhrúite é comhad GZ a chruthaítear leis an ngnáth-algartam comhbhrú [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Féadfaidh sé go bhfuil comhaid chomhbhrúite iolracha, eolairí agus stubs comhad. Forbraíodh an fhormáid seo ar dtús chun formáidí comhbhrú a athsholáthar ar chórais UNIX. agus tá sé fós ar cheann de na cineálacha cartlainne is coitianta ar chórais Linux. Is féidir le feidhmchláir ar nós [WinZip](https://www.winzip.com/en/) comhaid GZ a oscailt chun a bhfuil iontu a fheiceáil ar Windows agus MacOS araon.

## Formáid Chomhaid GZ - Tuilleadh Eolais

Úsáideann Gzip an algartam [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) chun cartlann a chomhbhrú agus tá sé difriúil leis an bhformáid cartlainne [ZIP](/compression/zip/) chun an t-algartam comhbhrú a chur i bhfeidhm ar chartlann iomlán seachas ar chomhaid aonair. Tá faisnéis mhionsonraithe faoin bhformáid comhaid i sonraíochtaí formáid comhaid GZIP leagan 4.3 arna fhoilsiú ag Internet Engineering Task Force (IETF). Cuimsíonn formáid an chomhaid:

* Ceanntásc Comhad

* Ceanntásca Roghnacha

* Sonraí Comhbhrúite

* Buntásc an Chomhaid


## Ceanntásc Comhad GZ ##

Tá 10 mbeart i gceanntásc an chomhaid GZ mar a leanas:

|Fritháireamh|Méid|Luach|Cur Síos
---|---|---|---|
|0|2|0x1f 0x8b|Uimhir dhraíochtúil lena sainaithnítear an cineál comhaid
|2|1| |Compression Method * 0-7 (Forchoimeádta) * 8 (Deflate)
|3|1| |Bratacha Comhad
|4|4| |stampa ama 32-giotán
|8|1| | Bratacha comhbhrú
|9|1| |Aitheantas an chórais oibriúcháin

### Bratacha an Chomhaid ###

|Luach|Aitheantóir|Cur Síos
---|---|---|
|0x01|FTEXT|Má tá sé socraithe ní mór caitheamh leis na sonraí neamh-chomhbhrúite mar théacs in ionad sonraí dénártha. Tugann an bhratach seo le fios tiontú deireadh-líne do chomhaid téacs tras-ardáin ach ní fhorfheidhmíonn sé é.
|0x02|FHCRC|Tá seiceáil ceanntásca (CRC-16) sa chomhad
|0x04|FEXTRA|Tá réimsí breise sa chomhad
|0x08|FNAME|Tá teaghrán ainm comhaid bunaidh sa chomhad
|0x10|FCOMMENT|Tá trácht sa chomhad
|0×20| |Ar cosaint
|0×40| |Ar cosaint
|0×80| |Ar cosaint

### Córas oibriucháin ###

|Luach|Cur Síos
---|---|
|0|Córas comhaid Saille (MS-DOS, OS/2, NT/Win32)
|1|Aimig
|2|VMS (nó OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|Córas comhad HPFS (OS/2, NT)
|7|Macintosh
|8|Córas Z
|9|CP/M
|10|BARR-20
|11|Córas comhad NTFS (NT)
|12|QDOS
|13|RISCOS Dearcán
|255|anaithnid

## Ceanntásca Roghnacha GZ ##

Is iad na ceannteidil bhreise roghnacha iad siúd atá sainithe ag bratacha an chomhaid agus áirítear leo faisnéis ar nós ainm an chomhaid bhunaidh, réimsí breise, nótaí tráchta agus seiceála ceanntásca.

## Sonraí Comhbhrúite ##

Tá na sonraí comhbhrúite ag baint úsáide as an algartam comhbhrúite DEFLATE sa chuid seo.

## Buntásc Comhad GZ ##

Tá buntásc an chomhaid 8 mbeart agus tá an fhaisnéis seo a leanas ann.

|Fritháireamh|Méid|Cur Síos
---|---|---|
|0|4|Seic (CRC-32)
|4|4|Luach méid sonraí neamh-chomhbhrúite i mbearta

## Tagairtí ##

* [gzip - Vicipéid](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: Sonraíocht formáid comhaid GZIP](https://datatracker.ietf.org/doc/html/rfc1952), le IETF.


