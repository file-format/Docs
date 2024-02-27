{
  "date": "2021-08-05",
  "keywords": [
"gsm",
"fil",
"udvidelse",
"format",
"Lyd",
"Globalt system til mobil lyd",
"gsm udvidelse",
"gsm filer"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om GSM-filformat og API'er, der kan oprette og åbne GSM-filer.",
  "title": "GSM - Globalt system til mobil lydfilformat",
  "linktitle": "GSM",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-gs-dam"
}
},
  "lastmod": "2021-08-05"
}

## Hvad er en GSM fil?

GSM er en filtypenavn, der er forbundet med Global System for Mobile Audio Format Files. Filer, der indeholder GSM-udvidelser, kan åbnes på Linux-, Windows- og Mac OS-platforme. GSM-filformatet tilhører kategorien lydfiler.

En GSM-fil er kodet med en tabsgivende CBR (Constant bitrate) lydkomprimeringscodec. Samplingshastigheden i en GSM-lydfil er 8000 samples/sekund, mens datahastigheden er omkring 13 kbps. Bithastigheden i GSM-filerne sikrer kvalitet under stemmeoptagelse. Desuden er GSM-filformatet også kendt som det globale standardformat, der skal bruges i mobiltelefoner, og WAV-filer kan også nemt kodes ved hjælp af et GSM-filformat. Eventuelle problemer med en GSM-fil kan nemt løses af brugeren selv uden at gå til en ekspert.

Brugere kan også konvertere GSM-filer til formaterne [MP3](/audio/mp3/) og [MP4](/video/mp4/).

## Kort historie om GSM-filformat

GSM er et lydfilformat, der blev skabt til internettelefoni i Europa. Det blev udviklet af European Telecommunications Standard Institute (ETSI) til at blive brugt som en 2G digital mobiltelefon, der bruges i mobiltelefoner og tablets. I dag bruges det til at gemme optagelser af telefonsamtaler og talebeskeder.

## GSM-filformatspecifikationer ##

GSM-arbejde på et struktureret netværk, der består af følgende sektioner:

- **Modulation** : Det er en proces med at transformere inputdata til et format, der nemt kan transmitteres. De transmitterede data demoduleres i den modtagende ende
- **Transmissionshastighed**: GSM er et digitalt system, der har en over bithastighed på 270 kbps
- **Uplink-frekvensområde**: 933-960 MHz
- **Downlink-frekvensområde**: 890 – 915 MHz
- **Kanalafstand**: Det betyder afstanden mellem tilstødende barrierer, som skal være omkring 200 kHz
- **Duplex Distance** : Det er mellemrummet mellem uplink- og downlink-frekvenser, der skal være 80 MHz
- **Talekodning**: GSM bruger Linear Predictive Coding (LPC). LPC komprimerer bithastigheden. Når lydsignalet passerer gennem et filter og efterligner stemmekanalen. GSM-koder tale ved 13kbps

| Lydkomprimeringsformat | Algoritme | Sample rate | Bithastighedstransformation | Latency | CBR | VBR | Stereo | Multikanal |
| ------------------------ | ---------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Ja | Nej | Nej | Nej |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Ja | Nej | Nej | Nej |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Ja | Nej | Nej | Nej |

## Referencer ##

* [GSM - af Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)


