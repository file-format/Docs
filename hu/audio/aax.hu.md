{
  "date" : "2021-06-08",
  "keywords" :[ "AAX", "fájl", "kiterjesztés", "formátum", "AAX fájl", "audio", "AAX fájlformátum", "mi az aax fájl", "AAX fájlformátum specifikációi" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az AAX fájlformátumról és az API-król, amelyek AAX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"AAX - Advanced Audio Coding File",
  "linktitle" : "AAX",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-08"
}

## Mi az AAX fájl?
Az .aax kiterjesztésű fájlok az [Audible](https://www.audible.com/) által fejlesztett hangoskönyvek; az Amazon.com Inc. tulajdonában lévő amerikai online podcast szolgáltatás és hangoskönyv. Ezeket a fájlokat az Audiblekids, az Audible.com és az iTunes Store használhatja. Az AAX fájlok digitális multimédiás hangoskönyvek, amelyek tartalmazhatnak olyan funkciókat, mint a grafika, a videók, a könyvjelzők és a videó idővonala; hasznosabbá és alkalmasabbá téve őket a gyerekeknek szóló **Képeskönyvekhez** és **Grafikai regényekhez**. Az AAX fájlok az AA fájlok továbbfejlesztett változatának minősülnek.

## AAX fájlformátum
Az AAX egy hangoskönyv fájlformátum, amely változó bitrátájának köszönhetően kiváló minőségű M4B fájl, és DRM (Digital Rights Management) titkosítási algoritmussal titkosítva van. Az e-könyvek többsége 64 kbit/s-os, 22,050 kHz-es, sztereó kódolású, némelyik 32k-s, a mono- és rádiólejátszások pedig általában 128 kbit/s-os és 44,1 kHz-es kódolásúak. Az AAX fájlformátum hangja AAC formátumban van kódolva (változó minőség).

### Az AAX fájlformátum specifikációi
A hallható AAX fájlformátum minőségi specifikációinak részletei az alábbiakban láthatók:

- **Bitráta:** 32 - 128 kbit/s
- **Mintavételi frekvencia:** 22,050 - 44,10 kHz
- **Bitmélység:** Ismeretlen
- **Csatorna:** Mono vagy sztereó
- **MByte/óra:** 28.8
- **Tartó:** MPEG-4 14. rész
- **Minőség leírása:** AAC hang

### Digitális jogkezelés (DRM)
Az Audible fájlformátumok magukba foglalják a kódolt hangokat, de tartalmazzák a jogosulatlan lejátszások megakadályozását is egy Audible felhasználónévvel és jelszóval, amely alapértelmezés szerint akár négy számítógépen és három okostelefonon is használható egyszerre. Az iskolák és a könyvtárak különféle típusú engedélyeket kaphatnak. A DRM felelős a következők ellenőrzéséért:
- A jogosulatlan felhasználói hozzáférés
- Írjon korlátozott számú CD-t a korlátlan lejátszáshoz
- Hallható tartalom engedélyezése korlátozott számú eszközön
De még mindig találhat sok más szoftvereszközt, amely könnyen megkerülheti az Audible DRM-vezérlését. Az Audible mostantól DRM-mentes címeket kínál a tartalomírók számára. Az FFmpeg 2.8.1 vagy újabb verziói képesek natív módon lejátszani az .aax fájlformátumokat.


## Referenciák ##

* [Audible (szolgáltatás) – a Wikipédia által](https://en.wikipedia.org/wiki/Audible_(service))
* [Audiofájl formátuma – a Wikipedia által](https://en.wikipedia.org/wiki/Audio_file_format)

