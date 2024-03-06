{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "title": "MKV faila formāts",
  "keywords": [
"mkv",
"matroska video",
"mkv formātā",
"kā atskaņot mkv failus",
"video",
"failu",
"formātā"
],
  "description": "Uzziniet par MKV failu formātu un API, kas var izveidot un atvērt MKV failus.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-lvv"
}
},
  "lastmod": "2020-17-11"
}


## Kas ir MKV fails? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- Atbalsts ātrai meklēšanai.
- Iespēja izvēlēties dažādas audio un video straumes.
- Atbalsts subtitriem (cieti kodēti un mīksti kodēti).
- Atbalsts metadatiem, nodaļām un izvēlnēm.
- Iespēja straumēt tiešsaistē.
- Iespēja atgūt kļūdainus failus, kas nodrošina iespēju atskaņot bojātus failus.

## Īsa vēsture ##

MKV fails radās 2002. gadā Krievijā. Galvenais izstrādātājs bija Lasse Kärkkäinen, kurš strādāja ar Matroska dibinātāju Stīvu Lomme un programmētāju komandu. MKV tika izstrādāts kā atvērto standartu projekts, kas nozīmē, ka tas ir atvērtā koda un brīvi lietojams. Laikam ejot, formāts tika uzlabots un kļuva par WebM multivides formāta pamatu 2010. gadā.

## Matroska dizains ##

Matroska pievieno EBML specifikācijai šādus ierobežojumus.

- **EBML galvenes** **docType** ir jābūt matroska”.
- **EBML galvenes** **EBMLMaxIDLength** ir jābūt 4.
- **EBML galvenes** **EBMLMaxSizeLength** ir jābūt no 1 līdz 8 (ieskaitot).

Visi augstākā līmeņa elementi ir kodēti 4 oktetos.

- Valodu kodi: Matroska (1.–3. versija) izmantoja valodu kodus, kas var būt vai nu 3 burtu bibliogrāfiskā ISO-639-2 forma (piemēram, fre franču valodā), vai papildu valsts kods, piemēram, fre-ca.  Kanādas franču valodā. Sākot ar Matroska 4. versiju, valodu kodiem VAR izmantot ISO 639-2 vai BCP 47, lai gan ieteicams izmantot BCP 47.
- Fiziskie veidi: tiem ir atšķirīga nozīme gan audio, gan video failiem. Piemēram, ChapterPhysicalEquiv = 60 nozīmē (CD / 12 / 10 / 7 / TAPE / MINIDISC / DAT) audio un (DVD / VHS / LASERDISC) video.
- Bloka struktūra - Bloka galvene: Bloka galvenē ir informācija par celiņa numuru, laika zīmogiem, savienojuma veidu utt.
- Sašņorēšana: tas ir mehānisms, kas ļauj ietaupīt vietu, glabājot datus, ko parasti izmanto maziem datu blokiem (kadriem). Ir 3 šņoru veidi:
  - "Xiph: rāmis ar 255 lieluma reizinājumu, kas kodēts ar 0 izmēra beigās. Piemēram, kods 765 ir 255;255;255;0."
  - "EBML: kadra izmērs tiek kodēts kā atšķirība starp iepriekšējo izmēru un šo izmēru. Pirmais izmērs mežģīnē ir bez zīmēm, bet citi izmanto diapazona maiņu, lai iegūtu zīmi uz katras vērtības."
  - "fiksēts izmērs: izmērs paliek nemainīgs."
- Vienkāršā bloka struktūra: to iedvesmojusi **Bloku struktūra**, un galvenā atšķirība ir **Keyframe** un **Izmetams** karodziņu pievienošana. Izņemot to, viss ir vienāds.

## Matroska struktūra ##

Matroska dokumentam ir jāsastāv no vismaz viena **EBML dokumenta**, izmantojot **Matroska dokumenta veidu**. Katram **EBML dokumentam** jāsākas ar **EBML galveni**, kam seko **EBML saknes elements**, kas ir definēts kā segments. Matroska definē vairākus augstākā līmeņa elementus, kas var rasties **segmentā**.

EBML izmanto elementu sistēmu, lai izveidotu EBML dokumentu. Šis ir Matroska faila augstākā līmeņa elementu saraksts:

- **EBML dokuments**: visa faila iesaiņojums.
- **EBML galvene**: tajā ir tāda faila galvenes informācija kā DocType.
- **Segments**: augšējais elements, kas satur visus citus augstākā līmeņa elementus.
- **SeekHead**: tajā ir ietverta citu augstākā līmeņa elementu segmentu pozīcija.
- **Informācija**: tajā ir vispārīga informācija par segmentu.
- **Ieraksti**: augstākā līmeņa informācijas elements ar daudziem aprakstītiem ierakstiem.
- **Chapters**: It is used to define basic menus and partition data.
- **Klasteris**: augstākā līmeņa elements, kas satur bloka struktūru.
- **Cues**: augstākā līmeņa elements, kas satur visus segmentā lokālos ierakstus, kuriem ir nepieciešama piekļuve.
- **Pielikumi**: tajā ir pievienoti faili.
- **Tagi**: šis elements satur metadatus, kas apraksta ierakstus, izdevumus, nodaļas, pielikumus vai segmentu kopumā.

Šajā tabulā ir parādīta Matroska dokumenta struktūra ar lielāko daļu elementu, kas tiek parādīti hierarhijā:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML galvene | | | |
| Segments | SeekHead| Meklēt | SeekID |
| | | | SeekPosition |
| | Informācija | SegmentUID | |
| | | Segmenta faila nosaukums | |
| | | PrevUID | |
| | | Iepriekšējais faila nosaukums | |
| | | NextUID | |
| | | NākamaisFaila nosaukums | |
| | | SegmentFamily | |
| | | NodaļaTulkot | |
| | | TimestampScale | |
| | | Ilgums | |
| | | DatumsUTC | |
| | | Nosaukums | |
| | | MuxingApp | |
| | | WritingApp | |
| | Dziesmas | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Vārds |
| | | | Valoda |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | Alfa režīms |
| | | | | Pikseļu platums |
| | | | | PixelHeight |
| | | | | Displeja platums |
| | | | | Displeja augstums |
| | | | | AspectRatioType |
| | | | | Krāsa |
| | | | Audio | Paraugu ņemšanas frekvence |
| | | | | Kanāli |
| | | | | BitDepth |
| | Nodaļas | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | NodaļaAtom | NodaļaUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | NodaļaLaiksBeigas |
| | | | | NodaļaKarogsHidden |
| | | | | nodaļaDisplejs | ChapString |
| | | | | | ChapLanguage |
| | Klasteris | Laika zīmogs |
| | | SilentTracks |
| | | Pozīcija |
| | | Iepriekšējais izmērs |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Norādes | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Pielikumi | Pievienotais fails | Faila apraksts |
| | | | Faila nosaukums |
| | | | FileMimeType |
| | | | FileUID |
| | | | File Referral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Birkas | Atzīme | Mērķi | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### Kodeku izmantošana ###

Ja nevēlaties jaunu multivides atskaņotāju un vēlaties izmantot esošo atskaņotāju, jums būs jāinstalē daži kodeki (saīsinājuma/dekompresijas saīsinājums). Lai gan kodeku lejupielāde ir derīga iespēja, jums jābūt uzmanīgiem attiecībā uz avotu, jo tie var saturēt ļaunprātīgu programmatūru.

## Atsauces Nr.

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)

