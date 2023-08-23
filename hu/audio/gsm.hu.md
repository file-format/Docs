{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "file", "extension", "format", "Audio", "Global System for Mobile Audio", "gsm extension", "gsm files"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a GSM fájlformátumról és az API-król, amelyek GSM-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"GSM – Global System for Mobile Audio File Format",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Mi az a GSM fájl?

A GSM egy fájlkiterjesztés, amely a Global System for Mobile Audio Format Files programhoz van társítva. A GSM kiterjesztést tartalmazó fájlok Linux, Windows és Mac OS platformokon nyithatók meg. A GSM fájlformátum az audiofájlok kategóriába tartozik.

A GSM-fájlokat veszteséges CBR (állandó bitrátájú) hangtömörítési kodekkel kódolják. A GSM audio fájl mintavételi sebessége 8000 minta/másodperc, míg az adatátviteli sebesség körülbelül 13 kbps. A GSM-fájlokon belüli bitsebesség garantálja a hangfelvétel minőségét. Ezenkívül a GSM fájlformátumot a mobiltelefonokban használatos globális szabványos formátumnak is nevezik, és a WAV fájlok is könnyen kódolhatók GSM fájlformátum használatával. A GSM-fájlokkal kapcsolatos problémákat a felhasználó könnyedén megoldhatja anélkül, hogy szakemberhez fordulna.

A felhasználók a GSM fájlokat [MP3](/hu/audio/mp3/) és [MP4](/hu/video/mp4/) formátumba is konvertálhatják.

## A GSM fájlformátum rövid története

A GSM egy audio fájlformátum, amelyet az internetes telefonáláshoz hoztak létre Európában. Az Európai Távközlési Szabványügyi Intézet (ETSI) fejlesztette ki, hogy mobiltelefonokban és táblagépekben 2G digitális mobiltelefonként használják. Ma telefonbeszélgetések és hangüzenetek felvételeinek tárolására szolgál.

## GSM fájlformátum specifikációi ##

GSM munka egy strukturált hálózaton, amely a következő részekből áll:

- **Moduláció**: Ez egy olyan folyamat, amely során a bemeneti adatokat könnyen továbbítható formátumba alakítják át. A továbbított adatok a vevő oldalon demodulálva vannak
- **Átviteli sebesség**: A GSM egy digitális rendszer, amelynek bitsebessége meghaladja a 270 kbps-t
- **Felfelé irányuló frekvenciatartomány**: 933-960 MHz
- **Lefelé irányuló frekvenciatartomány**: 890 – 915 MHz
- **Csatornatávolság**: A szomszédos sorompók közötti távolságot jelenti, amelynek körülbelül 200 kHz-nek kell lennie.
- **Duplex távolság**: a felfelé irányuló és a lefelé irányuló frekvenciák közötti tér, amelynek 80 MHz-nek kell lennie.
- **Beszédkódolás**: A GSM lineáris prediktív kódolást (LPC) használ. Az LPC tömöríti a bitsebességet. Amikor az audiojel áthalad egy szűrőn és utánozza a hangpályát. A GSM beszédet kódolja 13 kbps sebességgel

| Hangtömörítési formátum | Algoritmus | Mintavételi arány | Bitsebességű transzformáció | Késés | CBR | VBR | Sztereó | Többcsatornás |
| ------------------------- | --------- | ----------- | ------------------- | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Igen | Nem | Nem | Nem |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Igen | Nem | Nem | Nem |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Igen | Nem | Nem | Nem |

## Referenciák ##

* [GSM – a Wikipedia által](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

