{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "fil", "tillägg", "format", "Ljud", "Globalt system för mobilt ljud", "gsm-tillägg", "gsm-filer"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om GSM-filformat och API:er som kan skapa och öppna GSM-filer.",
  "title" :"GSM - Global System for Mobile Audio File Format",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Vad är en GSM-fil?

GSM är ett filtillägg som är associerat med Global System for Mobile Audio Format Files. Filer som innehåller GSM-tillägg kan öppnas på Linux-, Windows- och Mac OS-plattformar. GSM-filformatet tillhör kategorin ljudfiler.

En GSM-fil är kodad med en förlustfri CBR (Constant bitrate) ljudkomprimeringscodec. Samplingshastigheten i en GSM-ljudfil är 8000 sampel/sekund medan datahastigheten är cirka 13 kbps. Bithastigheten i GSM-filerna säkerställer kvalitet under röstinspelning. Dessutom är GSM-filformatet också känt som det globala standardformatet som ska användas i mobiltelefoner och WAV-filer kan också enkelt kodas med ett GSM-filformat. Eventuella problem med en GSM-fil kan enkelt lösas av användaren själv utan att gå till en expert.

Användare kan också konvertera GSM-filer till formaten [MP3](/sv/audio/mp3/) och [MP4](/sv/video/mp4/).

## Kort historik över GSM-filformat

GSM är ett ljudfilformat som skapades för internettelefoni i Europa. Den har utvecklats av European Telecommunications Standard Institute (ETSI) för att användas som en digital 2G-mobil som används i mobiltelefoner och surfplattor. Idag används den för att lagra inspelningar av telefonsamtal och röstmeddelanden.

## GSM-filformatspecifikationer ##

GSM-arbete på ett strukturerat nätverk som består av följande sektioner:

- **Modulation** : Det är en process att omvandla indata till ett format som enkelt kan överföras. Den överförda datan demoduleras vid den mottagande änden
- **Sändningshastighet** : GSM är ett digitalt system som har en bithastighet över 270 kbps
- **Upplänksfrekvensområde**: 933-960 MHz
- **Nedlänksfrekvensområde**: 890 – 915 MHz
- **Kanalavstånd**: Det betyder avståndet mellan intilliggande barriärer som bör vara cirka 200 kHz
- **Duplexavstånd** : Det är utrymmet mellan upplänks- och nedlänksfrekvenser som ska vara 80 MHz
- **Talkodning** : GSM använder linjär prediktiv kodning (LPC). LPC komprimerar bithastigheten. När ljudsignalen passerar genom ett filter och härmar röstkanalen. GSM-kodar tal vid 13 kbps

| Ljudkomprimeringsformat | Algoritm | Samplingsfrekvens | Bithastighetsomvandling | Latens | CBR | VBR | Stereo | Flerkanaligt |
| ------------------------ | ---------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Ja | Nej | Nej | Nej |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Ja | Nej | Nej | Nej |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Ja | Nej | Nej | Nej |

## Referenser ##

* [GSM - av Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

