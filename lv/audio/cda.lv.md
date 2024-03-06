{
  "date": "2021-06-09",
  "keywords": [
"cda",
"failu",
"pagarinājumu",
"formātā",
"kas ir cda fails",
"mūzika",
"cda faila formātā",
"cda faila formāta specifikācija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CDA failu formātu un API, kas var izveidot, konvertēt un atvērt CDA failus.",
  "title": "CDA — CD audio celiņa saīsnes fails",
  "linktitle": "CDA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-cda"
}
},
  "lastmod": "2021-06-09"
}

## Kas ir CDA fails?

Fails ar paplašinājumu .cda ir mazs fails, ko Microsoft Windows ģenerē katram audio kompaktdiskā esošajam audio celiņam. Šajos failos ir ietverta tipiska informācija, piemēram, ierakstu laiki un Windows saīsne, kas lietotājiem ļauj piekļūt konkrētiem audio celiņiem. CDA faili nav mūzika, bet tie norāda uz mūzikas failu, kas atrodas kaut kur atmiņā. Mēs to varam teikt kā audio faila saīsni, kas atrodas kompaktdiskā.

## CDA faila formāts

CDA faila formātu izmanto, lai pateiktu datoram, kuru audio failu atskaņot kompaktdiskā. Tādējādi CDA faili kļūst bezjēdzīgi atdalīti no kompaktdiska, ko tie pārstāv. CDA faili parasti tiek uzskatīti par RIFF resursiem. Pašreizējā .cda faila versijā ir tikai viens gabals ar nosaukumu CDDA un satur tikai vienu datu bloku ar nosaukumu FMT. Šis bloks ir 24 baitus garš. Operētājsistēmas Windows izveidoto identifikatoru izmanto ar Windows 95 un Windows 98 saistītais CD diskdzinis, un tā atskaņotājs nevar izveidot savienojumu ar FreeDB vai CDDB. Lai tas varētu parādīt dziesmas nosaukumu un izpildītāja vārdu, jums ir manuāli jāievada šī informācija failā cdplayer.ini.

### CDA faila organizēšana

Šajā tabulā ir parādīta informācija par tipiskām nobīdēm:
| kompensēt | garums | saturs |
---|---|---|
| 0x00 | 4 | 4 ASCII rakstzīmes RIFF |
| 0x04 | 4 | šāda gabala lielums: vienmēr 36 (44–8), 4 baiti (Intel secībā) |
| 0x08 | 4 | chunk identifier: the 4 ASCII characters "CDDA"-lv |
| 0x0C | 4 | 3 ASCII rakstzīmes fmt, kam seko atstarpe |
| 0x10 | 4 | gabala garums: vienmēr 24, 4 baiti (Intel pasūtījums) |
| 0x14 | 2 | version of the CD format, on 2 bytes (Intel order). In May 2006, always equal to 1. |
| 0x016 | 2 | number of the range, on 2 bytes (Intel order). The first track has the number 1. |
| 0x18 | 4 | identifikators, ko sistēma Windows aprēķināja failam cdplayer.exe. |
| 0x1c | 4 | diapazona nobīde, kadru skaitā (Intel secībā) |
| 0x20 | 4 | celiņa ilgums, kopējais kadru skaits (Intel pasūtījums) |
| 0x24 | 1 | diapazona pozīcija: rāmji |
| 0x25 | 1 | diapazona pozīcija: sekundes |
| 0x26 | 1 | diapazona pozīcija: minūtes |
| 0x27 | 1 | nulles baits (binārā vērtība 0) |
| 0x28 | 1 | trases ilgums: kadri |
| 0x29 | 1 | trases ilgums: sekundes |
| 0x2a | 1 | trases ilgums: minūtes |
| 0x2b | 1 | nulles baits (binārā vērtība 0) |

## Atsauces

* [.cda fails — Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


