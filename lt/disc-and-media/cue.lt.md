{
  "date": "2021-06-09",
  "keywords": [
"užuomina",
"failą",
"pratęsimas",
"formatu",
"kas yra signalo failas",
"muzika",
"cue failo formatas",
"cue failo formato specifikacija",
"užuominos lapas",
"CDRWIN"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CUE failų formatą ir API, kurios gali kurti, konvertuoti ir atidaryti CUE failus.",
  "title": "CUE – Cue lapo failas",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cu-lte"
}
},
  "lastmod": "2021-07-01"
}

## Kas yra CUE failas?

Failas su plėtiniu .cue, taip pat žinomas kaip cue lapo failas, yra metaduomenų failas, kuriame yra informacijos apie takelių išdėstymą kompaktiniame arba DVD diske. Juos palaiko medijos leistuvai ir optinių diskų kūrimo programos. Pagrindinius kompaktiniame diske saugomus garso duomenis nurodo signalo failas, taip pat takelių ilgio, disko pavadinimų ir atlikėjų specifikacijos. Taigi, jei viename garso faile yra keli takeliai, signalo failas gali būti naudojamas padalyti garsą į kelis failus arba nurodyti įvairius takelius.

## CUE failo formatas

CUE arba cue lapų failai saugomi paprasto teksto formatu, kurį gali įskaityti žmogus. Informacija žymos faile yra komandos su vienu ar daugiau parametrų. Šios komandos taikomos visam failui arba atskiram takeliui, priklausomai nuo konkrečios komandos ir konteksto. CDRWIN vartotojo vadove aprašomos ženklinimo lapo sintaksės ir semantikos specifikacijos.

## CUE lapo pagrindinės komandos

|Komanda|Aprašymas|
---|---|
|FAILAS| Nurodo failą su duomenimis ir jo formatą, pvz., [MP3](/audio/mp3/), [WAV](/audio/wav/) arba paprastą dvejetainį disko vaizdą)|
|TRAKAS| Apibrėžia takelio konteksto informaciją, pvz., numerį ir tipą arba režimą.|
|INDEKSAS| Nurodo poziciją kaip indeksą FILE. Formatas yra mm:ss:ff (minutės-sekundės kadras).|
|PREGAP ir POSTGAP|Tai rodo takelio išankstinį arba po jo esantį tarpą, kuris nėra saugomas jokiame duomenų faile. Ilgis nurodytas tuo pačiu minučių-sekundės kadro formatu kaip ir INDEX.|

### CUE lapo pavyzdys

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```

## Kiti CUE failai

Štai kiti failų tipai, kuriuose naudojamas **.cue** failo plėtinys.

**Diskas ir laikmena**
- [CUE – Cue lapo failas](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## Nuorodos

* [.cda failas – pateikė Vikipedija](https://en.wikipedia.org/wiki/.cda_file)


