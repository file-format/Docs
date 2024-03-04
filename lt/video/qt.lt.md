{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QT failo formatas – greitas filmo failas",
  "keywords": [
"QT",
"QuickTime vaizdo įrašas",
"qt formatu",
"kaip paleisti qt failus",
"Greitas filmo failas",
"QTFF",
"vaizdo įrašą",
"Apple"
],
  "description": "Sužinokite apie QT failo formatą ir API, kurios gali kurti ir atidaryti QT failus.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-ltt"
}
},
  "lastmod": "2021-02-16"
}

## Kas yra QT failas?

Failas su plėtiniu .qt yra daugialypės terpės sudėtinio rodinio failas, kurį QuickTime sistema naudoja daugialypės terpės failų turiniui saugoti. Apple Inc. sukurtas QuickTime failo formatas (QTFF) yra daugialypės terpės talpyklos failas, kuriame yra garso, vaizdo ar teksto, kurį galima atkurti vėliau. Tai pasirenkamas formatas keičiantis skaitmenine laikmena tarp įrenginių, programų ir operacinių sistemų. QT failai taip pat išsaugomi [MOV](/video/mov/) formatu, kurį taip pat sukūrė Apple Inc. Kai kurios programos, kuriomis galima atidaryti QT failus, yra Apple QuickTime grotuvas, VLC medijos leistuvas ir Media Player Classic su K-Lite Codec Pack.

## QT failo formatas

QTFF yra orientuotas į objektą, kuris atskleidžia lanksčią objektų kolekciją, kad būtų lengviau analizuoti ir išplėsti. Kiekviename QT failo takelyje yra skaitmeniniu būdu užkoduotas medijos srautas arba duomenų nuoroda į medijos srautą, esantį kitame faile. Hierarchinė duomenų struktūra, kurią sudaro objektai, vadinami atomais, veikia kaip sekimo konteineriai. Apple Inc oficialiai pateikia [QT file format](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) failo formato specifikacijas kūrėjui.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Atomai

Atom yra pagrindinis QuickTime failo vienetas. Bet kuriame atome prieš kitus laukus yra du pagrindiniai laukai: Dydžio ir Tipo laukai. Dydžio lauke rodomas atomo dydis, o tipo lauke nurodomas atome saugomų duomenų tipas. Iš prigimties atomai yra hierarchiniai, o tai reiškia, kad viename atome gali būti kitų atomų, kuriuose vis dar gali būti kitų. Pavyzdinio atomo išdėstymas parodytas kitame paveikslėlyje.

Kiekvienas atomas turi dvi dalis, antraštę ir duomenis. Antraštėje yra dydžio ir tipo laukai, o duomenų dalyje yra tikrieji duomenys. Be to, kiekvienas laukas paaiškinamas toliau:

#### Atomo dydis

Atomo antraštė ir turinys nurodomi 32 bitų sveikuoju skaičiumi, žinomu kaip atomo dydis. Dydžio lauke yra atomo dydis baitais, išreikštas 32 bitų sveikuoju skaičiumi.

#### Atomo tipas

Atomo tipas taip pat rodomas 32 bitų sveikuoju skaičiumi, kuris dažniausiai traktuojamas kaip keturių simbolių laukas su knemonine verte, pvz., moov (0x6D6F6F76) filmo atomui arba trak (0x7472616B) bėgių atomas. Kai žinomas atomo tipas, jis leidžia interpretuoti jo duomenis.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Failo struktūra ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV apibrėžtas potipiu, kuris turi būti qt. Norint sukurti MOV failą, reikia kartoti gabalus, kol bus aptiktas nežinomas tipas.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. 32 poslinkyje (šeš. šešiolik.: 20) yra antrasis gabalas, kurio dydis yra 8 ir tipas **mdat** (šešiolik.: 6D 64 61 74).

Kitas gabalas yra poslinkyje 32+8#40 (šeš. šešiolik.: 28), jo dydis yra 3 263 028 (šeš. šešiolik.: 00 31 CA 34), o tipas **mdat** (šeš.: 6D 64 61 74) 44 poslinkyje (šeš. šešiolik. : 2C). Kitas gabalas yra poslinkyje 40 + 3 263 028 # 3 263 068 (šeš.: 00 31 CA 5C), jo dydis yra 21 189 (šeš. šešiolik.: 00 00 52 C5) ir tipas **moov** (šeš. šešiolik.: 6D 6F) atst. 1 836 019 574 (šeš. 00 31 CA 60). Tai yra paskutinė dalis, todėl bendras failo dydis yra 3 263 068 + 21 189 # 3 284 257 baitai.

## Nuorodos Nr.

* [QT failo formatas – Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)

* [QuickTime failo formatas – Vikipedija](https://en.wikipedia.org/wiki/QuickTime_File_Format)


