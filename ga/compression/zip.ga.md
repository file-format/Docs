{
  "date": "2019-12-09",
  "keywords": [
"comhad zip",
"formáid comhaid zip",
"Cad is comhad a zip",
"comhad",
"sampla zip",
"síneadh comhad zip",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIP",
  "description": "Cad is comhad ZIP agus APIs ann ar féidir comhaid ZIP a chruthú agus a oscailt.",
  "linktitle": "ZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-gap"
}
},
  "lastmod": "2019-12-09"
}

## Cad is comhad ZIP ann? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the ZIP file size. ZIP file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKZIP](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made ZIP file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## Stair Achomair ar Formáid Chomhaid ZIP

Téann stair fhormáid comhaid ZIP siar go dtí an cás ina ndearna System Enhancement Associates (SEA) i gcoinne PKWARE as a áirgiúlacht ARC a úsáid gan ceadanna dá thrádmharc agus cóipchearta cuma agus comhéadan úsáideora an táirge. Roimhe seo, bhí Phil Katz tar éis cód foinse SEA a athscríobh agus scaoileadh PKXARC, eastóscóir ARC, agus PKARC, comhbhrúiteoir comhaid, mar earraí saor in aisce do chórais MS-DOS. Ag dul amú ar an dlí, ní raibh PKWARE in ann aon rud a bhaineann le ARC a úsáid a thuilleadh. Seo é an áit ar tháinig cruthú comhbhrú comhad nua ar an saol, ainmnithe mar ZIP a rinneadh mar chuid d’fhóntas PKZIP ag PKWARE, Inc.

D'eisigh Katz na sonraíochtaí formáid comhaid ZIP isteach go poiblí, agus ag an am céanna coinníodh na cearta dílseánaigh ar a fóntais chomhbhrú agus asbhainte ie PKZIP. Bhí (agus tá) an córas comhbhrú ZIP in ann comhaid a chartlannú i bhfillteán trí algartam seiceála iomarcaíochta timthriallach 32-giotán ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) chun méideanna comhaid a chomhbhrú. Murab ionann agus ARC, chuimsigh fillteáin .ZIP comhad eolaire a raibh ról leabhar cód cripteagrafóra ann, agus an fhaisnéis riachtanach chun na comhaid chomhbhrúite a sholáthar.

## Modhanna Comhbhrúite Tacaithe i ZIP

De réir sonraíochtaí Formáid Chomhaid .ZIP, tacaítear leis na modhanna comhbhrú seo a leanas.

* Store - le tuiscint aon comhbhrú

* Laghdaigh

* Laghdú (Tugann sé seo fachtóirí comhbhrú ó leibhéal 1 go leibhéal 4)

* Implode

* Deflate

* Díbhoilsciú64

* BZIP2

* LZMA (EFS)

* WavPack

* Leagan PPMd I, Ath 1


DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Sonraíochtaí Formáid Comhaid ZIP

Tá an cumas ag comhaid ZIP comhaid iolracha a stóráil ag baint úsáide as teicnící comhbhrú éagsúla agus ag an am céanna tacaíonn siad le comhad a stóráil gan aon chomhbhrú. Stóráiltear/comhbhrúitear gach comhad ina n-aonar, rud a chabhraíonn lena n-eastóscadh, nó le cinn nua a chur leis, gan comhbhrú nó dí-chomhbhrú a chur i bhfeidhm ar an gcartlann iomlán.

### Formáid Chomhaid ZIP Fhoriomlán

Tá gach comhad Zip struchtúrtha ar an mbealach seo a leanas:


| Formáid comhaid ZIP
---|
| Ceanntásc an Chomhaid Áitiúil 1
|Sonraí Comhad 1
| Tuairisceoir Sonraí 1
| Ceanntásc an Chomhaid Áitiúil 2
|Sonraí Comhad 2
| Tuairisceoir Sonraí 2
| ....
| ....
| Ceanntásc an Chomhaid Áitiúil N
|Sonraí Comhad N
|Tuairisceoir Sonraí N
| Ceanntásc Díchriptithe Cartlainne
|Cartlann Taifead Sonraí Breise
| Eolaire Lárnach

Úsáideann formáid comhaid ZIP algartam CRC 32-giotán chun críche cartlannaithe. Chun na comhaid chomhbhrúite a sholáthar, coimeádann cartlann ZIP eolaire ag an deireadh a choinníonn iontráil na gcomhad atá ann agus a suíomh sa chomhad cartlainne. Mar sin, imríonn sé ról an ionchódaithe chun faisnéis a chuimsiú is gá chun na comhaid chomhbhrúite a sholáthar. Úsáideann léitheoirí ZIP an t-eolaire chun liosta na gcomhad a luchtú gan cartlann ZIP iomlán a léamh. Coinníonn an fhormáid seo déchóipeanna den struchtúr eolaire chun cosaint níos fearr a sholáthar ar chailliúint sonraí.

Léirítear gach comhad i gcartlann ZIP mar iontráil aonair ina bhfuil Ceanntásc Comhad Áitiúil i ngach iontráil agus ina dhiaidh sin an data comhaid chomhbhrúite. Tá na tagairtí do na hiontrálacha comhaid seo go léir ag an Eolaire ag deireadh na cartlainne. Ba cheart go seachnódh léitheoirí comhaid ZIP na ceanntásca comhaid áitiúla a léamh agus ba cheart gach sórt liostú comhad a léamh ón Eolaire. Is é an tEolaire seo an t-aon fhoinse le haghaidh iontrálacha comhaid bailí sa chartlann mar is féidir comhaid a chur i gceangal i dtreo dheireadh na cartlainne freisin. Sin é an fáth má léann léitheoir ceanntásca áitiúla de chartlann ZIP ón tús, d'fhéadfadh sé iontrálacha neamhbhailí (scriosta) a léamh chomh maith nach bhfuil mar chuid den Eolaire atá á scriosadh as an gcartlann.

Ní gá go mbeadh ord na n-iontrálacha comhaid sa eolaire lárnach ag teacht le hord na n-iontrálacha comhaid sa chartlann.

### Iontrálacha Comhad ZIP

Socraítear iontrálacha i gcomhad ZIP ceann i ndiaidh a chéile ina bhfuil gach iontráil comhdhéanta de:

* Ceanntásc Comhad Áitiúil

* Réimsí Sonraí Breise Roghnacha

* Sonraí úsáideora (comhbhrúite go roghnach / criptithe go roghnach)


Léiríonn Ceanntásc an Chomhaid Áitiúil gach iontráil faisnéis faoin gcomhad amhail nóta tráchta, méid comhaid agus ainm comhaid. Is féidir leis na réimsí sonraí breise (roghnach) faisnéis a sholáthar le haghaidh roghanna insínteachta na formáide ZIP.

#### Ceanntásc Comhaid Logánta

Tá struchtúr sainiúil páirce ag an gCeanntásc Comhad Áitiúil atá comhdhéanta de luachanna ilbhearta. Stóráiltear na luachanna go léir in ord beart beag-endian ina n-áirítear fad na páirce an fad i mbearta. Úsáideann na struchtúir go léir i gcomhad ZIP sínithe 4-bheart le haghaidh gach iontráil comhaid. Is é 0x06054b50 deireadh síniú an eolaire láir agus is féidir é a idirdhealú trí úsáid a bhaint as a shíniú uathúil féin. Seo a leanas ord na faisnéise atá stóráilte sa Cheanntásc Comhad Áitiúil.


|Fritháireamh | Beart | Cur síos
---|---|---|
|0|4|Síniú ceanntásc an chomhaid áitiúil # 0x04034b50 (léite mar uimhir cheannteidil bheag)
|4|2|Leagan ag teastáil chun eastóscadh (íosmhéid)
|6|2|Bratach giotán cuspóra ghinearálta
|8|2|Modh comhbhrúite
|10|2|Comhad an t-am modhnaithe is déanaí
|12|2|Comhad dáta an mhodhnaithe deiridh
|14|4|CRC-32
|18|4|Méid comhbhrúite
|22|4|Méid neamh-chomhbhrúite
|26|2|Fad ainm comhaid (n)
|28|2|Fad páirce breise (m)
|30|n|Ainm an Chomhaid
|30+n|m|Réimse Breise

#### Ceanntásc Comhad Eolaire Lárnach


|Fritháireamh | Beart | Cur síos
---|---|---|
|0|4|Síniú ceanntásc an chomhaid láir # 0x02014b50
|4|2|Leagan déanta ag
|6|2|Leagan ag teastáil chun eastóscadh (íosmhéid)
|8|2|Bratach giotán cuspóra ghinearálta
|10|2|Modh comhbhrúite
|12|2|Comhad an t-am modhnaithe is déanaí
|14|2|Comhad dáta an mhodhnaithe deiridh
|16|4|CRC-32
|20|4|Méid comhbhrúite
|24|4|Méid neamh-chomhbhrúite
|28|2|Fad ainm comhaid (n)
|30|2|Fad páirce breise (m)
|32|2|Fad nóta tráchta comhaid (k)
|34|2|Uimhir diosca nuair a thosaíonn an comhad
|36|2|Tréithe an chomhaid inmheánaigh
|38|4|Tréithe comhaid sheachtraigh
|42|4|Fritháireamh coibhneasta ceanntásc an chomhaid logánta. Is é seo líon na mbeart idir tús an chéad diosca ar a dtarlaíonn an comhad, agus tús ceanntásc an chomhaid áitiúil. Ligeann sé seo do bhogearraí a léann an eolaire lárnach suíomh an chomhaid a aimsiú laistigh den chomhad ZIP.
|46|n|Ainm an chomhaid
|46+n|m|Réimse breise
|46+n+m|k|Nóta tráchta sa chomhad

#### Deireadh le Taifead an Eolaire Lárnach


|Fritháireamh | Beart | Cur síos
---|---|---|
|0|4|Síniú deireadh an eolaire láir # 0x06054b50
|4|2|Uimhir an diosca seo
|6|2|Diosca a gcuirtear tús leis an eolaire lárnach
|8|2|Líon na dtaifead eolaire lárnach ar an diosca seo
|10|2|Líon iomlán na dtaifead eolaire lárnach
|12|4|Méid an eolaire láir (bearta)
|16|4|Fritháireamh thús na eolaire láir, i gcoibhneas le tús na cartlainne
|20|2|fad nóta tráchta (n)
|22|n|Nóta tráchta

## Tagairtí

* [PKWARE ZIP File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struchtúr an Chomhaid PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)


