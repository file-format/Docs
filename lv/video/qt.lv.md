{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QT faila formāts — ātrais filmas fails",
  "keywords": [
"QT",
"QuickTime video",
"qt formātā",
"kā atskaņot qt failus",
"Ātrās filmas fails",
"QTFF",
"video",
"Apple"
],
  "description": "Uzziniet par QT faila formātu un API, kas var izveidot un atvērt QT failus.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-lvt"
}
},
  "lastmod": "2021-02-16"
}

## Kas ir QT fails?

Fails ar paplašinājumu .qt ir multivides konteinera fails, ko QuickTime ietvars izmanto multivides faila satura glabāšanai. Apple Inc. izstrādātais QuickTime faila formāts (QTFF) ir multivides konteinera fails, kas satur audio, video vai tekstu, lai to varētu atskaņot vēlāk. Tas ir izvēlētais formāts digitālo datu nesēju apmaiņai starp ierīcēm, lietojumprogrammām un operētājsistēmām. QT faili tiek saglabāti arī [MOV](/video/mov/) formātā, ko arī izstrādāja Apple Inc. Dažas lietojumprogrammas, ar kurām var atvērt QT failus, ir Apple QuickTime Player, VLC multivides atskaņotājs un Media Player Classic ar K-Lite Codec Pack.

## QT faila formāts

QTFF ir objektorientēts, kas nodrošina elastīgu objektu kolekciju, lai atvieglotu parsēšanu un paplašināšanu. Katrs celiņš QT failā satur digitāli kodētu multivides straumi vai datu atsauci uz multivides straumi, kas atrodas citā failā. Hierarhiskā datu struktūra, kas sastāv no objektiem, ko sauc par atomiem, darbojas kā trases konteineri. Apple Inc ir oficiāli pieejamas [QT file format](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) faila formāta specifikācijas izstrādātāja uzziņai.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Atomi

Atom ir QuickTime faila pamatvienība. Jebkurā atomā pirms jebkura cita lauka ir divi galvenie lauki: lauki Izmērs un Tips. Lieluma lauks parāda atoma izmēru, bet tipa lauks norāda atomā saglabāto datu veidu. Pēc būtības atomi ir hierarhiski, kas nozīmē, ka viens atoms var saturēt citus atomus, kuri joprojām var saturēt citus. Parauga atoma izkārtojums ir parādīts nākamajā attēlā.

Katram atomam ir divas daļas, galvene un dati. Galvenē ir izmēra un veida lauki, un datu daļā ir faktiskie dati. Turklāt katrs lauks ir izskaidrots tālāk:

#### Atoma izmērs

Atoma galveni un saturu norāda ar 32 bitu veselu skaitli, kas pazīstams kā atoma lielums. Lieluma laukā ir ietverts atoma lielums baitos, kas izteikts ar 32 bitu neparakstītu veselu skaitli.

#### Atoma tips

Atoma veidu parāda arī 32 bitu vesels skaitlis, kas lielākoties tiek uzskatīts par četru rakstzīmju lauku ar knemonisku vērtību, piemēram, moov” (0x6D6F6F76) filmas atomam vai trak” (0x7472616B) trases atoms. Kad atoma tips ir zināms, tas ļauj interpretēt tā datus.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Faila struktūra ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV definēts ar apakštipu, kam jābūt qt. Lai izveidotu MOV failu, ir nepieciešams atkārtot gabalus, līdz tiek atklāts nezināms veids.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Nobīdē 32 (hex: 20) atrodas otrais gabals, kura izmērs ir 8 un ierakstiet **mdat** (hex: 6D 64 61 74).

Nākamais fragments atrodas nobīdē 32+8#40 (hex: 28), un tā izmērs ir 3 263 028 (hex: 00 31 CA 34), un 44. nobīdē (hex. veids ir **mdat** (hex: 6D 64 61 74) : 2C). Nākamā daļa atrodas nobīdē 40 + 3 263 028 # 3 263 068 (hex: 00 31 CA 5C), un tās izmērs ir 21 189 (hex: 00 00 52 C5) un ierakstiet **moov** (hex: 6D 6F) pie 6F. 1 836 019 574 (hex: 00 31 CA 60). Šis ir pēdējais fragments, tāpēc kopējais faila lielums ir 3 263 068 + 21 189 # 3 284 257 baiti.

## Atsauces Nr.

* [QT faila formāts — Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)

* [QuickTime faila formāts — Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


