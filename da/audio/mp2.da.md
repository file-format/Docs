{
  "date": "2021-06-11",
  "keywords": [
"mp2",
"mp2-fil",
"udvidelse",
"format",
"hvad er en mp2-fil",
"musik",
"mp2 filformat"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MP2-filformater og API'er, der kan oprette, konvertere og åbne MP2-filer.",
  "title": "MP2 - MPEG Layer 2 lydfilformat",
  "linktitle": "MP2",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mp-da2"
}
},
  "lastmod": "2021-06-11"
}

## Hvad er en MP2-fil?

En MP2-fil, som også kaldes MPA-fil, er en lydfil komprimeret med Layer II af MPEG-1 eller MPEG-2; et tabsgivende lydkomprimeringsformat defineret af ISO/IEC 11172-3 sammen med MPEG-1 Audio Layer I og MPEG-1 Audio Layer III ([MP3](/audio/mp3/)), for at reducere lydfilstørrelsen. Hvorimod MP3 er mere populær end MP2 på grund af dens mindre størrelse og tilgængelighed over internettet. Derfor er MP2 stadig en vital standard for lydudsendelser.

## MP2 filformat

MPEG Audio Layer II (MP2) er kernealgoritmen i MP3-standarderne. MPEG-1 Audio Layer 2-kodning blev hentet fra MUSICAM audio codec. Det startede som Digital Audio Broadcast (DAB)-projektet i Tyskland som en del af EUREKA-forskningsprogrammet. Eureka 147 indeholdt tre hovedelementer: Transmission Coding & Multiplexing, COFDM Modulation og MUSICAM Audio Coding (Masking pattern Universal Sub-band Integrated Coding And Multiplexing). MUSICAM var en af de få kodninger, som var i stand til at opnå høj lydkvalitet ved bithastigheder i området 64 til 192 kbit/s pr. monofonisk kanal. Målet var at levere lav forsinkelse, lav kompleksitet, fejlrobusthed, korte adgangsenheder og opfylde de tekniske krav til udsendelse, telekommunikation og optagelse på digitale lagringsmedier.

MP2 er en sub-band audio encoder, som kan komprimeres i tidsdomænet med en low-delay filterbank, der genererer 32 frekvensdomænekomponenter. Til sammenligning er MP3 en transformation audio encoder med hybrid filterbank, hvilket betyder, at komprimering anvendes i frekvensdomænet efter en hybrid transformation fra tidsdomænet. MP2-koderen kan udnytte interkanalredundanser ved at bruge valgfri joint stereo-intensitetskodning.

### MP2-filformatspecifikationer

MP2-filformatet er baseret på successive digitale frames med 1152 samplingsintervaller med fire mulige formater:

- monoformat
- stereoformat
- intensitetskodet joint stereo format (stereo irrelevans)
- dual channel (ukorreleret) format
Nogle vigtige tekniske specifikationer for MP2 er angivet i tabellen nedenfor:

|Specifikation| Beskrivelse|
---|---|
|**Sampling rates**| 32, 44,1 og 48 kHz|
|**Bithastigheder**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 og 384 kbit/s|
|**Yderligere samplingshastigheder**|16, 22,05 og 24 kHz|
|**Yderligere bithastigheder**|8, 16, 24, 40 og 144 kbit/s|
|**Multikanalunderstøttelse**|Op til 5 lydkanaler i fuld rækkevidde og en LFE-kanal (Low Frequency Enhancement-kanal)|

## Referencer ##

* [MPEG-1 Audio Layer II - Af Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


