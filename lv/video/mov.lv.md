{
  "date": "2019-10-11",
  "keywords": [
"mov failu",
"mov faila formātā",
"kas ir mov fails",
"failu",
"mov piemērs",
"mov faila paplašinājums",
"pagarinājumu",
"formātā",
"Ātrs laiks",
"MPEG-4"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MOV fails — Apple QuickTime filmas faila formāts",
  "description": "Uzziniet par MOV failu formātu un API, kas var izveidot un atvērt MOV failus.",
  "linktitle": "MOV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mo-lvv"
}
},
  "lastmod": "2021-07-29"
}

## Kas ir MOV fails?

MOV fails ir Apple Inc. izstrādāts video faila veids, kas satur vienu vai vairākus ierakstus. Katrā ierakstā tiek saglabāta filma, audio, filmu klipi un subtitri. Tas ir multivides konteiners, kurā var uzglabāt dažāda veida multivides elementus. MOV video formāts ir saderīgs gan ar Windows, gan ar Macintosh sistēmām. Tas izmanto saspiešanai kodētu MPEG-4, un celiņi tiek uzturēti objektos, ko sauc par atomiem un kas ir ievietoti hierarhiskā datu struktūrā.

## Īsa MOV faila formāta vēsture

MPEG-4 file format has evolved from QuickTime File Format (**QTFF**) specification in 2001. Starptautiskā standartizācijas organizācija apstiprināja formātu, un MPEG-4 1. daļas sistēmu specifikācijas tika publicētas 1999. gadā. 2001. gadā tika publicēts pārskatīšanas faila formāts [MP4](/video/mp4/).

MP4 pirmā versija tika pārskatīta 2003. gadā kā MPEG-4 14. daļa (ISO/IEC 14496-14:2003). 2004. gadā MP4 tika vispārināts, lai noteiktu vispārēju struktūru visiem laika multivides failiem. Tāpēc tagad tas tiek izmantots kā pamats dažādiem citiem multivides failu formātiem.

## QuickTime faila formāts (QTFF) — plašāka informācija

Lai strādātu ar digitālo multividi, QTFF var glabāt dažāda veida datus. Tas ir ideju formāts digitālo mediju apmaiņai, jo formāts nosaka standartus jebkura veida mediju struktūru aprakstīšanai. Faila formāts sastāv no elastīgas objektu orientētu objektu kolekcijas. Filmu glabāšanai diskos QuickTime izmanto divas struktūras, ti, atomi un QT atomi.

### Atomi

Atom ir QuickTime faila pamatvienība. Jebkurā atomā pirms jebkura cita lauka ir divi galvenie lauki: lauki Izmērs un Tips. Lieluma lauks parāda atoma izmēru, bet tipa lauks norāda atomā saglabāto datu veidu. Pēc būtības atomi ir hierarhiski, kas nozīmē, ka viens atoms var saturēt citus atomus, kuri joprojām var saturēt citus. Parauga atoma izkārtojums ir parādīts nākamajā attēlā.

Katram atomam ir divas daļas: galvene un dati. Galvenē ir izmēra un veida lauki, un datu daļā ir faktiskie dati. Turklāt katrs lauks ir izskaidrots tālāk:

### Atoma izmērs

Atoma galveni un saturu norāda ar 32 bitu veselu skaitli, kas pazīstams kā atoma lielums. Lieluma laukā ir ietverts atoma lielums baitos, kas izteikts ar 32 bitu neparakstītu veselu skaitli.

### Atoma tips

Atoma veidu parāda arī 32 bitu vesels skaitlis, kas lielākoties tiek uzskatīts par četru rakstzīmju lauku ar knemonisku vērtību, piemēram, moov” (0x6D6F6F76) filmas atomam vai trak” (0x7472616B) trases atoms. Kad atoma tips ir zināms, tas ļauj interpretēt tā datus.

### QT atomi un atomu konteineri

QT atomi nodrošina vispārējas nozīmes uzglabāšanas formātu, un tiem ir paplašināta galvene, kas sastāv no laukiem Size, Type, Atom ID un Count of Child atoms. QT atomi ir iesaiņoti atomu konteinerā, unikālā datu struktūrā, kam ir galvene ar bloķēšanas skaitu. Katrā atoma konteinerā ir viens saknes atoms, kas ir QT atoms. QT atoma izkārtojums ir parādīts attēlā zemāk.

QT atom konteinera galvenē ir šādi dati:

Rezervēts: 10 baitu elements ar vērtību 0.

Bloķēšanas skaits: 16 bitu vesels skaitlis ar vērtību 0.

QT atomu galvenēm ir šādi dati:

**Izmērs -** QT atoma galvene un saturs ir norādīts baitos ar 32 bitu veselu skaitli. Lapas atoma gadījumā šis lauks satur viena atoma izmēru.

**Tips -** Atoma tips ir norādīts ar 32 bitu veselu skaitli. Ja tas ir saknes atoms, vērtība tiek iestatīta uz sean.

**Atom ID —** tas ir 32 bitu vesels skaitlis, kas parāda atoma ID, un tam ir jābūt unikālam visiem brāļiem un māsām. Saknes atomam vienmēr atoma ID vērtība ir 1.

**Rezervēts —** 16 bitu vesels skaitlis, kas jāiestata uz 0.

**Bērnu skaits —** 16 bitu vesels skaitlis, kas norāda atoma bērnu atomu skaitu.

**Rezervēts —** 32 bitu vesels skaitlis, kas jāiestata uz 0.

## MOV failu failu struktūra

MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV definēts ar apakštipu, kam jābūt qt. Lai izveidotu MOV failu, ir nepieciešams atkārtot gabalus, līdz tiek atklāts nezināms veids.

Here is a `sample example`: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Nobīdē 32 (hex: 20) atrodas otrais gabals, kura izmērs ir 8 un ierakstiet **mdat** (hex: 6D 64 61 74).

Nākamais fragments atrodas nobīdē 32+8#40 (hex: 28), un tā izmērs ir 3 263 028 (hex: 00 31 CA 34), un 44. nobīdē (hex. veids ir **mdat** (hex: 6D 64 61 74) : 2C). Nākamā daļa atrodas nobīdē 40 + 3 263 028 # 3 263 068 (hex: 00 31 CA 5C), un tās izmērs ir 21 189 (hex: 00 00 52 C5) un ierakstiet **moov** (hex: 6D 6F) pie 6F. 1 836 019 574 (hex: 00 31 CA 60). Šis ir pēdējais fragments, tāpēc kopējais faila lielums ir 3 263 068 + 21 189 # 3 284 257 baiti.

## Kā konvertēt MOV failu?

Ir pieejami daudzi multivides atskaņotāji un programmatūras video redaktori, lai pārveidotu MOV failus citos populāros video failu formātos. Daži no multivides atskaņotājiem, kas var pārvērst MOV failus citos formātos, ir šādi:

 * VideoLAN VLC multivides atskaņotājs
 * Eltima Elmedia Player

Vairāki multivides atskaņotāji un video redaktori, tostarp VideoLAN VLC multivides atskaņotājs un Eltima Elmedia Player, var pārvērst MOV failus citos formātos. Šī programmatūra var pārvērst MOV failus šādos video formātos.

 * MPEG-4 video — [MP4](/video/mp4/)
 * WebM video — [WEBM](/video/webm/)
 * Video transporta straume — [TS](/video/ts/)
 * Uzlaboto sistēmu formāts — [ASF](/video/ts/)
 * Ogg Vorbis Audio — [OGG](/audio/ogg/)
 * MP3 audio — [MP3](/audio/mp3/)
 * Bezmaksas audio kodeks bez zudumiem — [FLAC](/audio/flac/)
 * WAVE Audio — [WAV](/audio/wav/)

## Atvērtā pirmkoda API MOV failiem

 * [React Native API, lai pārveidotu MOV par MP4](https://github.com/taltultc/react-native-mov-to-mp4)
 * [Python API MOV failu labošanai](https://github.com/nrosenstein-stuff/movrepair)
 * [Ruby API, lai pārveidotu MOV par GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Atsauces

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)


