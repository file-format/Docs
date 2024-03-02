{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QT-tiedostomuoto - nopea elokuvatiedosto",
  "keywords": [
"QT",
"QuickTime video",
"qt muodossa",
"kuinka toistaa qt-tiedostoja",
"Nopea elokuvatiedosto",
"QTFF",
"video",
"Omena"
],
  "description": "Opi QT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata QT-tiedostoja.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-fit"
}
},
  "lastmod": "2021-02-16"
}

## Mikä on QT-tiedosto?

Tiedosto, jonka tunniste on .qt, on multimediasäilötiedosto, jota QuickTime-kehys käyttää multimediatiedostojen sisällön tallentamiseen. Apple Inc:n kehittämä QuickTime File Format (QTFF) on multimediasäilötiedosto, joka sisältää ääntä, videota tai tekstiä toistettavaksi myöhemmin. Se on valittu muoto digitaalisen median vaihtamiseen laitteiden, sovellusten ja käyttöjärjestelmien välillä. QT-tiedostot tallennetaan myös [MOV](/video/mov/)-muodossa, jonka on myös kehittänyt Apple Inc. Joitakin sovelluksia, jotka voivat avata QT-tiedostoja, ovat Apple QuickTime Player, VLC-mediasoitin ja Media Player Classic K-Lite Codec Packilla.

## QT-tiedostomuoto

QTFF on oliopohjainen, joka paljastaa joustavan objektikokoelman jäsentämisen ja laajentamisen helpottamiseksi. Jokainen QT-tiedoston raita sisältää digitaalisesti koodatun mediavirran tai dataviittauksen toisessa tiedostossa olevaan mediavirtaan. Hierarkkinen tietorakenne, joka koostuu atomeiksi kutsutuista objekteista, toimii seurantasäiliöinä. Apple Inc. on virallisesti saatavilla [QT file format](https://developer.apple.com/documentation/quicktime-file-format):n tiedostomuotomääritykset kehittäjälle.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Atomit

Atom on QuickTime-tiedoston perusyksikkö. Jokaisessa atomissa on kaksi pääkenttää ennen muita kenttiä: Koko- ja Tyyppikentät. Kokokenttä näyttää atomin koon, kun taas tyyppikenttä osoittaa atomiin tallennettujen tietojen tyypin. Atomit ovat luonteeltaan hierarkkisia, mikä tarkoittaa, että yksi atomi voi sisältää muita atomeja, jotka voivat silti sisältää muita. Esimerkkiatomin asettelu näkyy seuraavassa kuvassa.

Jokaisella atomilla on kaksi osaa, otsikko ja tiedot. Otsikko sisältää koko- ja tyyppikentät ja tieto-osa sisältää varsinaiset tiedot. Lisäksi jokainen kenttä on selitetty alla:

#### Atomin koko

Atomin otsikko ja sisältö ilmaistaan 32-bittisellä kokonaisluvulla, joka tunnetaan atomin kokona. Kokokenttä sisältää atomin koon tavuina ilmaistuna 32-bittisenä etumerkittömänä kokonaislukuna.

#### Atomityyppi

Atomin tyyppi näkyy myös 32-bittisellä kokonaisluvulla, jota käsitellään enimmäkseen neljän merkin kenttänä, jolla on knemonic-arvo, kuten moov (0x6D6F6F76) elokuvaatomille tai trak (0x7472616B) raideatomi. Kun atomityyppi on tiedossa, se mahdollistaa sen tietojen tulkitsemisen.

!{{HYPERLINKKI1}}

## Tiedostorakenne ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV määritellään alatyypillä, jonka on oltava qt. MOV-tiedoston muodostamiseksi tarvitaan osien iterointia, kunnes tuntematon tyyppi havaitaan.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Siirtymässä 32 (heksa: 20) sijaitsee toinen pala, jonka koko on 8 ja tyyppi **mdat** (heksa: 6D 64 61 74).

Seuraava pala sijaitsee offsetissa 32+8#40 (heksa: 28) ja sen koko on 3 263 028 (heksa: 00 31 CA 34) ja tyyppi **mdat** (heksa: 6D 64 61 74) offsetissa 44 (heksadesimaali) : 2C). Seuraava pala sijaitsee offsetissa 40 + 3 263 028#3 263 068 (heksa: 00 31 CA 5C) ja sen koko on 21 189 (heksa: 00 00 52 C5) ja tyyppi **moov** (heksa: 6D 6F) 6F offset 1 836 019 574 (heksaluku: 00 31 CA 60). Tämä on viimeinen kappale, joten tiedoston kokonaiskoko on 3 263 068 + 21 189 # 3 284 257 tavua.

## Viitteet ##

* [QT-tiedostomuoto – Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [QuickTime-tiedostomuoto - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


