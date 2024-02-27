{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QT-filformat - hurtig filmfil",
  "keywords": [
"QT",
"QuickTime video",
"qt format",
"hvordan man spiller qt-filer",
"Hurtig film fil",
"QTFF",
"video",
"Æble"
],
  "description": "Lær om QT-filformat og API'er, der kan oprette og åbne QT-filer.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-dat"
}
},
  "lastmod": "2021-02-16"
}

## Hvad er en QT fil?

En fil med filtypen .qt er en multimediebeholderfil, der bruges af QuickTime-rammeværket til at gemme multimediefilindhold. QuickTime File Format (QTFF) er udviklet af Apple Inc. en multimediebeholderfil, der indeholder lyd, video eller tekst til afspilning senere. Det er det valgte format til udveksling af digitale medier mellem enheder, applikationer og operativsystemer. QT-filer gemmes også i [MOV](/video/mov/)-format, der også blev udviklet af Apple Inc. Nogle af de programmer, der kan åbne QT-filer, omfatter Apple QuickTime-afspiller, VLC-medieafspiller og Media Player Classic med K-Lite Codec Pack.

## QT filformat

QTFF er objektorienteret, der afslører en fleksibel samling af objekter for at lette parsing og udvidelse. Hvert spor i en QT-fil indeholder en digitalt kodet mediestrøm eller en datareference til mediestrømmen, der er placeret i en anden fil. Den hierarkiske datastruktur bestående af objekter kaldet atomer fungerer som sporbeholdere. Filformatspecifikationer for [QT file format](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) er officielt tilgængelige af Apple Inc til udviklerens reference.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Atomer

Atom er den grundlæggende enhed i QuickTime-filen. Der er to hovedfelter i ethvert atom før ethvert andet felt: Størrelses- og Typefelter. Størrelsesfeltet viser størrelsen af atomet, mens typefeltet angiver typen af data, der er gemt i atomet. Af natur er atomer hierarkiske, hvilket betyder, at et atom kan indeholde andre atomer, som stadig kan indeholde andre. Layoutet af et prøveatom er vist i det følgende billede.

Hvert atom har to dele, header og data. Overskriften indeholder felterne størrelse og type, og datadelen indeholder de faktiske data. Yderligere er hvert felt forklaret nedenfor:

#### Atomstørrelse

Atomets overskrift og indhold er angivet med et 32-bit heltal kendt som atomets størrelse. Størrelsesfeltet indeholder atomets størrelse i bytes, udtrykt i et 32-bit heltal uden fortegn.

#### Atomtype

Atomets type er også vist med et 32-bit heltal, som for det meste behandles som et felt med fire tegn med knemonisk værdi, såsom 'moov' (0x6D6F6F76) for et filmatom eller 'trak' (0x7472616B) for et sporatom. Når atomtypen er kendt, tillader den fortolkning af dens data.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Filstruktur ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV defineret af undertype, som skal være qt. For at komponere MOV-fil, kræves itererende bidder, indtil ukendt type er fundet.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Ved offset 32 (hex: 20) er placeret den anden chunk, som har en størrelse på 8 og type **mdat** (hex: 6D 64 61 74).

Den næste del er placeret ved offset 32+8#40 (hex: 28) og har en størrelse 3.263.028 (hex: 00 31 CA 34) og type **mdat** (hex: 6D 64 61 74) ved offset 44 (hex : 2C). Den næste del er placeret ved offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) og har en størrelse 21,189 (hex: 00 00 52 C5) og type **moov** (hex: 6D 6F 6F 76) ved offset 1.836.019.574 (hex: 00 31 CA 60). Dette er den sidste del, så den samlede filstørrelse er 3.263.068+21.189#3.284.257 bytes.

## Referencer ##

* [QT-filformat - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)

* [QuickTime-filformat - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


