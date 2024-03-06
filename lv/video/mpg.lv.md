{
  "date": "2021-04-15",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MPG faila formāts",
  "keywords": [
"MPG",
"file",
"pagarinājumu",
"formātā",
"video formātā",
"kas ir mpg faila formāts",
"mpg faila formātā",
"mpg failu atskaņotājs",
"mpeg kompresija",
"video",
"MPEG",
"MPEG-1",
"MPEG-2"
],
  "description": "Uzziniet par MPG failu formātu un API, kas var izveidot un parādīt, kā atvērt MPG failus.",
  "linktitle": "MPG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mp-lvg"
}
},
  "lastmod": "2021-07-26"
}

## Kas ir MPG faila formāts? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. Ir arī citi paplašinājumi, piemēram, .m2ts, kas norāda precīzu konteineru, šajā gadījumā MPEG-2 TS, taču tas maz attiecas uz MPEG-1 datu nesēju. [.mp3](/audio/mp3/) ir visizplatītākais paplašinājums failiem, kas satur MP3 audio. MP3 fails ir tipiska neapstrādāta audio straume; tradicionālais veids, kā atzīmēt MP3 failus, ir straumes datu ierakstīšana katra kadra atkritumu segmentos, kas saglabā multivides informāciju, bet tos izmet **mpg failu atskaņotājs**. Šī ir līdzīga metode, ko izmanto AAC failu marķēšanai, taču mūsdienās tā tiek atbalstīta mazāk.

## MPEG saspiešana ##

Nosaukums MPEG apzīmē Moving Pictures Experts Group. MPEG ir video saspiešanas rīks, kas ietver attēlu un skaņu saspiešanu, kā arī abu sinhronizāciju.
Pašlaik ir vairāki MPEG standarti.

- MPEG-1 ir piedāvāts vidējiem datu pārraides ātrumiem, aptuveni 1,5 Mbit/sek.
- MPEG-2 ir piedāvāts lielam datu pārraides ātrumam vismaz 10 Mbit/s.
- MPEG-3 tika ierosināts HDTV saspiešanai, taču tika konstatēts, ka tas ir lieks un tika apvienots ar MPEG-2.
- MPEG-4 ir ierosināts ļoti zemam datu pārraides ātrumam, kas ir mazāks par 64 Kbit/s.


## Programmas straume MPG faila formātā ##

Programmas straume ir konteiners digitālā audio, video un cita veida multipleksēšanai. Programmas straumes formāts ir norādīts MPEG-1 (ISO/IEC 11172-1) 1. daļā un MPEG-2 sistēmas 1. daļā (ISO/IEC standarts 13818-1/ITU-T H.222.0). MPEG-2 programmu straume ir analoga, līdzīga ISO/IEC 11172 sistēmu slānim un ir saderīga ar priekšu.

### Kodēšanas informācija ###

Tālāk ir sniegta kodēšanas informācija par daļēju MPEG-2 programmas straumes pakotnes galvenes formātu:

| Vārds | Bitu skaits | Apraksts |
---|---|---|
| sinhronizēt baitus | 32 | 0x000001BA |
| marķiera uzgaļi | 2 | 01b MPEG-2 versijai. MPEG-1 versijas marķiera biti ir 4 biti ar vērtību 0010b. |
| Sistēmas pulkstenis [32..30] | 3 | Sistēmas pulksteņa atsauces (SCR) biti no 32 līdz 30 |
| marķiera uzgalis | 1 | Vienmēr iestatīts 1 bits. |
| Sistēmas pulkstenis [29..15] | 15 | Sistēmas pulksteņa biti no 29 līdz 15 |
| marķiera uzgalis | 1 | Vienmēr iestatīts 1 bits. |
| Sistēmas pulkstenis [14..0] | 15 | Sistēmas pulksteņa biti no 14 līdz 0 |
| marķiera uzgalis | 1 | Vienmēr iestatīts 1 bits. |
| SCR pagarinājums | 9 | |
| marķiera uzgalis | 1 | Vienmēr iestatīts 1 bits. |
| bitu pārraides ātrums | 22 | Vienībās 50 baiti sekundē. |
| marķiera biti | 2 | Vienmēr iestatīti 11 biti. |
| rezervēts | 5 | rezervēta izmantošanai nākotnē |
| pildījuma garums | 3 | |
| pildījuma baiti | 8*pildījuma garums | |
| sistēmas galvene (pēc izvēles) | 0 vai vairāk | ja seko sistēmas galvenes sākuma kods: 0x000001BB |

Šajā tabulā parādīts daļējas sistēmas galvenes formāts:

| Vārds | Baitu skaits | Apraksts |
---|---|---|
| sinhronizēt baitus | 4 | 0x000001BB |
| galvenes garums | 2 | |
| ātruma ierobežojumi un marķiera biti | 3 | |
| audio iesiets un karodziņi | 1 | |
| karodziņi, marķiera bits un video iesiets | 1 | |
| Pakešu ātruma ierobežojums un rezervētais baits | 1 | |


## Atsauces Nr.

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



