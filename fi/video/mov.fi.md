{
  "date": "2019-10-11",
  "keywords": [
"mov tiedosto",
"mov-tiedostomuoto",
"mikä on mov-tiedosto",
"tiedosto",
"mov esimerkki",
"mov tiedostopääte",
"laajennus",
"muoto",
"QuickTime",
"MPEG-4"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MOV-tiedosto - Apple QuickTime Movie -tiedostomuoto",
  "description": "Opi MOV-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata MOV-tiedostoja.",
  "linktitle": "MOV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mo-fiv"
}
},
  "lastmod": "2021-07-29"
}

## Mikä on MOV-tiedosto?

MOV-tiedosto on Apple Inc:n kehittämä videotiedostotyyppi, joka sisältää yhden tai useamman raidan. Jokainen raita tallentaa elokuvan, äänen, elokuvaleikkeet ja tekstitykset. Se on multimediasäiliö, johon voidaan tallentaa erilaisia mediaelementtejä. MOV-videomuoto on yhteensopiva sekä Windows- että Macintosh-järjestelmien kanssa. Se käyttää pakkaamiseen koodattua MPEG-4:ää ja raitoja ylläpidetään objekteissa, joita kutsutaan atomeiksi ja jotka on sijoitettu hierarkkiseen tietorakenteeseen.

## MOV-tiedostomuodon lyhyt historia

MPEG-4 file format has evolved from QuickTime File Format (**QTFF**) specification in 2001. Kansainvälinen standardointijärjestö hyväksyi muodon ja MPEG-4 Part 1 -järjestelmäspesifikaatiot julkaistiin vuonna 1999. Vuonna 2001 julkaistiin versiotiedostomuoto [MP4](/video/mp4/).

MP4:n ensimmäinen versio tarkistettiin vuonna 2003 nimellä MPEG-4 Part 14 (ISO/IEC 14496-14:2003). Vuonna 2004 MP4 yleistettiin määrittelemään yleinen rakenne kaikille aikaperusteisille mediatiedostoille. Siksi sitä käytetään nyt useiden muiden multimediatiedostomuotojen perustana.

## QuickTime-tiedostomuoto (QTFF) - Lisätietoja

Digitaalisen multimedian kanssa työskentelyyn QTFF voi sisältää monenlaista dataa. Se on ideamuoto digitaalisen median vaihtoon, koska muoto määrittelee standardit kaikenlaisten mediarakenteiden kuvaamiselle. Tiedostomuoto koostuu joustavasta olio-objektien kokoelmasta. Elokuvien tallentamiseen levyille QuickTime käyttää kahta rakennetta eli atomeja ja QT-atomeja.

### Atomit

Atom on QuickTime-tiedoston perusyksikkö. Jokaisessa atomissa on kaksi pääkenttää ennen muita kenttiä: Koko- ja Tyyppikentät. Kokokenttä näyttää atomin koon, kun taas tyyppikenttä osoittaa atomiin tallennettujen tietojen tyypin. Atomit ovat luonteeltaan hierarkkisia, mikä tarkoittaa, että yksi atomi voi sisältää muita atomeja, jotka voivat silti sisältää muita. Esimerkkiatomin asettelu näkyy seuraavassa kuvassa.

Jokaisella atomilla on kaksi osaa, otsikko ja tiedot. Otsikko sisältää koko- ja tyyppikentät ja tieto-osa sisältää varsinaiset tiedot. Lisäksi jokainen kenttä on selitetty alla:

### Atomin koko

Atomin otsikko ja sisältö ilmaistaan 32-bittisellä kokonaisluvulla, joka tunnetaan atomin kokona. Kokokenttä sisältää atomin koon tavuina ilmaistuna 32-bittisenä etumerkittömänä kokonaislukuna.

### Atomityyppi

Atomin tyyppi näkyy myös 32-bittisellä kokonaisluvulla, jota käsitellään enimmäkseen neljän merkin kenttänä, jolla on knemonic-arvo, kuten moov (0x6D6F6F76) elokuvaatomille tai trak (0x7472616B) raideatomi. Kun atomityyppi on tiedossa, se mahdollistaa sen tietojen tulkitsemisen.

### QT-atomit ja atomisäiliöt

QT-atomit tarjoavat yleiskäyttöisen tallennusmuodon ja niillä on laajennettu otsikko, joka koostuu koko-, tyyppi-, atomin tunnus- ja lapsiatomien määrä -kentistä. QT-atomit on kääritty atomisäiliöön, joka on ainutlaatuinen tietorakenne, jossa on otsikko, jossa on lukitusmäärä. Jokaisessa atomisäiliössä on yksi juuriatomi, joka on QT-atomi. QT-atomin asettelu on esitetty alla olevassa kuvassa.

QT-atomisäiliön otsikossa on seuraavat tiedot:

Varattu: 10-tavuinen elementti, jonka arvo on 0.

Lukitusmäärä: 16-bittinen kokonaisluku, jonka arvo on 0.

QT-atomiotsikoissa on seuraavat tiedot:

**Koko -** QT-atomin otsikko ja sisältö ilmaistaan tavuina 32-bittisellä kokonaisluvulla. Lehtiatomin tapauksessa tämä kenttä sisältää yhden atomin koon.

**Tyyppi -** Atomin tyyppi ilmaistaan 32-bittisellä kokonaisluvulla. Jos se on juuriatomi, arvoksi asetetaan sean.

**Atom ID -** Se on 32-bittinen kokonaisluku, joka näyttää atomin tunnuksen ja jonka on oltava yksilöllinen kaikille sisaruksille. Juuriatomin tunnuksen arvo on aina 1.

**Varattu -** 16-bittinen kokonaisluku, joka on asetettava arvoon 0.

**Lapsiluku -** 16-bittinen kokonaisluku, joka ilmaisee atomin lapsiatomien lukumäärän.

**Varattu -** 32-bittinen kokonaisluku, joka on asetettava arvoon 0.

## MOV-tiedostojen tiedostorakenne

MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV määritellään alatyypillä, jonka on oltava qt. MOV-tiedoston muodostamiseksi tarvitaan osien iterointia, kunnes tuntematon tyyppi havaitaan.

Here is a `sample example`: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Siirtymässä 32 (heksa: 20) sijaitsee toinen pala, jonka koko on 8 ja tyyppi **mdat** (heksa: 6D 64 61 74).

Seuraava pala sijaitsee offsetissa 32+8#40 (heksa: 28) ja sen koko on 3 263 028 (heksa: 00 31 CA 34) ja tyyppi **mdat** (heksa: 6D 64 61 74) offsetissa 44 (heksadesimaali) : 2C). Seuraava pala sijaitsee offsetissa 40 + 3 263 028#3 263 068 (heksa: 00 31 CA 5C) ja sen koko on 21 189 (heksa: 00 00 52 C5) ja tyyppi **moov** (heksa: 6D 6F) 6F offset 1 836 019 574 (heksaluku: 00 31 CA 60). Tämä on viimeinen kappale, joten tiedoston kokonaiskoko on 3 263 068 + 21 189 # 3 284 257 tavua.

## Kuinka muuntaa MOV-tiedostoa?

MOV-tiedostojen muuntamiseen muihin suosittuihin videotiedostomuotoihin on saatavilla runsaasti mediasoittimia ja ohjelmisto-videoeditoreja. Jotkut mediasoittimet, jotka voivat muuntaa MOV-tiedostoja muihin muotoihin, ovat:

 * VideoLAN VLC mediasoitin
 * Eltima Elmedia Player

Useat mediasoittimet ja videoeditorit, mukaan lukien VideoLAN VLC -mediasoitin ja Eltima Elmedia Player, voivat muuntaa MOV-tiedostoja muihin muotoihin. Nämä ohjelmistot voivat muuntaa MOV-tiedostoja seuraaviin videomuotoihin.

 * MPEG-4-video – [MP4](/video/mp4/)
 * WebM-video - [WEBM](/video/webm/)
 * Video Transport Stream - [TS](/video/ts/)
 * Advanced Systems -muoto - [ASF](/video/ts/)
 * Ogg Vorbis Audio - [OGG](/audio/ogg/)
 * MP3-ääni – [MP3](/audio/mp3/)
 * Ilmainen häviötön äänikoodekki – [FLAC](/audio/flac/)
 * WAVE-ääni – [WAV](/audio/wav/)

## Avoimen lähdekoodin API MOV-tiedostoille

 * [React Native API muuntaa MOV:n MP4:ksi](https://github.com/taltultc/react-native-mov-to-mp4)
 * [Python-sovellusliittymä MOV-tiedostojen korjaamiseen](https://github.com/nrosenstein-stuff/movrepair)
 * [Ruby-sovellusliittymä MOV:n muuntamiseen GIF-muotoon](https://github.com/skygroundmedia/convert-mov-to-gif)

## Viitteet

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)


