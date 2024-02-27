{
  "date": "2019-12-13",
  "keywords": [
"AC3",
"fil",
"udvidelse",
"format",
"Lydkodning",
"MPEG"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om AC3-filformat og API'er, der kan oprette og åbne AC3-filer.",
  "title": "AC3 - Audio Codec 3 fil",
  "linktitle": "AC3",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-ac-da3"
}
},
  "lastmod": "2019-12-13"
}

## Hvad er AC3 fil?

En fil med filtypenavnet .ac3 er en Audio Codec 3-fil, introduceret af Dolby Laboratories. Det er et lydformat, der kan indeholde op til seks kanalers lydoutput. Formatet var oprindeligt blevet brugt til lyd, men bruges nu også til andre applikationer såsom HDTV-udsendelser, DVD'er, Blue-ray-diske og spillekonsoller. Programmer, der kan åbne AC3-filer, omfatter Apple QuickTime-afspiller, Microsoft Windows Media Player, Winamp, MPlayer og andre lignende.

## AC3 filformat

AC3 files are binary in nature and based on the Modified Discrete Cosine Transform (MDCT) which is a lossy compression algorithm. Dolby Laboratories used the MDCT algorithm along with perceptual coding principles to develop the AC-3 audio format. This led to the release of the AC-3 format as the Dolby Digital standard in 1991. Formatet understøtter leveringen af fem kanaler til højttalere med normal frekvens (20 Hz - 20.000 Hz) og en kanal (20 Hz - 120 Hz) til de subwooferdrevne lavfrekvente effekter. AC3 understøtter samplehastigheder op til 48 kHz.

### Tekniske detaljer for AC3-filformat

Dolby Digital-teknologien bruger en meget effektiv måde til at komprimere størrelsen af multikanals lydfiler uden at forringe lydkvaliteten. Denne komprimering fører til mindre filstørrelse, hvilket gør det nemt at distribuere lydfilerne. Ved at bruge Dolby Digital er det muligt at inkludere et komplet 5.1-kanals lydmix på en filmprint eller en DVD.

#### Specifikationer
Dolby Digital-specifikationerne er som følger.

|Felt|Specifikation|
---|---|
|Kanaler |1.0 til 5.1, diskret|
|DVD-datahastighed, 5.1-kanals lyd| 384 eller 448 kbps|
|Blu-ray Disc-datahastighed, 5.1-kanals lyd|640 kbps|
|Understøtter Dolby-metadata |Ja|
|Forbindelser |S/PDIF, HDMI®, IEEE 1394|
|Mixing/streaming-funktioner|Ja|

#### MetaData-parametre

|Metadataparameter| Oplysninger|Kontrol|
---|---|---|
|Dialogniveau| |Ja|
|Kanaltilstand| | Ja|
|LFE-kanal| | Ja|
|Bitstream-tilstand| Ja| Ja|
|Linjetilstandskomprimering| | Ja|
|RF mode kompression| | Ja|
|RF overmodulationsbeskyttelse| | Ja|
|Center downmix niveau| | Ja|
|Surround downmix niveau| | Ja|
|Dolby Surround-tilstand| |Ja|
|Lydproduktionsinformation| Ja||
|Blandingsniveau| Ja||
|Rumstype| Ja||
|Copyright bit| Ja||
|Original bitstream| Ja||
|Foretrukken stereo downmix| |Ja|
|Lt/Rt Center downmix niveau||Ja|
|Lt/Rt Surround downmix niveau||Ja|
|Lo/Ro Center downmix niveau||Ja|
|Lo/Ro Surround downmix niveau||Ja|
|Dolby Digital Surround EX™-tilstand||Ja|
|A/D-konvertertype|Ja||
|DC filter||Ja|
|Lavpasfilter||Ja|
|LFE lavpasfilter||Ja|
|Surround 3 dB dæmpning||Ja|
|Surroundfaseskift||Ja|

## Referencer

* [AC3 - Af Wikiepedia](https://en.wikipedia.org/wiki/Dolby_Digital)

* [Dolby Digital 5.1](https://professional.dolby.com/tv/dolby-digital)


