{
  "date": "2019-10-11",
  "keywords": [
"mov failą",
"mov failo formatas",
"kas yra mov failas",
"failą",
"mov pavyzdys",
"mov failo plėtinys",
"pratęsimas",
"formatu",
"QuickTime",
"MPEG-4"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MOV failas – Apple QuickTime filmo failo formatas",
  "description": "Sužinokite apie MOV failo formatą ir API, kurios gali kurti ir atidaryti MOV failus.",
  "linktitle": "MOV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mo-ltv"
}
},
  "lastmod": "2021-07-29"
}

## Kas yra MOV failas?

MOV failas yra vaizdo įrašo failo tipas, sukurtas Apple Inc., kuriame yra vienas ar daugiau takelių. Kiekviename takelyje saugomas filmas, garso įrašas, filmų klipai ir subtitrai. Tai daugialypės terpės talpykla, kurioje galima laikyti įvairaus tipo medijos elementus. MOV vaizdo formatas suderinamas su Windows ir Macintosh sistemomis. Jis naudoja MPEG-4 koduotą glaudinimui, o takeliai palaikomi objektuose, vadinamuose atomais, kurie yra patalpinti į hierarchinę duomenų struktūrą.

## Trumpa MOV failo formato istorija

MPEG-4 file format has evolved from QuickTime File Format (**QTFF**) specification in 2001. Tarptautinė standartizacijos organizacija patvirtino formatą, o MPEG-4 1 dalies sistemos specifikacijos buvo paskelbtos 1999 m. 2001 m. buvo paskelbtas pataisytas failo formatas [MP4](/video/mp4/).

Pirmoji MP4 versija buvo peržiūrėta 2003 m. kaip MPEG-4 14 dalis (ISO/IEC 14496-14:2003). 2004 m. MP4 buvo apibendrintas siekiant apibrėžti bendrą visų laiko pagrindu veikiančių medijos failų struktūrą. Todėl dabar jis naudojamas kaip įvairių kitų daugialypės terpės failų formatų pagrindas.

## „QuickTime“ failo formatas (QTFF) – daugiau informacijos

Norint dirbti su skaitmenine multimedija, QTFF gali talpinti daugybę duomenų. Tai keitimosi skaitmeninėmis laikmenomis idėjos formatas, nes formatas apibrėžia bet kokios rūšies žiniasklaidos struktūrų apibūdinimo standartus. Failo formatas susideda iš lanksčios objektų orientuotų objektų kolekcijos. Filmų saugojimui diskuose QuickTime naudoja dvi struktūras, ty atomus ir QT atomus.

### Atomai

Atom yra pagrindinis QuickTime failo vienetas. Bet kuriame atome prieš kitus laukus yra du pagrindiniai laukai: Dydžio ir Tipo laukai. Dydžio lauke rodomas atomo dydis, o tipo lauke nurodomas atome saugomų duomenų tipas. Iš prigimties atomai yra hierarchiniai, o tai reiškia, kad viename atome gali būti kitų atomų, kuriuose vis dar gali būti kitų. Pavyzdinio atomo išdėstymas parodytas kitame paveikslėlyje.

Kiekvienas atomas turi dvi dalis: antraštę ir duomenis. Antraštėje yra dydžio ir tipo laukai, o duomenų dalyje yra tikrieji duomenys. Be to, kiekvienas laukas paaiškinamas toliau:

### Atomo dydis

Atomo antraštė ir turinys nurodomi 32 bitų sveikuoju skaičiumi, žinomu kaip atomo dydis. Dydžio lauke yra atomo dydis baitais, išreikštas 32 bitų sveikuoju skaičiumi.

### Atomo tipas

Atomo tipas taip pat rodomas 32 bitų sveikuoju skaičiumi, kuris dažniausiai traktuojamas kaip keturių simbolių laukas su knemonine verte, pvz., moov (0x6D6F6F76) filmo atomui arba trak (0x7472616B) bėgių atomas. Kai žinomas atomo tipas, jis leidžia interpretuoti jo duomenis.

### QT atomai ir atomų konteineriai

QT atomai suteikia bendrosios paskirties saugojimo formatą ir turi išplėstą antraštę, kurią sudaro laukai Size, Type, Atom ID ir Count of Child atoms. QT atomai yra suvynioti į atomų konteinerį, unikalią duomenų struktūrą, turinčią antraštę su užrakto skaičiumi. Kiekviename atomo konteineryje yra vienas šaknies atomas, kuris yra QT atomas. QT atomo išdėstymas parodytas paveikslėlyje žemiau.

QT atomo konteinerio antraštėje yra šie duomenys:

Rezervuotas: 10 baitų elementas, kurio reikšmė yra 0.

Užrakinimo skaičius: 16 bitų sveikasis skaičius, kurio vertė yra 0.

QT atomo antraštėse yra šie duomenys:

**Dydis –** QT atomo antraštė ir turinys nurodomi baitais 32 bitų sveikuoju skaičiumi. Lapo atomo atveju šiame lauke yra vieno atomo dydis.

**Tipas –** Atomo tipas žymimas 32 bitų sveikuoju skaičiumi. Jei tai yra šakninis atomas, tada reikšmė nustatoma į sean.

**Atom ID –** Tai 32 bitų sveikasis skaičius, rodantis atomo ID ir turi būti unikalus visiems broliams ir seserims. Šaknies atomas visada turi atomo ID reikšmę kaip 1.

**Rezervuota –** 16 bitų sveikasis skaičius, kuris turi būti nustatytas į 0.

**Vaikų skaičius –** 16 bitų sveikasis skaičius, nurodantis antrinių atomų atomų skaičių.

**Rezervuota –** 32 bitų sveikasis skaičius, kuris turi būti nustatytas į 0.

## MOV failų failų struktūra

MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV apibrėžtas potipiu, kuris turi būti qt. Norint sukurti MOV failą, reikia kartoti gabalus, kol bus aptiktas nežinomas tipas.

Here is a `sample example`: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. 32 poslinkyje (šeš. šešiolik.: 20) yra antrasis gabalas, kurio dydis yra 8 ir tipas **mdat** (šešiolik.: 6D 64 61 74).

Kitas gabalas yra poslinkyje 32+8#40 (šeš. šešiolik.: 28), jo dydis yra 3 263 028 (šeš. šešiolik.: 00 31 CA 34), o tipas **mdat** (šeš.: 6D 64 61 74) 44 poslinkyje (šeš. šešiolik. : 2C). Kitas gabalas yra poslinkyje 40 + 3 263 028 # 3 263 068 (šeš.: 00 31 CA 5C), jo dydis yra 21 189 (šeš. šešiolik.: 00 00 52 C5) ir tipas **moov** (šeš. šešiolik.: 6D 6F) atst. 1 836 019 574 (šeš. 00 31 CA 60). Tai yra paskutinė dalis, todėl bendras failo dydis yra 3 263 068 + 21 189 # 3 284 257 baitai.

## Kaip konvertuoti MOV failą?

Yra daug daugialypės terpės grotuvų ir programinės įrangos vaizdo redaktorių, skirtų MOV failams konvertuoti į kitus populiarius vaizdo failų formatus. Kai kurie medijos leistuvai, galintys konvertuoti MOV failus į kitus formatus, yra šie:

 * VideoLAN VLC medijos grotuvas
 * Eltima Elmedia Player

Keletas daugialypės terpės grotuvų ir vaizdo įrašų redaktorių, įskaitant VideoLAN VLC medijos leistuvą ir Eltima Elmedia Player, gali konvertuoti MOV failus į kitus formatus. Ši programinė įranga gali konvertuoti MOV failus į šiuos vaizdo formatus.

 * MPEG-4 vaizdo įrašas – [MP4](/video/mp4/)
 * WebM vaizdo įrašas – [WEBM](/video/webm/)
 * Vaizdo įrašų perdavimo srautas – [TS](/video/ts/)
 * Išplėstinių sistemų formatas – [ASF](/video/ts/)
 * Ogg Vorbis Audio – [OGG](/audio/ogg/)
 * MP3 garsas – [MP3](/audio/mp3/)
 * Nemokamas Lossless garso kodekas – [FLAC](/audio/flac/)
 * WAVE garsas – [WAV](/audio/wav/)

## MOV failų atvirojo kodo API

 * [React Native API, skirta MOV konvertuoti į MP4](https://github.com/taltultc/react-native-mov-to-mp4)
 * [Python API, skirta MOV failams taisyti](https://github.com/nrosenstein-stuff/movrepair)
 * [Ruby API, skirta MOV konvertuoti į GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Nuorodos

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)


