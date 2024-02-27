{
  "date": "2021-08-09",
  "keywords": [
"mmf",
"fil",
"udvidelse",
"format",
"lyd",
"smaf",
"mmf forlængelse",
"mmf filer",
"mobil musikfil",
"yamaha"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MMF filformat og API'er, der kan oprette og åbne MMF filer.",
  "title": "MMF - Mobil musikfilformat",
  "linktitle": "MMF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mm-daf"
}
},
  "lastmod": "2021-08-09"
}

## Hvad er en MMF fil?

MMF er en filtypenavn forbundet med en SMAF-fil. MMF står for Mobile Music File, mens SMAF står for syntetisk musik Mobile Application Format. MMF-filerne i en smartphone indeholder systemringetoner, lyd og kan også indeholde grafik og tekstvisning. MMF'en indeholder yderligere tre typer instrumentparametre, herunder FM, PCM og Stream PCM. Disse filformater er kompatible med Windows-systemplatformen. MMF-filerne er kategoriseret som datafiler. Normalt understøtter Microsoft Mail MMF-filer. Filen med MMF-suffiks kan kopieres til enhver mobilenhed eller systemplatform.

Desuden er disse filer meget mindre i størrelse sammenlignet med standard MIDI-formatfiler. [WAV](/audio/wav/)- og [MID](/audio/mid/)-filer kan konverteres til MMF-format, som derefter kan deles og distribueres som lydindhold. Disse filer kan modtages via e-mail direkte til telefoner og pc.


## Kort historie om MMF-filformat

Yamaha udviklede SMAF-værktøjer som lydfiler, så smartphones kan gemme et større antal unikke ringetoner. Yamaha introducerede SMAF med produktionen af deres MA-1, MA-2, MA-3, MA-5 og MA-7 LSI lydchips. Alle disse formater blev ganske velkendte blandt mobiltelefoner på det østasiatiske marked i begyndelsen af 2000.

På internationalt plan blev MMF-formatet godkendt af Samsung. Ved hjælp af MMF-formatet var Samsung i stand til at designe en bred vifte af polyfoniske ringetoner til brug i Samsung-smartphones.

Yamaha ønskede at gøre formatet endnu mere populært, og så videre, de officielle Yamaha SMAF-filer, udgav den flere værktøjer, der var kompatible med dette format. Med denne kan brugere nu nemt afspille MMF-filer på deres computere.


## MMF filformatspecifikationer ##

MMF-filer er kategoriseret i datasektioner. En præfiksstruktur omkring en 8-byte bruges til at beskrive hvert segment.
4-byte-mærket inkluderer CNTI, OPDA, MSTR, MTR og ATR. Datastørrelse plus 8 bytes er chunkstørrelsen; hele filstørrelsen beregnes ved at summere alle chunk-størrelser. Hvis en fil ikke er blevet beskadiget, skal den summerede filstørrelse være den samme som en primær headerstørrelse.

### Header ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Her er et eksempel på MMF-fil:

![](../mmf.png)

## Referencer

* [MMF - af Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


