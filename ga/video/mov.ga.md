{
  "date": "2019-10-11",
  "keywords": [
"comhad mov",
"Formáid comhaid mov",
"Cad is comhad mov ann",
"comhad",
"sampla mov",
"Síneadh comhad mov",
"síneadh",
"formáid",
"QuickTime",
"MPEG-4"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad MOV - Formáid Chomhaid Scannán Apple QuickTime",
  "description": "Foghlaim faoi fhormáid comhaid MOV agus APIs ar féidir leo comhaid MOV a chruthú agus a oscailt.",
  "linktitle": "MOV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mo-gav"
}
},
  "lastmod": "2021-07-29"
}

## Cad is comhad MOV ann?

Is cineál comhaid físe é comhad MOV, arna fhorbairt ag Apple Inc., ina bhfuil rian amháin nó níos mó. Stórálann gach rian scannán, fuaime, gearrthóga scannáin agus fotheidil. Is coimeádán ilmheán é atá in ann cineálacha éagsúla eilimintí meáin a stóráil. Tá formáid físeán MOV ag luí leis an dá Windows agus córais Macintosh. Úsáideann sé MPEG-4 códaithe le haghaidh comhbhrú agus coinnítear rianta i rudaí ar a dtugtar adaimh a chuirtear i struchtúr ordlathach sonraí.

## Stair Achomair ar Formáid Chomhaid MOV

MPEG-4 file format has evolved from QuickTime File Format (**QTFF**) specification in 2001. Cheadaigh Eagraíocht Idirnáisiúnta na gCaighdeán an fhormáid agus foilsíodh sonraíochtaí córais MPEG-4 Cuid 1 i 1999. In 2001, foilsíodh formáid comhaid athbhreithnithe [MP4](/video/mp4/).

Athbhreithníodh an chéad leagan de MP4 in 2003 mar MPEG-4 Cuid 14 (ISO/IEC 14496-14:2003). Sa bhliain 2004, rinneadh MP4 a ghinearálú chun struchtúr ginearálta a shainiú do gach comhad meán ama-bhunaithe. Dá bhrí sin, anois tá sé in úsáid mar bhonn le haghaidh formáidí comhaid ilmheán éagsúla eile.

## Formáid Chomhaid QuickTime (QTFF) - Tuilleadh Eolais

D'fhonn oibriú le ilmheán digiteach, is féidir le QTFF go leor cineálacha sonraí a choinneáil. Is formáid smaointe é le haghaidh malartú meán digiteach mar go sainmhíníonn an fhormáid na caighdeáin chun cur síos a dhéanamh ar aon chineál struchtúir meán. Is éard atá i bhformáid an chomhaid ná bailiúchán solúbtha de réada atá dírithe ar oibiachtaí. Chun scannáin a stóráil ar dhioscaí, úsáideann QuickTime dhá struchtúr ie `adaimh` agus `adaimh QT`.

### Adamh

Is é Atom bunaonad an chomhaid QuickTime. Tá dhá mhórréimse in aon adamh roimh aon réimse eile: Réimsí Méid agus Cineál. Léiríonn an réimse méide méid an adaimh agus léiríonn an réimse cineál an cineál sonraí atá stóráilte san adamh. De réir an dúlra, tá adaimh ordlathach, rud a chiallaíonn gur féidir adaimh amháin a bheith ann a bhféadfadh adaimh eile a bheith iontu fós. Taispeántar leagan amach adaimh samplach san íomhá seo a leanas.

Tá dhá chuid ag gach adamh, `ceanntásc`, agus `sonraí`. Tá na réimsí méid agus cineál sa cheanntásc agus tá na sonraí iarbhír sa chuid sonraí. Ina theannta sin, mínítear gach réimse thíos:

### Méid an Adaimh

Léirítear ceanntásc agus inneachar an adaimh le slánuimhir 32-giotán ar a dtugtar méid an adaimh. Cuimsíonn an réimse méide méid an adaimh i mbearta, arna shloinneadh i slánuimhir 32-giotán gan síniú.

### Cineál Adaimh

Taispeántar cineál an adaimh freisin le slánuimhir 32-giotán, a láimhseáiltear den chuid is mó mar réimse ceithre charachtar le luach knemonic, mar 'moov' (0x6D6F6F76) le haghaidh adamh scannáin, nó 'trak' (0x7472616B) le haghaidh adamh rian. Nuair a bhíonn an cineál adaimh ar eolas, ceadaíonn sé a chuid sonraí a léirmhíniú.

### Adaimh QT agus Coimeádáin Adaimh

Soláthraíonn adaimh QT formáid stórála ilchuspóireach agus tá ceanntásc leathnaithe acu comhdhéanta de réimsí Méid, Cineál, ID Adaimh, agus Comhaireamh Leanaí. Tá adaimh QT fillte i gcoimeádán adaimh, struchtúr sonraí uathúil a bhfuil ceanntásc le comhaireamh glas. Tá fréimhe amháin i ngach coimeádán adaimh, is é sin an t-adamh QT. Taispeántar leagan amach an adaimh QT san fhíor thíos.

Tá na sonraí seo a leanas ag ceanntásc coimeádán adamh QT:

Curtha in áirithe: Eilimint 10 beart a bhfuil luach 0 uirthi.

Comhaireamh Glais: slánuimhir 16-giotán le luach 0.

Tá na sonraí seo a leanas ag ceanntásca adaimh QT:

**Méid -** Léirítear ceanntásc adaimh QT agus inneachar i mbeart le slánuimhir 32-giotán. I gcás adamh duille, tá méid adaimh amháin sa réimse seo.

**Cineál -** Léirítear cineál an adaimh le slánuimhir 32-giotán. Sa chás gurb é an bunadamh é, socraítear an luach go 'sean'.

**Aitheantas Adamh -** Is slánuimhir 32-giotán é a thaispeánann an t-aitheantas adaimh agus caithfidh sé a bheith uathúil do gach siblín. Fréamhadamh luach ID adaimh mar 1 i gcónaí.

** In áirithe -** Slánuimhir 16-giotán nach mór a shocrú go 0.

**Comhaireamh leanaí -** Slánuimhir 16-giotán a léiríonn líon na n-adamh linbh in adamh.

**Áirithe -** Slánuimhir 32-giotán a chaithfear a shocrú go 0.

## Struchtúr Comhaid Chomhaid MOV

MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV sainithe ag fo-chineál a chaithfidh a bheith qt. Chun comhad MOV a chumadh, tá gá le smután atriallach go dtí go n-aimsítear cineál anaithnid.

Here is a `sample example`: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Ar fhritháireamh 32 (heics: 20) tá an dara smután, a bhfuil méid 8 aige agus cineál **mdat** (hex: 6D 64 61 74).

Tá an chéad smután eile suite ag fritháireamh 32+8#40 (hex: 28) agus tá méid 3,263,028 aige (hex: 00 31 CA 34) agus clóscríobh **mdat** (hex: 6D 64 61 74) ag fritháireamh 44 (hex :2C). Tá an chéad smután eile suite ag fritháireamh 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) agus tá méid 21,189 aige (hex: 00 00 52 C5) agus clóscríobh **moov** (hex: 6D 6F 6F offset 76). 1,836,019,574 (hex: 00 31 CA 60). Is é seo an smután deireanach, mar sin méid iomlán comhaid 3,263,068+21,189#3,284,257 beart.

## Conas Comhad MOV a Thiontú?

Tá neart na n-imreoirí meáin agus eagarthóirí físeán bogearraí ar fáil a thiontú comhaid MOV formáidí comhaid físe tóir eile. I measc cuid de na himreoirí meán is féidir comhaid MOV a thiontú go formáidí eile tá:

 * Seinnteoir meáin VLC VideoLAN
 * Seinnteoir ceoil Eltima Elmedia

Is féidir le roinnt imreoirí meán agus eagarthóirí físeáin, lena n-áirítear seinnteoir meáin VideoLAN VLC agus Eltima Elmedia Player, comhaid MOV a thiontú go formáidí eile. Is féidir leis na bogearraí seo comhaid MOV a thiontú go formáidí físeáin a leanas.

 * Físeán MPEG-4 - [MP4] (/físeán/mp4/)
 * Físeán WebM - [WEBM](/video/webm/)
 * Sruth Físiompair - [TS](/fístéip/ts/)
 * Formáid Ardchórais - [ASF](/video/ts/)
 * Fuaime Ogg Vorbis - [OGG](/audio/ogg/)
 * Fuaime MP3 - [MP3] (/audio/mp3/)
 * Codec Fuaime Gan Chailliúint Saor in Aisce - [FLAC](/audio/ flac/)
 * Fuaime WAVE - [WAV](/audio/wav/)

## Open Source API le haghaidh Comhaid MOV

 * [React Native API chun MOV a thiontú go MP4](https://github.com/taltultc/react-native-mov-to-mp4)
 * [Python API chun Comhaid MOV a dheisiú]( https://github.com/nrosenstein-stuff/movrepair)
 * [Ruby API chun MOV a thiontú go GIF]( https://github.com/skygroundmedia/convert-mov-to-gif)

## Tagairtí

* [ https://en.wikipedia.org/wiki/QuickTime_File_Format]( https://en.wikipedia.org/wiki/QuickTime_File_Format)


