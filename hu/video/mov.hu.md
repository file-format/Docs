{
  "date" : "2019-10-11",
  "keywords" :[ "mov fájl", "mov fájl formátum", "mi az a mov fájl", "fájl", "mov példa", "mov fájl kiterjesztése", "kiterjesztés", "formátum", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV fájl – Apple QuickTime Movie File Format",
  "description":"További információ a MOV fájlformátumról és az API-król, amelyek MOV fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Mi az a MOV fájl?

A MOV-fájl az Apple Inc. által kifejlesztett videofájl, amely egy vagy több műsorszámot tartalmaz. Minden szám egy filmet, hangot, filmklipeket és feliratokat tárol. Ez egy multimédiás tároló, amely különböző típusú médiaelemeket képes tárolni. A MOV videó formátum Windows és Macintosh rendszerekkel is kompatibilis. A tömörítéshez MPEG-4 kódolást használ, és a sávokat az atomoknak nevezett objektumok tartják fenn, amelyek egy hierarchikus adatszerkezetben vannak elhelyezve.

## A MOV fájlformátum rövid története

Az MPEG-4 fájlformátum a QuickTime File Format (**QTFF**) specifikációból fejlődött ki 2001-ben. A Nemzetközi Szabványügyi Szervezet jóváhagyta a formátumot, és az MPEG-4 Part 1 rendszerspecifikációit 1999-ben tették közzé. 2001-ben egy revíziós fájl formátum [MP4](/hu/video/mp4/) megjelent.

Az MP4 első verzióját 2003-ban módosították MPEG-4 Part 14 néven (ISO/IEC 14496-14:2003). 2004-ben az MP4-et általánosították, hogy meghatározza az összes időalapú médiafájl általános szerkezetét. Ezért ma már számos egyéb multimédiás fájlformátum alapjaként szolgál.

## QuickTime fájlformátum (QTFF) – További információ

A digitális multimédiával való együttműködés érdekében a QTFF sokféle adatot képes tárolni. Ez egy ötletformátum a digitális média cseréjéhez, mivel a formátum meghatározza a szabványokat bármilyen típusú médiastruktúra leírására. A fájlformátum objektum-orientált objektumok rugalmas gyűjteményéből áll. A filmek lemezen való tárolására a QuickTime két struktúrát használ, azaz "atomokat" és "QT atomokat".

### Atomok

Az Atom a QuickTime fájl alapegysége. Minden atomban két fő mező található minden más mező előtt: Méret és Típus mező. A méret mező az atom méretét mutatja, míg a típus mező az atomban tárolt adatok típusát. Az atomok természetüknél fogva hierarchikusak, ami azt jelenti, hogy egy atom tartalmazhat más atomokat, amelyek továbbra is tartalmazhatnak másokat. A mintaatom elrendezése a következő képen látható.

Minden atomnak két része van, "fejléc" és "adat". A fejléc a méret és típus mezőket tartalmazza, az adatrész pedig a tényleges adatokat. Továbbá az alábbiakban az egyes mezőket ismertetjük:

### Atomméret

Az atom fejlécét és tartalmát egy 32 bites egész szám jelzi, amelyet az atom méretének nevezünk. A méret mező tartalmazza az atom méretét bájtban, 32 bites előjel nélküli egész számban kifejezve.

### Atom típusa

Az atom típusát egy 32 bites egész szám is mutatja, amelyet többnyire négykarakteres mezőként kezelnek knemonikus értékkel, például „moov” (0x6D6F6F76) filmatom esetén, vagy „trak” (0x7472616B) egy nyomatom. Ha az atom típusa ismert, lehetővé teszi az adatok értelmezését.

### QT atomok és atomtartályok

A QT atomok általános célú tárolási formátumot biztosítanak, és kiterjesztett fejlécük van, amely a Méret, Típus, Atomazonosító és Gyermek atomok száma mezőkből áll. A QT atomok egy atomtárolóba vannak csomagolva, amely egy egyedi adatstruktúra, amelynek fejléce zárszámmal rendelkezik. Minden atomtartályban van egy gyökératom, ez a QT atom. A QT atom elrendezése az alábbi ábrán látható.

A QT atom konténer fejléce a következő adatokat tartalmazza:

Fenntartva: 10 bájtos elem 0 értékkel.

Zárolási szám: 16 bites egész szám 0 értékkel.

A QT atomfejlécek a következő adatokat tartalmazzák:

**Méret -** A QT atom fejlécet és tartalmát bájtokban 32 bites egész szám jelzi. Levélatom esetén ez a mező egyetlen atom méretét tartalmazza.

**Típus -** Az atom típusát egy 32 bites egész szám jelzi. Abban az esetben, ha ez a gyökératom, akkor az érték „sean” lesz.

**Atom ID -** Ez egy 32 bites egész szám, amely az atomazonosítót mutatja, és minden testvér számára egyedinek kell lennie. A gyökératom az atomazonosító értéke mindig 1.

**Fenntartva -** 16 bites egész szám, amelyet 0-ra kell állítani.

**Child count -** 16 bites egész szám, amely az atom gyermekatomjainak számát jelzi.

**Fenntartva -** 32 bites egész szám, amelyet 0-ra kell állítani.

## A MOV fájlok fájlszerkezete

A MOV fájlok egymást követő darabokból állnak. Minden csonknak van egy 8 bájtos fejléce: 4 bájtos csonkméret (big-endian, magas bájt először) és 4 bájtos csonktípus - az előre meghatározott aláírások egyike: "ftyp", "mdat", "moov", "pnot" ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Az első darab "ftype" típusú, és van egy altípusa a 8-as eltolásnál. A MOV-t altípus határozza meg, amelynek "qt"-nek kell lennie. A MOV-fájl összeállításához ismételni kell a darabokat, amíg ismeretlen típust észlel.

Íme egy "minta példa": Egy minta MOV-fájl bináris adatainak vizsgálatakor nyilvánvaló, hogy az **ftyp** (hex: 66 74 79 70) aláírással kezdődik a 4. eltolásnál, amely meghatározza a QuickTime tárolófájl típusát. A fájl altípusa **qt~_~_** (hex: 71 74 20 20), amely a MOV fájltípusra mutat. Az első blokk mérete 32 (hexa: 00 00 00 20, big-endian, magas bájt először), a mérete 0 eltolásnál található. írja be az **mdat** (hex: 6D 64 61 74).

A következő darab a 32+8#40 eltolásnál (hex: 28) található, mérete 3 263 028 (hex: 00 31 CA 34), típusa pedig **mdat** (hex: 6D 64 61 74) a 44-es eltolásnál (hex) : 2C). A következő darab a 40 + 3 263 028#3 263 068 eltolásnál található (hex: 00 31 CA 5C), mérete 21 189 (hex: 00 00 52 C5), és típusa **moov** (hex: 6D 6F) at 6F 1 836 019 574 (hex: 00 31 CA 60). Ez az utolsó darab, tehát a teljes fájlméret 3 263 068+21 189#3 284 257 bájt.

## Hogyan lehet MOV fájlt konvertálni?

Rengeteg médialejátszó és szoftveres videószerkesztő áll rendelkezésre a MOV-fájlok más népszerű videofájl-formátumokba konvertálására. A MOV-fájlokat más formátumba konvertáló médialejátszók közül néhány:

* VideoLAN VLC médialejátszó
* Eltima Elmedia Player

Számos médialejátszó és videószerkesztő, köztük a VideoLAN VLC médialejátszó és az Eltima Elmedia Player, képes a MOV fájlokat más formátumokká konvertálni. Ezek a szoftverek MOV fájlokat konvertálhatnak a következő videó formátumokba.

* MPEG-4 videó – [MP4](/hu/video/mp4/)
* WebM Video - [WEBM](/hu/video/webm/)
* Video Transport Stream – [TS](/hu/video/ts/)
* Fejlett rendszerek formátuma – [ASF](/hu/video/ts/)
* Ogg Vorbis Audio – [OGG](/hu/audio/ogg/)
* MP3 audio - [MP3](/hu/audio/mp3/)
* Ingyenes veszteségmentes audiokodek – [FLAC](/hu/audio/flac/)
* WAVE Audio - [WAV](/hu/audio/wav/)

## Nyílt forráskódú API MOV-fájlokhoz

* [React Native API a MOV MP4-re konvertálásához](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API a MOV-fájlok javításához](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API a MOV GIF formátumba konvertálásához](https://github.com/skygroundmedia/convert-mov-to-gif)

## Hivatkozások

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

