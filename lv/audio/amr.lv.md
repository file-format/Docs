{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"failu",
"pagarinājumu",
"formātā",
"kas ir amr fails",
"mūzika",
"amr faila formāts",
"amr fails",
"konvertēt amr failu uz mp3",
"atskaņot amr failu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par AMR failu formātu un API, kas var izveidot, konvertēt un atvērt AMR failus.",
  "title": "AMR — adaptīvs vairāku ātrumu kodeku fails",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-lvr"
}
},
  "lastmod": "2021-04-29"
}

## Kas ir AMR fails?
Fails ar paplašinājumu .amr ir audio datu formāts, kas attiecas uz **Adaptive Multi-Rate** audio kodeku; sastāv no vairāku ātrumu šaurjoslas runas kodeka, kas kodē šaurjoslas signālus ar 4,75-12,2 kbit/s bitu pārraides ātrumu ar maksas kvalitātes runu, sākot no 7,4 kbit/s; izmanto saites adaptāciju, lai izvēlētos vienu no astoņiem dažādiem bitu pārraides ātrumiem.

## AMR faila formāts
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. AMR faila formāts tiek izmantots arī, lai saglabātu runāto audio, izmantojot **Adaptive Multi-Rate** audio kodeku, ko izmanto daudzi viedtālruņi, lai saglabātu ierakstītas runas.

### Faila formāta struktūra
AMR (Adaptive Multi-Rate) ir audio formāts; plaši izmanto dažādās mobilajās lietojumprogrammās un ierīcēs, parasti audio atskaņotājos/rakstītājos vai VoIP lietojumprogrammās. AMR var klasificēt arī šādi:

1. AMR-NB (šaurjosla)
2. AMR-WB (platjosla)

Parasti AMR attiecas uz AMR-NB. AMR faila formātam ir šāda struktūra:

Katrā AMR failā ir 6 baitu galvene, kas atpazīst failu kā AMR audio. Šī galvene vienmēr ir iestatīta uz:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Tas parasti ir līdzīgs visiem AMR-NB failiem. Ja galvene atbilst standartam, iespējams, fails ir bojāts un to nevajadzētu izmantot. AMR fails sastāv no vesela skaita iesaiņotu audio kadru. Katrs no šiem kadriem veido 20 ms audio. Katru kadru var kodēt, izmantojot jebkuru no derīgajiem AMR-NB režīmiem (0-7, 8 SID DTX režīmā). Tā kā kadrus var kodēt ar dažādiem bitu pārraides ātrumiem, šo tipisko metodi sauc par adaptīvo vairāku ātrumu (AMR).
#### AMR režīmi
Tālāk ir norādīti dažādi AMR režīmi un tiem atbilstošie bitu pārraides ātrumi:

|MODE| BITU LIKUMI|
---|---|
|0| AMR 4,75 — kodē ar ātrumu 4,75 kbit/s|
|1 | AMR 5.15 — kodē ar ātrumu 5,15 kbit/s|
|2 | AMR 5.9 — kodē ar ātrumu 5,9 kbit/s|
|3 | AMR 6.7 — kodē ar ātrumu 6,7 kbit/s|
|4 | AMR 7.4 — kodē ar ātrumu 7,4 kbit/s|
|5 | AMR 7,95 — kodē ar ātrumu 7,95 kbit/s|
|6 | AMR 10.2 — kodē ar ātrumu 10,2 kbit/s|
|7 | AMR 12.2 — kodē ar ātrumu 12,2 kbit/s|

AMR režīmu kadra lielums baitos (ieskaitot galvenes baitu) ir norādīts tālāk:

|CMR |MODE |KARAM IZMĒRS(baitos )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Atsauces Nr.

* [Adaptive Multi-Rate audio kodeks — Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [RTP slodzes formāts un failu krātuves formāts AMR un AMR-WB audio kodekiem](https://tools.ietf.org/html/rfc4867#page-35)


