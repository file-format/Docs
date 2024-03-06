{
  "date": "2021-04-26",
  "keywords": [
"aiff",
"failu",
"pagarinājumu",
"formātā",
"audio apmaiņas faila formāts",
"mūzika",
"aiff faila formāts",
"aiff uz mp3",
"aiff vs wav",
"konvertēt aiff uz mp3"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par AIFF failu formātu un API, kas var izveidot, konvertēt un atvērt AIFF failus.",
  "title": "AIFF — audio apmaiņas faila formāts",
  "linktitle": "AIFF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-aif-lvf"
}
},
  "lastmod": "2021-04-26"
}

## Kas ir AIFF fails?
AIFF (Audio Interchange File Format) ir nesaspiests audio faila formāts, ko Apple izstrādāja 1998. gadā, bet tā pamatā ir **EA IFF 85** (Standard for Interchange Format Files, ko izstrādājis Electronic Arts), kas ir iesaiņojuma formāts, ko izmanto Amiga sistēmās. . Šis faila formāts ir izstrādāts ar standartu izlases skaņu glabāšanai. Formāts ir pietiekami elastīgs, un tas ļauj saglabāt monofoniskas vai daudzkanālu izlases skaņas ar dažādiem izlases ātrumiem un izlases platumiem. Tā kā AIFF faili ir nesaspiesti, tie ir lielāki nekā citi formāti ar zaudējumiem, piemēram, [MP3](/audio/mp3/).

AIFF faili sastāv no 2 nesaspiesta stereo audio kanāliem ar 16 bitu izlases lielumu, kas ierakstīts ar frekvenci 44,1 khz. Augstas audio kvalitātes dēļ 5 minūšu audio var aizņemt līdz 50 MB vietas diskā, kas ir līdzīgs faila formātam [WAV](/audio/wav/).

## AIFF pret WAV

AIFF un WAV kvalitātes ziņā ir gandrīz vienādi. Abos no tiem tiek izmantots viens un tas pats PCM (impulsa koda modulācijas) kodējums, kas padara tos lielākus, salīdzinot ar citiem zudumu formātiem, piemēram, [MP3](/audio/mp3/), [M4A](/audio/m4a/). Dažas no vispārīgajām atšķirībām ir uzrakstītas zemāk esošajā tabulā:

|AIFF|WAV|
---|---|
|Tiek izmantots galvenokārt MAC|Pārsvarā tiek izmantots personālajiem datoriem|
|Atļauj metadeta| Neatļauj metadeta|

## AIFF failu struktūra

**EA IFF 85** nosaka vispārējo struktūru datu glabāšanai failos. **EA IFF 85** fails sastāv no vairākiem datu gabaliem. AIFF faila gabals sastāv no galvenes informācijas, kam seko dati:
{{< figure src="../chunk.png" alt="AIFF gabals" >}}

AIFF fails ir vairāku dažādu veidu gabalu kolekcija. Ir divi vispārīgi gabalu veidi, kas ir svarīgi, lai izveidotu AIFF faila daļu:
- **Common Chunk**: satur svarīgus parametrus, kas apraksta izlases skaņu, piemēram, tās garums un izlases ātrums.
- **Skaņas datu daļa**: satur faktiskos audio paraugus.
Ir daudz citu izvēles daļu, kas uzskaita instrumenta parametrus, definē marķierus, saglabā lietojumprogrammas informāciju utt.

### Vietējie gabalu veidi

Daļu veidi, kas veido AIFF, ir norādīti tabulā:

|Grupas veids| Apraksts|
---|---|
|Common Chunk|Common Chunk apraksta izlases skaņas pamatparametrus|
|Skaņas datu gabals|Skaņas datu gabals satur faktiskos paraugu kadrus|
|Marker Chunk|Marķiera gabalā ir marķieri, kas norāda uz pozīcijām skaņas datos|
|Instrument Chunk|Instrument Chunk definē pamatparametrus, ko instruments, piemēram, paraugs, var izmantot skaņas datu atskaņošanai|
|MIDI Data Chunk|MIDI Data Chunk var izmantot, lai saglabātu MIDI datus|
|Audio ierakstīšanas daļa|Audio ierakstīšanas gabals satur informāciju, kas attiecas uz audio ierakstīšanas ierīcēm|
|Lietojumprogrammai specifisks gabals|Lietojumprogrammas specifisko daļu var izmantot jebkādiem mērķiem lietojumprogrammu ražotāji|
|Komentāru daļa|Komentāru daļa tiek izmantota, lai saglabātu komentārus FORM AIFF|
|Teksta gabali - vārds, autors, autortiesības, anotācija| Visi ir teksta gabali|

## Atsauces Nr.

* [Audio apmaiņas faila formāts — Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)


