{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid QT - Comhad Mearscannáin",
  "keywords": [
"QT",
"Físeán QuickTime",
"formáid qt",
"Conas a imirt comhaid qt",
"Comhad Scannán Tapa",
"QTFF",
"físeán",
"Úll"
],
  "description": "Foghlaim faoi fhormáid comhaid QT agus APIs ar féidir leo comhaid QT a chruthú agus a oscailt.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-gat"
}
},
  "lastmod": "2021-02-16"
}

## Cad is comhad QT ann?

Is comhad coimeádán ilmheán é comhad a bhfuil iarmhír .qt aige a úsáideann creat QuickTime chun ábhar comhaid ilmheán a stóráil. Arna fhorbairt ag Apple Inc. is comhad coimeádán ilmheán é an QuickTime File Format (QTFF) ina bhfuil fuaime, físeáin nó téacs le haghaidh athsheinm níos déanaí. Is í an fhormáid is rogha le haghaidh malartú meán digiteach idir feistí, feidhmchláir agus córais oibriúcháin. Déantar comhaid QT a shábháil freisin i bhformáid [MOV](/video/mov/) a d'fhorbair Apple Inc freisin. I measc cuid de na feidhmchláir is féidir comhaid QT a oscailt tá Apple QuickTime imreoir, seinnteoir meáin VLC, agus Media Player Classic le K-Lite Codec Pack.

## Formáid Chomhaid QT

Tá an QTFF dírithe ar oibiachtaí a nochtar bailiúchán solúbtha réad ar mhaithe le parsáil agus fairsingiú a éascú. Tá sruth meán atá ionchódaithe go digiteach nó tagairt sonraí don sruth meán atá suite i gcomhad eile i ngach rian i gcomhad QT. Feidhmíonn an struchtúr ordlathach sonraí atá comhdhéanta de réada ar a dtugtar adaimh mar choimeádáin rianta. Tá sonraíochtaí formáid comhaid do [QT file format](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) ar fáil go hoifigiúil ag Apple Inc mar thagairt don fhorbróir.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Adamh

Is é Atom bunaonad an chomhaid QuickTime. Tá dhá mhórréimse in aon adamh roimh aon réimse eile: Réimsí Méid agus Cineál. Léiríonn an réimse méide méid an adaimh agus léiríonn an réimse cineál an cineál sonraí atá stóráilte san adamh. De réir an dúlra, tá adaimh ordlathach, rud a chiallaíonn gur féidir adaimh amháin a bheith ann a bhféadfadh adaimh eile a bheith iontu fós. Taispeántar leagan amach adaimh samplach san íomhá seo a leanas.

Tá dhá chuid, ceanntásc, agus sonraí ag gach adamh. Tá na réimsí méid agus cineál sa cheanntásc agus tá na sonraí iarbhír sa chuid sonraí. Ina theannta sin, mínítear gach réimse thíos:

#### Méid an Adaimh

Léirítear ceanntásc agus inneachar an adaimh le slánuimhir 32-giotán ar a dtugtar méid an adaimh. Cuimsíonn an réimse méide méid an adaimh i mbearta, arna shloinneadh i slánuimhir 32-giotán gan síniú.

#### Cineál Adaimh

Taispeántar cineál an adaimh freisin le slánuimhir 32-giotán, a láimhseáiltear den chuid is mó mar réimse ceithre charachtar le luach knemonic, mar 'moov' (0x6D6F6F76) le haghaidh adamh scannáin, nó 'trak' (0x7472616B) le haghaidh adamh rian. Nuair a bhíonn an cineál adaimh ar eolas, ceadaíonn sé a chuid sonraí a léirmhíniú.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Struchtúr Comhaid ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV sainithe ag fo-chineál a chaithfidh a bheith qt. Chun comhad MOV a chumadh, tá gá le smután atriallach go dtí go n-aimsítear cineál anaithnid.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Ar fhritháireamh 32 (heics: 20) tá an dara smután, a bhfuil méid 8 aige agus cineál **mdat** (hex: 6D 64 61 74).

Tá an chéad smután eile suite ag fritháireamh 32+8#40 (hex: 28) agus tá méid 3,263,028 aige (hex: 00 31 CA 34) agus clóscríobh **mdat** (hex: 6D 64 61 74) ag fritháireamh 44 (hex :2C). Tá an chéad smután eile suite ag fritháireamh 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) agus tá méid 21,189 aige (hex: 00 00 52 C5) agus clóscríobh **moov** (hex: 6D 6F 6F offset 76). 1,836,019,574 (hex: 00 31 CA 60). Is é seo an smután deireanach, mar sin méid iomlán comhaid 3,263,068+21,189#3,284,257 beart.

## Tagairtí ##

* [Formáid Comhaid QT - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)

* [Formáid Comhaid QuickTime - Vicipéid]( https://ga.wikipedia.org/wiki/QuickTime_File_Format)


