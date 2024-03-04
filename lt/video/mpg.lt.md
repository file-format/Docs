{
  "date": "2021-04-15",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MPG failo formatas",
  "keywords": [
"MPG",
"failą",
"pratęsimas",
"formatu",
"vaizdo formatu",
"kas yra mpg failo formatas",
"mpg failo formatas",
"mpg failų grotuvas",
"mpeg suspaudimas",
"vaizdo įrašą",
"MPEG",
"MPEG-1",
"MPEG-2"
],
  "description": "Sužinokite apie MPG failo formatą ir API, kurios gali sukurti ir parodyti, kaip atidaryti MPG failus.",
  "linktitle": "MPG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mp-ltg"
}
},
  "lastmod": "2021-07-26"
}

## Kas yra MPG failo formatas? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. Taip pat yra kitų plėtinių, pvz., .m2ts, nurodančių tikslų konteinerį, šiuo atveju MPEG-2 TS, tačiau tai mažai aktualu MPEG-1 laikmenai. [.mp3](/audio/mp3/) yra labiausiai paplitęs failų, kuriuose yra MP3 garso, plėtinys. MP3 failas yra tipiškas neapdoroto garso srautas; tradicinis MP3 failų žymėjimo būdas yra įrašyti srauto duomenis į kiekvieno kadro šiukšlių segmentus, kurie išsaugo medijos informaciją, bet yra atmesti **mpg failų grotuvo**. Tai panaši technika, naudojama AAC failams žymėti, tačiau šiais laikais ji mažiau palaikoma.

## MPEG suspaudimas ##

Pavadinimas MPEG reiškia Moving Pictures Experts Group. MPEG yra vaizdo įrašų glaudinimo įrankis, kuris apima vaizdų ir garsų suspaudimą, taip pat jų dviejų sinchronizavimą.
Šiuo metu yra keli MPEG standartai.

- MPEG-1 siūlomas vidutiniam duomenų perdavimo greičiui, maždaug 1,5 Mbit/sek.
- MPEG-2 siūlomas dideliam duomenų perdavimo greičiui, bent 10 Mbit/sek.
- MPEG-3 buvo pasiūlytas HDTV glaudinimui, tačiau buvo nustatyta, kad jis perteklinis ir buvo sujungtas su MPEG-2.
- MPEG-4 siūlomas labai mažam duomenų perdavimo greičiui, mažesniam nei 64 Kbit/sek.


## Programos srautas MPG failo formatu ##

Programos srautas yra skaitmeninio garso, vaizdo ir kt. tankinimo talpykla. Programos srauto formatas nurodytas 1-oje MPEG-1 dalyje (ISO/IEC 11172-1) ir 1-oje MPEG-2 dalyje, sistemos (ISO/IEC standartas 13818-1/ITU-T H.222.0). MPEG-2 programos srautas yra analoginis ir panašus į ISO/IEC 11172 sistemų sluoksnį ir suderinamas.

### Kodavimo informacija ###

Pateikiame dalinio MPEG-2 Program Stream paketo antraštės formato kodavimo informaciją:

| Vardas | Bitų skaičius | Aprašymas |
---|---|---|
| sinchronizuoti baitus | 32 | 0x000001BA |
| žymekliai | 2 | 01b MPEG-2 versijai. MPEG-1 versijos žymeklio bitai yra 4 bitai, kurių vertė yra 0010b. |
| Sistemos laikrodis [32..30] | 3 | Sistemos laikrodžio atskaitos (SCR) bitai nuo 32 iki 30 |
| žymeklis | 1 | 1 bitas visada nustatytas. |
| Sistemos laikrodis [29..15] | 15 | Sistemos laikrodžio bitai nuo 29 iki 15 |
| žymeklis | 1 | 1 bitas visada nustatytas. |
| Sistemos laikrodis [14..0] | 15 | Sistemos laikrodžio bitai nuo 14 iki 0 |
| žymeklis | 1 | 1 bitas visada nustatytas. |
| SCR pratęsimas | 9 | |
| žymeklis | 1 | 1 bitas visada nustatytas. |
| bitų sparta | 22 | 50 baitų per sekundę vienetais. |
| žymekliai | 2 | Visada nustatyta 11 bitų. |
| rezervuota | 5 | rezervuotas naudoti ateityje |
| įdaro ilgis | 3 | |
| užpildymo baitai | 8* įdaro ilgis | |
| sistemos antraštė (neprivaloma) | 0 ar daugiau | jei seka sistemos antraštės pradžios kodas: 0x000001BB |

Šioje lentelėje parodytas dalinės sistemos antraštės formatas:

| Vardas | Baitų skaičius | Aprašymas |
---|---|---|
| sinchronizuoti baitus | 4 | 0x000001BB |
| antraštės ilgis | 2 | |
| greičio apribojimo ir žymeklio bitai | 3 | |
| garso įrišimas ir vėliavėlės | 1 | |
| vėliavėlės, žymeklis ir vaizdo įrašas surištas | 1 | |
| Paketų spartos apribojimas ir rezervuotas baitas | 1 | |


## Nuorodos Nr.

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



